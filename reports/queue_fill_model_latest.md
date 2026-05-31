# Queue / Fill Model

- Generated: 2026-05-31T00:11:47.118134+00:00
- Rows: 2,139
- Sources: {'live_paper_order': 2139}
- Authenticated rows/fills: 0 / 0
- Proxy model gate: True
- Authenticated live-fill gate: False
- AUC gate source: test
- Model version: `queue-fill-2d928f187a0a`

This model estimates passive limit-order fill probability. Current coverage is useful for paper/live simulation, but live capital remains blocked until authenticated Polymarket order lifecycle/fill rows exist.

## Metrics

| Split | Rows | Fill rate | Avg prob | Brier | Baseline Brier | AUC | ECE |
|---|---:|---:|---:|---:|---:|---:|---:|
| train | 1,283 | 38.50% | 38.77% | 0.0018967588052981586 | 0.23678306580020883 | 0.9999178994576233 | 0.28% |
| val | 428 | 44.16% | 44.16% | 0.010251591494533387 | 0.2497864521957265 | 0.9938345398596444 | 0.00% |
| test | 428 | 33.64% | 31.69% | 0.017018668245573337 | 0.22561158458841013 | 0.9786776212832552 | 1.96% |

## Gate Reasons

- authenticated fill rows below 500
