# Queue / Fill Model

- Generated: 2026-05-30T23:26:08.857882+00:00
- Rows: 2,003
- Sources: {'live_paper_order': 2003}
- Authenticated rows/fills: 0 / 0
- Proxy model gate: True
- Authenticated live-fill gate: False
- AUC gate source: test
- Model version: `queue-fill-d7d4993c015f`

This model estimates passive limit-order fill probability. Current coverage is useful for paper/live simulation, but live capital remains blocked until authenticated Polymarket order lifecycle/fill rows exist.

## Metrics

| Split | Rows | Fill rate | Avg prob | Brier | Baseline Brier | AUC | ECE |
|---|---:|---:|---:|---:|---:|---:|---:|
| train | 1,201 | 39.80% | 42.15% | 0.017275333630547604 | 0.23959633971412947 | 0.9999406818405412 | 2.35% |
| val | 401 | 39.15% | 39.15% | 0.007176904033633472 | 0.2382743457703276 | 0.997141589224183 | 0.00% |
| test | 401 | 40.15% | 38.19% | 0.022436290112927686 | 0.24030922526600973 | 0.9800077639751553 | 1.96% |

## Gate Reasons

- authenticated fill rows below 500
