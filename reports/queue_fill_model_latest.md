# Queue / Fill Model

- Generated: 2026-05-31T00:22:08.318371+00:00
- Rows: 2,171
- Sources: {'live_paper_order': 2171}
- Authenticated rows/fills: 0 / 0
- Proxy model gate: True
- Authenticated live-fill gate: False
- AUC gate source: test
- Model version: `queue-fill-ed2053319fe7`

This model estimates passive limit-order fill probability. Current coverage is useful for paper/live simulation, but live capital remains blocked until authenticated Polymarket order lifecycle/fill rows exist.

## Metrics

| Split | Rows | Fill rate | Avg prob | Brier | Baseline Brier | AUC | ECE |
|---|---:|---:|---:|---:|---:|---:|---:|
| train | 1,302 | 38.79% | 39.54% | 0.004664023872790847 | 0.23742570215738049 | 0.9999900617414313 | 0.76% |
| val | 434 | 44.01% | 44.01% | 0.010939269767778153 | 0.24913874672310826 | 0.9945381681856377 | 0.00% |
| test | 435 | 32.18% | 29.11% | 0.023461371818069746 | 0.22261808547261405 | 0.9641646489104116 | 3.08% |

## Gate Reasons

- authenticated fill rows below 500
