# Telonex Convergence Model

- Generated: 2026-05-31T17:50:25.591522+00:00
- Run: `20260531T175018Z`
- Labels: 7,662,289
- Target: `maker_trade_fill_positive` using PnL `maker_trade_fill_pnl_per_share`
- Feature set: `base_odds`
- Odds API features: True / coverage 81.96%
- Odds API test coverage: 69.32% / markets 166
- Model version: `20260531T175018Z-34bbf56d9ff0`
- Random seed: 42
- Independent metric recheck: True
- Recent/historical blend: recent_model=False / recent_weight=0.0 / window_days=21.0
- Saved predictions: test (1,890,652 rows)
- Markets/tokens: 1387 / 2761
- Positive target rate: 0.07%
- Feature guardrails: 83 selected / all-null 0 / high-missing 0
- ECE test/calibration: 2.5137615878781096e-05 / 9.321276706837497e-07
- Conformal 90% interval half-width: 0.0
- Regime conformal widths: {'003_005': 0.20847457627118643, '005_015_longshot': 0.0, '00_003': 0.10538116591928251, '015_050': 0.0, '050_075': 0.0, '075_092_favorite': 0.0, '092_097': 0.08037825059101655, '097_100': 0.2838283828382838}
- Selection score: `convergence_prob_lower`
- Selected threshold: 1.00000100
- Validation abstained: True
- Research gate: False / performance False / odds feature True / label coverage True
- Label coverage reasons: none
- Live capital gate: False

## Label Coverage

| Split | Rows | Markets | Positive | Target observed | Past trade rows | Fill any | Fill queue | Fill+ | Nonzero PnL |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| train | 4,191,448 | 970 | 2,820 | 4,191,448 | 4,007,348 | 1,404,937 | 109,780 | 2,820 | 109,780 |
| calibration | 785,239 | 104 | 894 | 785,239 | 672,667 | 231,215 | 12,061 | 894 | 12,061 |
| val | 794,950 | 104 | 785 | 794,950 | 744,982 | 259,139 | 14,836 | 785 | 14,836 |
| test | 1,890,652 | 209 | 988 | 1,890,652 | 1,495,155 | 198,121 | 15,691 | 988 | 15,691 |

## Classification

| Split | Rows | Positive | AUC | Brier | Log loss | ECE@10 |
|---|---:|---:|---:|---:|---:|---:|
| train | 4,191,448 | 0.07% | 0.9976076774326151 | 0.0005543124530682194 | 0.0021886514163021406 | 6.345968172129126e-05 |
| calibration | 785,239 | 0.11% | 0.9972093851432171 | 0.0009235809957993334 | 0.0033477903149496243 | 9.321276706837497e-07 |
| val | 794,950 | 0.10% | 0.9887676272250215 | 0.0008353071320689043 | 0.0035639955948946647 | 0.00013627015726267315 |
| test | 1,890,652 | 0.05% | 0.9922973965266424 | 0.00043694818713818986 | 0.0017627181564530729 | 2.5137615878781096e-05 |

## Trading Threshold

| Split | Trades | Markets | ROI | 95% CI | PnL/share sum | Win rate | Avg prob |
|---|---:|---:|---:|---|---:|---:|---:|
| train | 0 | 0 | n/a | n/a | 0.0000 | n/a | n/a |
| val | 0 | 0 | n/a | n/a | 0.0000 | n/a | n/a |
| test | 0 | 0 | n/a | n/a | 0.0000 | n/a | n/a |

## Entry Price Regimes

These buckets audit favourite-longshot and tail calibration behavior using the entry CLOB midpoint.

| Split | Price regime | Rows | Markets | Positive | Avg mid | Avg prob | ECE | Trades | ROI |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|
| train | 003_005 | 3,549 | 26 | 0.96% | 4.27% | 1.10% | 0.24% | 0 | n/a |
| train | 005_015_longshot | 333,750 | 187 | 0.08% | 11.35% | 0.07% | 0.01% | 0 | n/a |
| train | 00_003 | 2,190 | 23 | 1.64% | 1.30% | 2.10% | 0.53% | 0 | n/a |
| train | 015_050 | 1,748,568 | 857 | 0.05% | 34.51% | 0.05% | 0.00% | 0 | n/a |
| train | 050_075 | 1,413,060 | 705 | 0.05% | 62.07% | 0.05% | 0.00% | 0 | n/a |
| train | 075_092_favorite | 655,848 | 390 | 0.10% | 83.40% | 0.09% | 0.02% | 0 | n/a |
| train | 092_097 | 32,284 | 43 | 0.57% | 93.73% | 0.54% | 0.10% | 0 | n/a |
| train | 097_100 | 2,199 | 23 | 5.50% | 98.69% | 5.40% | 0.56% | 0 | n/a |
| calibration | 003_005 | 563 | 7 | 4.80% | 3.94% | 5.01% | 1.63% | 0 | n/a |
| calibration | 005_015_longshot | 117,682 | 44 | 0.06% | 12.01% | 0.08% | 0.02% | 0 | n/a |
| calibration | 00_003 | 1,090 | 7 | 3.30% | 1.13% | 2.52% | 0.79% | 0 | n/a |
| calibration | 015_050 | 271,433 | 79 | 0.06% | 38.99% | 0.08% | 0.02% | 0 | n/a |
| calibration | 050_075 | 256,234 | 65 | 0.08% | 59.33% | 0.06% | 0.02% | 0 | n/a |
| calibration | 075_092_favorite | 132,386 | 51 | 0.19% | 86.90% | 0.17% | 0.03% | 0 | n/a |
| calibration | 092_097 | 4,758 | 21 | 1.85% | 93.57% | 2.28% | 0.53% | 0 | n/a |
| calibration | 097_100 | 1,093 | 7 | 5.12% | 98.87% | 5.34% | 0.78% | 0 | n/a |
| val | 003_005 | 545 | 10 | 2.39% | 3.99% | 3.48% | 1.10% | 0 | n/a |
| val | 005_015_longshot | 88,569 | 35 | 0.05% | 12.34% | 0.07% | 0.02% | 0 | n/a |
| val | 00_003 | 871 | 5 | 4.25% | 1.40% | 2.64% | 1.84% | 0 | n/a |
| val | 015_050 | 305,902 | 84 | 0.05% | 40.94% | 0.05% | 0.01% | 0 | n/a |
| val | 050_075 | 282,961 | 74 | 0.06% | 56.82% | 0.05% | 0.00% | 0 | n/a |
| val | 075_092_favorite | 113,234 | 39 | 0.16% | 86.32% | 0.11% | 0.06% | 0 | n/a |
| val | 092_097 | 1,964 | 14 | 5.70% | 94.59% | 4.28% | 1.83% | 0 | n/a |
| val | 097_100 | 904 | 6 | 7.85% | 98.54% | 7.19% | 2.33% | 0 | n/a |
| test | 003_005 | 4,464 | 16 | 0.02% | 3.89% | 0.28% | 0.26% | 0 | n/a |
| test | 005_015_longshot | 279,924 | 80 | 0.02% | 11.69% | 0.03% | 0.01% | 0 | n/a |
| test | 00_003 | 593 | 8 | 3.04% | 1.28% | 4.64% | 1.77% | 0 | n/a |
| test | 015_050 | 657,930 | 168 | 0.04% | 33.26% | 0.04% | 0.01% | 0 | n/a |
| test | 050_075 | 479,795 | 139 | 0.05% | 61.51% | 0.05% | 0.00% | 0 | n/a |
| test | 075_092_favorite | 432,019 | 115 | 0.05% | 84.53% | 0.05% | 0.01% | 0 | n/a |
| test | 092_097 | 34,936 | 28 | 0.25% | 93.93% | 0.20% | 0.05% | 0 | n/a |
| test | 097_100 | 991 | 11 | 8.88% | 98.81% | 6.95% | 2.18% | 0 | n/a |

## Audit Artifacts

- Reliability plot: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/telonex_convergence_ml/20260531T175018Z/calibration_reliability.png`
- Calibration bins: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/telonex_convergence_ml/20260531T175018Z/calibration_bins.csv`
- Raw audit rows: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/telonex_convergence_ml/20260531T175018Z/audit_sample_rows.csv`
- Label SHA256: `1233ef779055fd65b8ccb205cac07cdc089d439cda2d7b232126663560183ec6`
- Model SHA256: `34bbf56d9ff04ac3c328cdc52d6a652d29c249690da1100b542ec8e34eeb5b82`

## Validation Threshold Grid

| Threshold | Trades | ROI | CI low | Win rate | Avg prob |
|---:|---:|---:|---:|---:|---:|
| 0.02439024 | 4,045 | -3.27% | -3.66% | 12.90% | 12.11% |
| 0.00555967 | 9,678 | -2.16% | -2.34% | 6.21% | 5.51% |
| 0.00078370 | 20,200 | -1.41% | -1.50% | 3.13% | 2.74% |
| 0.00010286 | 43,772 | -0.86% | -0.90% | 1.50% | 1.27% |
| 0.00000000 | 794,950 | -0.09% | -0.09% | 0.10% | 0.07% |
| 1.00000100 | 0 | n/a | n/a | n/a | n/a |

This model is trained on historical public CLOB convergence labels. The reported ROI is a ceiling, not a live estimate. It is not production proof because authenticated order lifecycle, queue position, complementary Yes/No book state, and market-impact/fill logs are still missing. Threshold selection uses validation only; the test split remains an audit readout, not a tuning surface.
