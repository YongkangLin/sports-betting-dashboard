# Profit Playbook - 2026-05-28 Live Pass

This file answers: "how do we generate profit?" using the current repo data and live scans.

## Short Answer

The only strategy that is executable today is strict, low-frequency cross-book arbitrage, provided both books are legally available to the trader and both legs can be placed before the price moves.

Prediction-market-only execution is the preferred long-term route, but there is no live prediction-market trade right now after adding realistic guards for time-to-start and ask depth.

## Live Scan Result

Scan time: `2026-05-28T17:03:39Z`.
Scanner: `scripts/74_continuous_arb_scanner.py --once --us-only --min-edge 0.03` after hardening stale-event checks.

Current executable candidates in `data/processed/execute_now.json`:

| ROI | Market | Leg A | Leg B | Start |
| ---: | --- | --- | --- | --- |
| 4.455% | boxing h2h | Lourdes Juarez +280 at DraftKings | Yokasta Valle -227 at Pinnacle | 2026-05-31 00:30 UTC |
| 1.397% | boxing h2h | Kevin Lerena -137 at Pinnacle | Ryad Merhy +145 at BetUS | 2026-05-30 18:00 UTC |
| 1.051% | tennis h2h | Quentin Halys +1160 at FanDuel | Alexander Zverev -1014 at GTBets | 2026-05-29 18:15 UTC |
| 0.976% | boxing h2h | Arturo Cardenas -125 at BetUS | Jordan Martinez +130 at Bally Bet | 2026-06-13 21:00 UTC |
| 0.678% | AFL h2h | Western Bulldogs -170 at BetUS | Collingwood Magpies +175 at DraftKings | 2026-05-30 09:35 UTC |

These are not guaranteed to be fillable. Before placing anything, re-run the scanner and manually confirm both legs on the books. If either leg moves, recompute the stake split or skip. Pinnacle appears in several current arbs; use it only if it is legally available to the trader.

## Prediction-Market Status

Live Polymarket-vs-sharp scans found no trade after costs:

- MLB: 6 matched games, 12 sides scanned. Closest raw edge was Chicago White Sox at +0.528 percentage points, below executable threshold after costs and not selected by the 2h/depth scanner.
- NBA: one matched game, no edge.
- NHL: one matched game, no edge.
- Boxing/MMA: no reliable Polymarket/Odds API event matches.

Current action for prediction markets: run the MLB 2h scanner in paper mode and wait. Do not deploy live capital until `VALIDATION.md` gates pass.

The latest CLOB depth report (`data/processed/poly_history_depth_report.json`) says the 90-day validation gate cannot be backfilled from current Polymarket `/prices-history` retention. That means the profitable prediction-market route has to grow forward via daily collection, or use a different historical price source.

## Execution Rules That Make This Profitable Instead Of Noisy

1. Never bet stale events. The scanner now rejects started/near-lock events and rejects missing timestamps.
2. For arbs, place the harder leg first, then immediately place the hedge leg.
3. Use small fixed stakes until the scanner log proves fills. Suggested initial size: $100 total per arb, not Kelly.
4. Skip any arb under 0.5% unless both books are already open and the stake is trivial.
5. Skip any market where either book is not legally available to the trader.
6. For prediction markets, use executable ask only, require top-of-book depth, and target the validated MLB 2h window.
7. Track every attempted trade: quoted price, filled price, timestamp, book, stake, and whether either leg failed.

## What To Run

```bash
# Find current arbitrage candidates and write execute_now.html/json
ODDS_API_KEY=... .venv/bin/python scripts/74_continuous_arb_scanner.py --once --us-only --min-edge 0.03

# Generate the phone-friendly execution sheet from the latest scan
.venv/bin/python scripts/78_execution_sheet.py

# Check one-sided +EV candidates; treat as lower confidence than arbs
ODDS_API_KEY=... .venv/bin/python scripts/81_live_onesided_picks.py --min-edge 0.03

# Prediction-market-only watchlist; paper mode only until validation gates pass
ODDS_API_KEY=... .venv/bin/python scripts/85_live_mlb_poly_scanner.py --min-edge 0.005 --paper
```

Do not write API keys into `.env` unless the file remains local and uncommitted. The Odds API quota cache now stores only a non-secret key id and last four characters.
