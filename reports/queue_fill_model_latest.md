# Queue / Fill Model

- Generated: 2026-05-31T01:14:43.529706+00:00
- Rows: 2,287
- Sources: {'live_paper_order': 2287}
- Authenticated rows/fills: 0 / 0
- Proxy model gate: True
- Authenticated live-fill gate: False
- AUC gate source: test
- Model version: `queue-fill-30700f567b4b`

This model estimates passive limit-order fill probability. Current coverage is useful for paper/live simulation, but live capital remains blocked until authenticated Polymarket order lifecycle/fill rows exist.

## Metrics

| Split | Rows | Fill rate | Avg prob | Brier | Baseline Brier | AUC | ECE |
|---|---:|---:|---:|---:|---:|---:|---:|
| train | 1,372 | 39.07% | 39.93% | 0.004361218511609284 | 0.23804707222330831 | 0.9998694476183675 | 0.87% |
| val | 457 | 44.42% | 44.42% | 0.012599145583622686 | 0.24975204867544193 | 0.9909235483495599 | 0.00% |
| test | 458 | 22.27% | 21.27% | 0.0187706279330861 | 0.20132044022146997 | 0.9637309980171843 | 2.02% |

## Gate Reasons

- authenticated fill rows below 500
