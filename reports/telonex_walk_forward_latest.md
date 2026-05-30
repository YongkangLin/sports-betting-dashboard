# Telonex Market-Disjoint Validation

- Generated: 2026-05-30T21:19:15.517273+00:00
- Feature set: `base`
- Target/PnL/Stake: `maker_trade_fill_positive` / `maker_trade_fill_pnl_per_share` / `entry_bid`
- Odds API features: False / coverage n/a / matched markets 0
- Labels: 2,888,585 / markets 216 / tokens 429
- Feature guardrails: 64 selected / all-null 0 / high-missing 0
- Folds requested/run: 2 / 2
- Fold market windows: train 80, calibration 20, validation 20, test 20
- Market ordering key: end
- Recent/historical blend requested: weight 0.0 / window days 21.0 / fold recent models 0/2
- Market-purged splits: true
- Row time-order enforced: False
- Adjacent timestamp purge: False / gap hours 1.0
- Aggregate test trades/markets: 0 / 0
- Aggregate test ROI: n/a (n/a to n/a)
- Positive ROI folds: 0 / 2
- Traded folds: 0 / 2
- Abstained folds: 2 / 2
- Market-disjoint gate: False

Each fold retrains the model from scratch, calibrates on a later market block, selects the trading threshold only on the validation block, and reports once on the next test block. Markets do not overlap across split roles.
Row timestamps may overlap across split roles because live sports markets overlap in calendar time. This validates unseen-market generalization, not strict temporal causality; use the temporal validation report for the no-future-row audit.

## Folds

| Fold | Train rows | Cal rows | Val rows | Test rows | Test markets | Abstain | Threshold | Test trades | Test ROI | CI | ECE |
|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|---|---:|
| 1 | 1,423,681 | 23,730 | 133,768 | 130,688 | 0 | True | 1.000001 | 0 | n/a | n/a | 0.13% |
| 2 | 1,926,185 | 380,136 | 232,578 | 349,686 | 0 | True | 1.000001 | 0 | n/a | n/a | 0.00% |

## Gate Reasons

- aggregate market-disjoint test ROI is not positive
- aggregate market-disjoint ROI CI lower bound is not positive
- aggregate test trades below 100
- aggregate test markets below 10
- no folds selected test trades
