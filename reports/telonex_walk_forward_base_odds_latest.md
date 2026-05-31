# Telonex Market-Disjoint Validation

- Generated: 2026-05-31T18:54:37.727559+00:00
- Feature set: `base_odds`
- Target/PnL/Stake: `maker_trade_fill_positive` / `maker_trade_fill_pnl_per_share` / `entry_bid`
- Odds API features: True / coverage 94.09% / matched markets 1151
- Labels: 1,800,129 / markets 1183 / tokens 2365
- Row cap: 2000000 / sampled diagnostic: True
- Feature guardrails: 83 selected / all-null 0 / high-missing 0
- Folds requested/run: 4 / 4
- Fold market windows: train 80, calibration 20, validation 20, test 20
- Market ordering key: end
- Recent/historical blend requested: weight 0.0 / window days 21.0 / fold recent models 0/4
- Market-purged splits: true
- Row time-order enforced: False
- Adjacent timestamp purge: False / gap hours 1.0
- Aggregate test trades/markets: 0 / 0
- Aggregate test ROI: n/a (n/a to n/a)
- Positive ROI folds: 0 / 4
- Traded folds: 0 / 4
- Abstained folds: 4 / 4
- Market-disjoint gate: False

Each fold retrains the model from scratch, calibrates on a later market block, selects the trading threshold only on the validation block, and reports once on the next test block. Markets do not overlap across split roles.
Row timestamps may overlap across split roles because live sports markets overlap in calendar time. This validates unseen-market generalization, not strict temporal causality; use the temporal validation report for the no-future-row audit.

## Folds

| Fold | Train rows | Cal rows | Val rows | Test rows | Test markets | Abstain | Threshold | Test trades | Test ROI | CI | ECE |
|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|---|---:|
| 1 | 86,288 | 30,631 | 37,222 | 33,396 | 0 | True | 1.000001 | 0 | n/a | n/a | 0.01% |
| 2 | 755,006 | 30,657 | 33,349 | 38,037 | 0 | True | 1.000001 | 0 | n/a | n/a | 0.01% |
| 3 | 1,095,080 | 6,350 | 9,345 | 23,732 | 0 | True | 1.000001 | 0 | n/a | n/a | 0.00% |
| 4 | 1,718,788 | 31,146 | 28,863 | 21,332 | 0 | True | 1.000001 | 0 | n/a | n/a | 0.00% |

## Gate Reasons

- sampled row-capped validation is diagnostic only, not capital proof
- aggregate market-disjoint test ROI is not positive
- aggregate market-disjoint ROI CI lower bound is not positive
- aggregate test trades below 100
- aggregate test markets below 40
- no folds selected test trades
