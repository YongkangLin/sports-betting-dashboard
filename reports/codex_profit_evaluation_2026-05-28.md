# Codex Profit Evaluation - 2026-05-28

Repo state reviewed after fast-forwarding `main` to `18b6321`.
Local audit/ranker were rerun after the score backfill.

## Data Snapshot

- Odds warehouse: 9,334 events, 4,065,556 quotes, 7,630 settled score rows.
- Polymarket observations are still thin. MLB has 3,282 rows across 314 events, but only a 22 day span (`2026-04-28` to `2026-05-21`).
- NBA has 556 obs across 45 events; NHL has 510 obs across 42 events; NFL matching currently has 0 obs.
- `scripts/87_data_audit.py` flags every Polymarket observation file as below the 90 day validation requirement.

## Main Findings

1. Broad sportsbook line-shopping results are not deployable.
   - `scripts/60_realized_pnl_v4.py` prints a strong historical result overall, driven by NHL.
   - The stricter NHL artifact already in the repo (`data/processed/nhl_strict_bets.parquet`) contradicts that: 2,023 strict NHL bets have ROI -2.09%, and positive-edge NHL rows are also negative.
   - Interpretation: the broad v4 NHL edge is likely stale-line, matching, timestamp, or selection artifact. Do not trade it.

2. One-sided soft-book betting did not validate.
   - `scripts/79_one_sided_edge_hunt.py` tested 23 cells after the score update.
   - Strict passes: 0.
   - Best visible cell was NBA h2h all-soft at min edge 2%, but test CI crosses zero.

3. Polymarket-only execution has one watchlist signal, not a live-capital signal.
   - `scripts/84_polymarket_edge_ranker.py` found two strict research passes, both MLB h2h at 2h lead:
     - min edge 1.0%, n_qual 66, test_n 27, test ROI +41.5%, CI lower +4.6%.
     - min edge 0.5%, n_qual 146, test_n 59, test ROI +27.7%, CI lower +2.1%.
   - The Kelly-stake warehouse hunt still has 0 strict passes.
   - Interpretation: paper trade MLB 2h only. The sample is too short and too small for real sizing.

4. Pure arbitrage is mathematically strongest, but operationally hardest.
   - Cross-book arbs can be real when both legs are executable, but this is exactly where account limits, stale quotes, and terms risk matter.
   - The current live opportunity JSON includes events that can be stale or already started, so live filters must enforce pre-commence and recent book updates before any execution.

## Profit Path

Priority should be legal prediction-market execution, not trying to route around sportsbook bans.

1. Build the MLB Polymarket 2h signal as a paper-traded watchlist:
   - Buy only if sharp fair probability minus executable Poly/Kalshi ask clears threshold.
   - Require live depth at ask for the full intended stake.
   - Record quoted ask, filled price, depth, timestamp, sharp source, and closing price.

2. Backfill enough Polymarket observations before trading:
   - Required: 90+ calendar days, test_n >= 100, n_qual >= 250.
   - Re-run `scripts/83_polymarket_warehouse_hunt.py --sports all --days 180 --force --collect-only`.
   - Then run `scripts/84_polymarket_edge_ranker.py --days 180` and `scripts/87_data_audit.py`.

3. Fix the data pipeline before expanding:
   - NFL has zero matched Poly observations.
   - Soccer samples are thin and no strict pass survives CI.
   - Live arb/opportunity scanners need hard stale-event rejection.

4. If a signal graduates:
   - Start at micro size, flat staking.
   - Add 0.25 Kelly only after a live paper-trade sample confirms expected CLV and fill quality.
   - Cap per-market exposure and stop trading after a weekly drawdown or after fill slippage erases expected edge.

## Compliance Notes

- Use only venues that are legal and available for the user's jurisdiction.
- Do not use VPNs, false identity, false residency, or routing through prediction markets to evade a sportsbook or exchange restriction.
- CFTC lists `QCX LLC d/b/a Polymarket US` as a designated contract market dated `2025-07-09`: https://www.cftc.gov/IndustryOversight/IndustryFilings/TradingOrganizations
- Polymarket US describes itself as a CFTC-regulated DCM; the international platform is separate and not CFTC regulated: https://www.polymarketexchange.com/ and https://polymarket.com/tos

## Shared-Agent Repo Protocol

- Always start by running `git fetch --prune origin` and checking `git status --short --branch`.
- Prefer `git merge --ff-only origin/main` before analysis.
- If local generated data is dirty, do not overwrite it blindly. Decide whether to preserve, regenerate, or discard based on ownership and file overlap.
- Commit durable insights, validation policy changes, and materially refreshed data. Avoid committing transient API keys, local venvs, or raw cache blobs.
