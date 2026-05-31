# Telonex Temporal Validation

- Generated: 2026-05-31T18:56:56.565871+00:00
- Feature set: `base_odds`
- Target/PnL/Stake: `maker_trade_fill_positive` / `maker_trade_fill_pnl_per_share` / `entry_bid`
- Odds API features: True / coverage 94.09% / matched markets 1151
- Odds API required: True / dropped rows 106,336
- Labels: 1,693,793 / markets 1151 / tokens 2301
- Row cap: 2000000 / sampled diagnostic: True
- Feature guardrails: 83 selected / all-null 0 / high-missing 0
- Time range: 2025-11-04 00:01:00+00:00 to 2026-05-29 02:09:00+00:00
- Time filter: start_after=None / end_before=None / dropped_rows=0
- Folds requested/run: 4 / 4
- Train mode: expanding
- Window days: train 21.0, calibration 5.0, validation 5.0, test 5.0, step 7.0
- Recent/historical blend requested: weight 0.0 / window days 21.0 / fold recent models 0/4
- Row time-order OK folds: 4 / 4
- Market overlap allowed: true / folds with overlap 0
- Aggregate test trades/markets: 0 / 0
- Aggregate test ROI: n/a (n/a to n/a)
- Positive ROI folds: 0 / 4
- Traded folds: 0 / 4
- Abstained folds: 4 / 4
- Temporal gate: False

Each fold trains only on earlier rows, calibrates on the next time block, selects the trading threshold only on the validation block, and reports once on the later test block. The default train window expands from the first available timestamp. The target/as-of purge prevents label horizons from crossing split boundaries.

This is a temporal leakage audit, not an unseen-market generalization audit. Same-market overlap is reported because a live bot can observe a market earlier and trade it later; use the market-disjoint report for the stricter unseen-market check.

## Folds

| Fold | Train rows | Cal rows | Val rows | Test rows | Test markets | Market overlap | Abstain | Threshold | Test trades | Test ROI | CI | ECE |
|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|---|---:|
| 1 | 2,239 | 76,811 | 226,538 | 270,349 | 0 | 0 | True | 1.000001 | 0 | n/a | n/a | 0.01% |
| 2 | 186,918 | 231,766 | 216,604 | 173,627 | 0 | 0 | True | 1.000001 | 0 | n/a | n/a | 0.01% |
| 3 | 533,596 | 196,556 | 82,502 | 32,730 | 0 | 0 | True | 1.000001 | 0 | n/a | n/a | 0.10% |
| 4 | 808,160 | 11,826 | 32,801 | 37,132 | 0 | 0 | True | 1.000001 | 0 | n/a | n/a | 0.04% |

## Gate Reasons

- sampled row-capped validation is diagnostic only, not capital proof
- aggregate temporal test ROI is not positive
- aggregate temporal ROI CI lower bound is not positive
- aggregate test trades below 100
- aggregate test markets below 40
- no temporal folds selected test trades

## Limitations

- Temporal validation enforces no future rows, but it allows the same market to appear in earlier and later split roles.
- Same-market overlap is realistic for live market-state learning but optimistic for unseen-market generalization.
- Historical CLOB backtest ROI remains a ceiling until authenticated order lifecycle, queue position, fills, and market impact are captured live.
