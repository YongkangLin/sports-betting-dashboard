# Telonex Convergence Model

- Generated: 2026-05-30T21:54:51.137295+00:00
- Run: `20260530T215450Z`
- Labels: 1,984,815
- Target: `maker_trade_fill_positive` using PnL `maker_trade_fill_pnl_per_share`
- Feature set: `base_odds`
- Odds API features: True / coverage 55.11%
- Odds API test coverage: 29.77% / markets 5
- Model version: `20260530T215450Z-3e90e2b5d8da`
- Random seed: 42
- Independent metric recheck: True
- Recent/historical blend: recent_model=False / recent_weight=0.0 / window_days=21.0
- Saved predictions: test (159,230 rows)
- Markets/tokens: 109 / 217
- Positive target rate: 0.16%
- Feature guardrails: 82 selected / all-null 0 / high-missing 0
- ECE test/calibration: 0.00022721751128733201 / 8.481309009035045e-07
- Conformal 90% interval half-width: 0.000441306266548985
- Regime conformal widths: {'005_015_longshot': 0.0, '00_003': 0.21739130434782608, '015_050': 0.0006374840628984276, '050_075': 0.0006374840628984276, '075_092_favorite': 0.0, '092_097': 0.0, '097_100': 0.6}
- Selection score: `convergence_prob_lower`
- Selected threshold: 1.00000100
- Validation abstained: True
- Research gate: False / performance False / odds feature True / label coverage True
- Label coverage reasons: none
- Live capital gate: False

## Label Coverage

| Split | Rows | Markets | Positive | Target observed | Past trade rows | Fill any | Fill queue | Fill+ | Nonzero PnL |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| train | 1,513,571 | 75 | 2,820 | 1,513,571 | 1,177,192 | 151,169 | 19,156 | 2,820 | 19,156 |
| calibration | 156,332 | 8 | 158 | 156,332 | 125,342 | 15,189 | 2,007 | 158 | 2,007 |
| val | 155,682 | 8 | 50 | 155,682 | 105,648 | 7,957 | 709 | 50 | 709 |
| test | 159,230 | 18 | 97 | 159,230 | 116,762 | 10,075 | 1,093 | 97 | 1,093 |

## Classification

| Split | Rows | Positive | AUC | Brier | Log loss | ECE@10 |
|---|---:|---:|---:|---:|---:|---:|
| train | 1,513,571 | 0.19% | 0.9974002694240309 | 0.00146952839517383 | 0.005680882351394952 | 0.0006487051760455852 |
| calibration | 156,332 | 0.10% | 0.9932146033805527 | 0.0007961723090590271 | 0.0033545386336225886 | 8.481309009035045e-07 |
| val | 155,682 | 0.03% | 0.9984150431787806 | 0.00023665984597732957 | 0.0010413064842660295 | 0.00010397077296296072 |
| test | 159,230 | 0.06% | 0.963893685247139 | 0.0005182182627419229 | 0.002796174657015096 | 0.00022721751128733201 |

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
| train | 003_005 | 1,156 | 23 | 2.85% | 3.95% | 4.39% | 1.54% | 0 | n/a |
| train | 005_015_longshot | 57,516 | 35 | 0.38% | 12.22% | 0.30% | 0.08% | 0 | n/a |
| train | 00_003 | 2,526 | 20 | 3.56% | 1.22% | 3.22% | 0.72% | 0 | n/a |
| train | 015_050 | 688,810 | 75 | 0.11% | 36.97% | 0.11% | 0.03% | 0 | n/a |
| train | 050_075 | 582,369 | 68 | 0.12% | 59.29% | 0.11% | 0.04% | 0 | n/a |
| train | 075_092_favorite | 175,994 | 51 | 0.33% | 82.18% | 0.31% | 0.15% | 0 | n/a |
| train | 092_097 | 2,631 | 27 | 10.72% | 94.53% | 9.72% | 4.11% | 0 | n/a |
| train | 097_100 | 2,569 | 21 | 7.08% | 98.75% | 7.74% | 2.94% | 0 | n/a |
| calibration | 003_005 | 50 | 1 | 2.00% | 3.82% | 7.71% | 5.71% | 0 | n/a |
| calibration | 005_015_longshot | 30,653 | 5 | 0.00% | 7.25% | 0.01% | 0.01% | 0 | n/a |
| calibration | 00_003 | 225 | 1 | 2.67% | 1.32% | 6.19% | 3.52% | 0 | n/a |
| calibration | 015_050 | 46,885 | 7 | 0.10% | 39.53% | 0.09% | 0.02% | 0 | n/a |
| calibration | 050_075 | 37,227 | 7 | 0.14% | 54.47% | 0.16% | 0.02% | 0 | n/a |
| calibration | 075_092_favorite | 18,270 | 6 | 0.08% | 85.19% | 0.04% | 0.05% | 0 | n/a |
| calibration | 092_097 | 22,792 | 3 | 0.03% | 93.62% | 0.02% | 0.01% | 0 | n/a |
| calibration | 097_100 | 230 | 1 | 12.17% | 98.64% | 9.69% | 3.00% | 0 | n/a |
| val | 003_005 | 1,400 | 3 | 0.00% | 3.95% | 0.00% | 0.00% | 0 | n/a |
| val | 005_015_longshot | 12,279 | 5 | 0.00% | 8.11% | 0.01% | 0.01% | 0 | n/a |
| val | 00_003 | 116 | 1 | 0.86% | 0.76% | 4.42% | 3.56% | 0 | n/a |
| val | 015_050 | 64,016 | 6 | 0.01% | 35.78% | 0.02% | 0.01% | 0 | n/a |
| val | 050_075 | 63,794 | 4 | 0.02% | 64.13% | 0.02% | 0.00% | 0 | n/a |
| val | 075_092_favorite | 6,390 | 6 | 0.17% | 89.70% | 0.09% | 0.11% | 0 | n/a |
| val | 092_097 | 7,571 | 3 | 0.03% | 94.09% | 0.02% | 0.01% | 0 | n/a |
| val | 097_100 | 116 | 1 | 17.24% | 99.24% | 8.13% | 10.84% | 0 | n/a |
| test | 003_005 | 2,898 | 2 | 0.00% | 3.85% | 0.12% | 0.12% | 0 | n/a |
| test | 005_015_longshot | 1,799 | 5 | 0.11% | 12.93% | 0.29% | 0.20% | 0 | n/a |
| test | 00_003 | 151 | 1 | 5.96% | 1.59% | 3.92% | 5.39% | 0 | n/a |
| test | 015_050 | 73,849 | 17 | 0.01% | 32.96% | 0.02% | 0.01% | 0 | n/a |
| test | 050_075 | 53,284 | 17 | 0.03% | 60.73% | 0.02% | 0.01% | 0 | n/a |
| test | 075_092_favorite | 24,015 | 10 | 0.10% | 81.04% | 0.07% | 0.06% | 0 | n/a |
| test | 092_097 | 3,083 | 2 | 0.94% | 96.01% | 0.36% | 0.60% | 0 | n/a |
| test | 097_100 | 151 | 1 | 6.62% | 98.41% | 6.74% | 3.58% | 0 | n/a |

## Audit Artifacts

- Reliability plot: `/Users/yongkanglin/Documents/Codex/2026-05-28/i-have-this-repo-git-github-3/Sports-Betting-ml/data/processed/telonex_convergence_ml/20260530T215450Z/calibration_reliability.png`
- Calibration bins: `/Users/yongkanglin/Documents/Codex/2026-05-28/i-have-this-repo-git-github-3/Sports-Betting-ml/data/processed/telonex_convergence_ml/20260530T215450Z/calibration_bins.csv`
- Raw audit rows: `/Users/yongkanglin/Documents/Codex/2026-05-28/i-have-this-repo-git-github-3/Sports-Betting-ml/data/processed/telonex_convergence_ml/20260530T215450Z/audit_sample_rows.csv`
- Label SHA256: `32537f0d3b561eb1f7a39bcb5ed6ad4834d6f854a4443683da29c657d09f223b`
- Model SHA256: `3e90e2b5d8da5a95009453c5545ecb5b076312796b17796da159a22954e03649`

## Validation Threshold Grid

| Threshold | Trades | ROI | CI low | Win rate | Avg prob |
|---:|---:|---:|---:|---:|---:|
| 0.00205310 | 895 | -1.53% | -1.99% | 3.46% | 3.00% |
| 0.00000000 | 155,682 | -0.03% | -0.04% | 0.03% | 0.02% |
| 1.00000100 | 0 | n/a | n/a | n/a | n/a |

This model is trained on historical public CLOB convergence labels. The reported ROI is a ceiling, not a live estimate. It is not production proof because authenticated order lifecycle, queue position, complementary Yes/No book state, and market-impact/fill logs are still missing. Threshold selection uses validation only; the test split remains an audit readout, not a tuning surface.
