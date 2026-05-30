# Queue / Fill Model

- Generated: 2026-05-30T23:55:25.508525+00:00
- Rows: 2,095
- Sources: {'live_paper_order': 2095}
- Authenticated rows/fills: 0 / 0
- Proxy model gate: True
- Authenticated live-fill gate: False
- AUC gate source: test
- Model version: `queue-fill-554575e69a45`

This model estimates passive limit-order fill probability. Current coverage is useful for paper/live simulation, but live capital remains blocked until authenticated Polymarket order lifecycle/fill rows exist.

## Metrics

| Split | Rows | Fill rate | Avg prob | Brier | Baseline Brier | AUC | ECE |
|---|---:|---:|---:|---:|---:|---:|---:|
| train | 1,257 | 38.42% | 39.77% | 0.00982326012196866 | 0.23660152311732105 | 0.999989300292637 | 1.35% |
| val | 419 | 44.87% | 44.87% | 0.011592226389913739 | 0.2515194149042213 | 0.9909390255134936 | 0.00% |
| test | 419 | 36.04% | 33.90% | 0.016852704794177244 | 0.23107637801106168 | 0.978377977661362 | 2.14% |

## Gate Reasons

- authenticated fill rows below 500
