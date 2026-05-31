# Queue / Fill Model

- Generated: 2026-05-31T00:50:02.552494+00:00
- Rows: 2,231
- Sources: {'live_paper_order': 2231}
- Authenticated rows/fills: 0 / 0
- Proxy model gate: True
- Authenticated live-fill gate: False
- AUC gate source: test
- Model version: `queue-fill-1239d631ebd8`

This model estimates passive limit-order fill probability. Current coverage is useful for paper/live simulation, but live capital remains blocked until authenticated Polymarket order lifecycle/fill rows exist.

## Metrics

| Split | Rows | Fill rate | Avg prob | Brier | Baseline Brier | AUC | ECE |
|---|---:|---:|---:|---:|---:|---:|---:|
| train | 1,338 | 38.71% | 38.78% | 0.002179107522077797 | 0.23726374728807914 | 0.9999858743761183 | 0.07% |
| val | 446 | 45.52% | 45.52% | 0.010682908455426061 | 0.252614727377944 | 0.9939183847229824 | 0.00% |
| test | 447 | 25.73% | 22.80% | 0.022775815936313136 | 0.20794981731634224 | 0.9565217391304348 | 2.93% |

## Gate Reasons

- authenticated fill rows below 500
