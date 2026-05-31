# Telonex Convergence Model

- Generated: 2026-05-31T15:35:34.040898+00:00
- Run: `20260531T153530Z`
- Labels: 3,886,357
- Target: `maker_trade_fill_positive` using PnL `maker_trade_fill_pnl_per_share`
- Feature set: `base_odds`
- Odds API features: True / coverage 71.07%
- Odds API test coverage: 60.43% / markets 34
- Model version: `20260531T153530Z-aeeeb0172cb0`
- Random seed: 42
- Independent metric recheck: True
- Recent/historical blend: recent_model=False / recent_weight=0.0 / window_days=21.0
- Saved predictions: test (1,091,540 rows)
- Markets/tokens: 411 / 809
- Positive target rate: 0.12%
- Feature guardrails: 83 selected / all-null 0 / high-missing 0
- ECE test/calibration: 2.0366123575247333e-05 / 7.47709569844729e-07
- Conformal 90% interval half-width: 0.00030048076923076925
- Regime conformal widths: {'003_005': 0.17269076305220887, '005_015_longshot': 3.6845983787767136e-05, '00_003': 0.27380952380952384, '015_050': 0.000704390702042733, '050_075': 0.00030048076923076925, '075_092_favorite': 0.00010369141435089174, '092_097': 0.2317596566523605, '097_100': 0.6720430107526882}
- Selection score: `convergence_prob_lower`
- Selected threshold: 1.00000100
- Validation abstained: True
- Research gate: False / performance False / odds feature True / label coverage True
- Label coverage reasons: none
- Live capital gate: False

## Label Coverage

| Split | Rows | Markets | Positive | Target observed | Past trade rows | Fill any | Fill queue | Fill+ | Nonzero PnL |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| train | 2,090,788 | 287 | 2,794 | 2,090,788 | 1,904,142 | 725,080 | 40,554 | 2,794 | 40,554 |
| calibration | 249,189 | 30 | 471 | 249,189 | 231,736 | 46,706 | 4,091 | 471 | 4,091 |
| val | 454,840 | 32 | 828 | 454,840 | 357,052 | 60,832 | 6,797 | 828 | 6,797 |
| test | 1,091,540 | 62 | 574 | 1,091,540 | 830,090 | 62,370 | 6,275 | 574 | 6,275 |

## Classification

| Split | Rows | Positive | AUC | Brier | Log loss | ECE@10 |
|---|---:|---:|---:|---:|---:|---:|
| train | 2,090,788 | 0.13% | 0.9979199676699005 | 0.0010156689038544897 | 0.003590357339506174 | 0.00040915026014339646 |
| calibration | 249,189 | 0.19% | 0.993665917978135 | 0.0015380153881131235 | 0.005820927151921865 | 7.47709569844729e-07 |
| val | 454,840 | 0.18% | 0.9954542423935592 | 0.001475238420354677 | 0.005354401269480681 | 0.00015263868125124156 |
| test | 1,091,540 | 0.05% | 0.9937336206678988 | 0.00044075828431711496 | 0.0018080186049063075 | 2.0366123575247333e-05 |

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
| train | 003_005 | 897 | 26 | 5.35% | 3.92% | 6.12% | 2.64% | 0 | n/a |
| train | 005_015_longshot | 482,144 | 172 | 0.06% | 11.93% | 0.07% | 0.01% | 0 | n/a |
| train | 00_003 | 2,440 | 21 | 1.80% | 1.04% | 2.70% | 0.90% | 0 | n/a |
| train | 015_050 | 553,777 | 176 | 0.13% | 36.25% | 0.19% | 0.06% | 0 | n/a |
| train | 050_075 | 465,920 | 117 | 0.13% | 59.94% | 0.16% | 0.04% | 0 | n/a |
| train | 075_092_favorite | 570,919 | 210 | 0.13% | 86.75% | 0.14% | 0.04% | 0 | n/a |
| train | 092_097 | 12,239 | 40 | 1.72% | 93.50% | 2.00% | 0.55% | 0 | n/a |
| train | 097_100 | 2,452 | 21 | 5.59% | 98.95% | 6.29% | 1.31% | 0 | n/a |
| calibration | 003_005 | 379 | 5 | 3.17% | 4.00% | 4.84% | 1.67% | 0 | n/a |
| calibration | 005_015_longshot | 84,208 | 26 | 0.03% | 12.99% | 0.04% | 0.01% | 0 | n/a |
| calibration | 00_003 | 392 | 4 | 7.65% | 1.64% | 5.61% | 2.20% | 0 | n/a |
| calibration | 015_050 | 40,375 | 19 | 0.16% | 32.90% | 0.26% | 0.11% | 0 | n/a |
| calibration | 050_075 | 24,599 | 11 | 0.38% | 58.67% | 0.32% | 0.08% | 0 | n/a |
| calibration | 075_092_favorite | 97,483 | 26 | 0.15% | 86.35% | 0.10% | 0.05% | 0 | n/a |
| calibration | 092_097 | 1,361 | 8 | 4.11% | 93.71% | 4.46% | 0.84% | 0 | n/a |
| calibration | 097_100 | 392 | 4 | 10.97% | 98.36% | 12.68% | 2.70% | 0 | n/a |
| val | 003_005 | 460 | 9 | 2.61% | 3.96% | 3.80% | 1.42% | 0 | n/a |
| val | 005_015_longshot | 25,473 | 18 | 0.15% | 11.47% | 0.20% | 0.05% | 0 | n/a |
| val | 00_003 | 801 | 5 | 4.37% | 1.41% | 2.64% | 1.89% | 0 | n/a |
| val | 015_050 | 198,874 | 28 | 0.11% | 40.08% | 0.12% | 0.02% | 0 | n/a |
| val | 050_075 | 179,502 | 27 | 0.13% | 57.12% | 0.11% | 0.02% | 0 | n/a |
| val | 075_092_favorite | 47,979 | 22 | 0.23% | 84.48% | 0.23% | 0.03% | 0 | n/a |
| val | 092_097 | 915 | 11 | 11.69% | 94.62% | 7.16% | 4.80% | 0 | n/a |
| val | 097_100 | 836 | 6 | 8.25% | 98.52% | 6.42% | 3.07% | 0 | n/a |
| test | 003_005 | 4,497 | 12 | 0.02% | 3.89% | 0.34% | 0.32% | 0 | n/a |
| test | 005_015_longshot | 125,622 | 30 | 0.03% | 10.61% | 0.04% | 0.01% | 0 | n/a |
| test | 00_003 | 738 | 8 | 2.44% | 1.27% | 4.22% | 2.29% | 0 | n/a |
| test | 015_050 | 413,775 | 52 | 0.03% | 31.77% | 0.04% | 0.01% | 0 | n/a |
| test | 050_075 | 288,284 | 41 | 0.04% | 62.81% | 0.05% | 0.01% | 0 | n/a |
| test | 075_092_favorite | 224,199 | 44 | 0.07% | 83.47% | 0.05% | 0.03% | 0 | n/a |
| test | 092_097 | 33,825 | 13 | 0.17% | 93.95% | 0.10% | 0.06% | 0 | n/a |
| test | 097_100 | 600 | 7 | 10.00% | 98.69% | 8.42% | 2.83% | 0 | n/a |

## Audit Artifacts

- Reliability plot: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/telonex_convergence_ml/20260531T153530Z/calibration_reliability.png`
- Calibration bins: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/telonex_convergence_ml/20260531T153530Z/calibration_bins.csv`
- Raw audit rows: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/telonex_convergence_ml/20260531T153530Z/audit_sample_rows.csv`
- Label SHA256: `8cdfb7cda52ff8ab59d31872381cd6a64e65df78ed427febd3caff5f3a59ee39`
- Model SHA256: `aeeeb0172cb0b7193974a6c9931e1accfb2904b252881397f0b265bd2f5a3ed3`

## Validation Threshold Grid

| Threshold | Trades | ROI | CI low | Win rate | Avg prob |
|---:|---:|---:|---:|---:|---:|
| 0.11112809 | 2,346 | -4.33% | -5.01% | 20.03% | 18.94% |
| 0.01899212 | 4,700 | -3.64% | -4.03% | 12.81% | 11.90% |
| 0.00111132 | 11,491 | -2.00% | -2.18% | 5.53% | 5.16% |
| 0.00000000 | 454,840 | -0.09% | -0.09% | 0.18% | 0.13% |
| 1.00000100 | 0 | n/a | n/a | n/a | n/a |

This model is trained on historical public CLOB convergence labels. The reported ROI is a ceiling, not a live estimate. It is not production proof because authenticated order lifecycle, queue position, complementary Yes/No book state, and market-impact/fill logs are still missing. Threshold selection uses validation only; the test split remains an audit readout, not a tuning surface.
