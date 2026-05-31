# Queue / Fill Model

- Generated: 2026-05-31T01:28:23.111320+00:00
- Rows: 2,313
- Sources: {'live_paper_order': 2313}
- Authenticated rows/fills: 0 / 0
- Proxy model gate: True
- Authenticated live-fill gate: False
- AUC gate source: test
- Model version: `queue-fill-6757471d1240`

This model estimates passive limit-order fill probability. Current coverage is useful for paper/live simulation, but live capital remains blocked until authenticated Polymarket order lifecycle/fill rows exist.

## Metrics

| Split | Rows | Fill rate | Avg prob | Brier | Baseline Brier | AUC | ECE |
|---|---:|---:|---:|---:|---:|---:|---:|
| train | 1,387 | 39.22% | 39.82% | 0.003306062525978938 | 0.2383820510674618 | 0.999995638824925 | 0.60% |
| val | 463 | 44.28% | 44.28% | 0.012703439555844947 | 0.2492795272103134 | 0.9901871809415768 | 0.00% |
| test | 463 | 22.03% | 19.15% | 0.027096573926336198 | 0.20132264278053424 | 0.9599967410787029 | 2.88% |

## Gate Reasons

- authenticated fill rows below 500
