# Queue / Fill Model

- Generated: 2026-05-31T00:05:54.140076+00:00
- Rows: 2,127
- Sources: {'live_paper_order': 2127}
- Authenticated rows/fills: 0 / 0
- Proxy model gate: True
- Authenticated live-fill gate: False
- AUC gate source: test
- Model version: `queue-fill-ccdbbbd6af6d`

This model estimates passive limit-order fill probability. Current coverage is useful for paper/live simulation, but live capital remains blocked until authenticated Polymarket order lifecycle/fill rows exist.

## Metrics

| Split | Rows | Fill rate | Avg prob | Brier | Baseline Brier | AUC | ECE |
|---|---:|---:|---:|---:|---:|---:|---:|
| train | 1,276 | 38.71% | 38.72% | 0.0014832008721676112 | 0.2372642760979157 | 0.9999301075825506 | 0.01% |
| val | 425 | 44.00% | 44.00% | 0.009143313200035056 | 0.24919340415286803 | 0.9939109333573001 | 0.00% |
| test | 426 | 34.27% | 32.17% | 0.018774609620253714 | 0.22723746790844224 | 0.9755381604696673 | 2.10% |

## Gate Reasons

- authenticated fill rows below 500
