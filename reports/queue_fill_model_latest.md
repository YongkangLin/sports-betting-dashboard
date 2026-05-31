# Queue / Fill Model

- Generated: 2026-05-30T19:41:16.457447+00:00
- Rows: 1,125
- Sources: {'live_paper_order': 1125}
- Authenticated rows/fills: 0 / 0
- Proxy model gate: True
- Authenticated live-fill gate: False
- AUC gate source: test
- Model version: `queue-fill-51670823ad59`

This model estimates passive limit-order fill probability. Current coverage is useful for paper/live simulation, but live capital remains blocked until authenticated Polymarket order lifecycle/fill rows exist.

## Metrics

| Split | Rows | Fill rate | Avg prob | Brier | Baseline Brier | AUC | ECE |
|---|---:|---:|---:|---:|---:|---:|---:|
| train | 675 | 62.52% | 62.24% | 0.0016148118528385184 | 0.23432866941015087 | 0.9988151658767772 | 0.28% |
| val | 225 | 6.22% | 6.22% | 0.004000000000955555 | 0.37527791495198903 | 0.9984766418415707 | 0.00% |
| test | 225 | 16.89% | 18.87% | 0.08262604307761175 | 0.3485717421124828 | 0.898747537292429 | 8.42% |

## Gate Reasons

- authenticated fill rows below 500
