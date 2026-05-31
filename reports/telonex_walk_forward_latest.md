# Telonex Market-Disjoint Validation

- Generated: 2026-05-31T15:41:08.811979+00:00
- Feature set: `base`
- Target/PnL/Stake: `maker_positive` / `maker_pnl_per_share` / `entry_bid`
- Odds API features: False / coverage n/a / matched markets 0
- Labels: 5,768,529 / markets 725 / tokens 1436
- Feature guardrails: 64 selected / all-null 0 / high-missing 0
- Folds requested/run: 4 / 4
- Fold market windows: train 80, calibration 20, validation 20, test 20
- Market ordering key: end
- Recent/historical blend requested: weight 0.0 / window days 21.0 / fold recent models 0/4
- Market-purged splits: true
- Row time-order enforced: False
- Adjacent timestamp purge: False / gap hours 1.0
- Aggregate test trades/markets: 577 / 9
- Aggregate test ROI: 3.79% (2.77% to 4.79%)
- Positive ROI folds: 1 / 4
- Traded folds: 1 / 4
- Abstained folds: 3 / 4
- Market-disjoint gate: False

Each fold retrains the model from scratch, calibrates on a later market block, selects the trading threshold only on the validation block, and reports once on the next test block. Markets do not overlap across split roles.
Row timestamps may overlap across split roles because live sports markets overlap in calendar time. This validates unseen-market generalization, not strict temporal causality; use the temporal validation report for the no-future-row audit.

## Folds

| Fold | Train rows | Cal rows | Val rows | Test rows | Test markets | Abstain | Threshold | Test trades | Test ROI | CI | ECE |
|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|---|---:|
| 1 | 245,002 | 90,542 | 101,559 | 101,524 | 0 | True | 1.000001 | 0 | n/a | n/a | 0.08% |
| 2 | 1,266,537 | 66,951 | 119,582 | 185,652 | 0 | True | 1.000001 | 0 | n/a | n/a | 1.45% |
| 3 | 2,989,593 | 139,004 | 162,308 | 166,553 | 0 | True | 1.000001 | 0 | n/a | n/a | 0.35% |
| 4 | 4,819,113 | 304,034 | 305,474 | 339,908 | 9 | False | 0.376535 | 577 | 3.79% | 2.78% to 4.88% | 0.50% |

## Gate Reasons

- aggregate test markets below 40
