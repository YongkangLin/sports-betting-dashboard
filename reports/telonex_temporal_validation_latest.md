# Telonex Temporal Validation

- Generated: 2026-05-30T21:21:26.253602+00:00
- Feature set: `base`
- Target/PnL/Stake: `maker_trade_fill_positive` / `maker_trade_fill_pnl_per_share` / `entry_bid`
- Odds API features: False / coverage n/a / matched markets 0
- Labels: 2,219,371 / markets 179 / tokens 357
- Feature guardrails: 64 selected / all-null 0 / high-missing 0
- Time range: 2026-05-15 00:01:00+00:00 to 2026-05-29 23:59:00+00:00
- Time filter: start_after=2026-05-15 00:00:00+00:00 / end_before=None / dropped_rows=669214
- Folds requested/run: 1 / 1
- Train mode: expanding
- Window days: train 5.0, calibration 2.0, validation 2.0, test 2.0, step 3.0
- Recent/historical blend requested: weight 0.0 / window days 21.0 / fold recent models 0/1
- Row time-order OK folds: 1 / 1
- Market overlap allowed: true / folds with overlap 1
- Aggregate test trades/markets: 0 / 0
- Aggregate test ROI: n/a (n/a to n/a)
- Positive ROI folds: 0 / 1
- Traded folds: 0 / 1
- Abstained folds: 1 / 1
- Temporal gate: False

Each fold trains only on earlier rows, calibrates on the next time block, selects the trading threshold only on the validation block, and reports once on the later test block. The default train window expands from the first available timestamp. The target/as-of purge prevents label horizons from crossing split boundaries.

This is a temporal leakage audit, not an unseen-market generalization audit. Same-market overlap is reported because a live bot can observe a market earlier and trade it later; use the market-disjoint report for the stricter unseen-market check.

## Folds

| Fold | Train rows | Cal rows | Val rows | Test rows | Test markets | Market overlap | Abstain | Threshold | Test trades | Test ROI | CI | ECE |
|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|---|---:|
| 1 | 209,172 | 110,152 | 130,283 | 226,720 | 0 | 63 | True | 1.000001 | 0 | n/a | n/a | 0.02% |

## Gate Reasons

- aggregate temporal test ROI is not positive
- aggregate temporal ROI CI lower bound is not positive
- aggregate test trades below 100
- aggregate test markets below 10
- no temporal folds selected test trades

## Limitations

- Temporal validation enforces no future rows, but it allows the same market to appear in earlier and later split roles.
- Same-market overlap is realistic for live market-state learning but optimistic for unseen-market generalization.
- Historical CLOB backtest ROI remains a ceiling until authenticated order lifecycle, queue position, fills, and market impact are captured live.
