# Queue / Fill Model

- Generated: 2026-05-31T00:33:19.208600+00:00
- Rows: 2,195
- Sources: {'live_paper_order': 2195}
- Authenticated rows/fills: 0 / 0
- Proxy model gate: True
- Authenticated live-fill gate: False
- AUC gate source: test
- Model version: `queue-fill-6cc7b3c72129`

This model estimates passive limit-order fill probability. Current coverage is useful for paper/live simulation, but live capital remains blocked until authenticated Polymarket order lifecycle/fill rows exist.

## Metrics

| Split | Rows | Fill rate | Avg prob | Brier | Baseline Brier | AUC | ECE |
|---|---:|---:|---:|---:|---:|---:|---:|
| train | 1,317 | 38.65% | 39.14% | 0.004415911679590656 | 0.23711421634844612 | 1.0 | 0.49% |
| val | 439 | 45.10% | 45.10% | 0.010709910248594221 | 0.2517669469221194 | 0.9944570183159395 | 0.00% |
| test | 439 | 29.38% | 26.34% | 0.02329444887064845 | 0.21608323834858562 | 0.9612403100775193 | 3.05% |

## Gate Reasons

- authenticated fill rows below 500
