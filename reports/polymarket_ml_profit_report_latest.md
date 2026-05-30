# Polymarket ML Profit Report - 20260529T212018Z

## Verdict

**LIVE CAPITAL: HOLD**

The model is promising only if its test CI lower bound is positive and the sample clears the live-capital gate. Otherwise this remains a paper-trading/research model.

## Data

- Clean rows: 94,098 from 5,041 events.
- Date span: 2025-06-07T13:20:00+00:00 to 2026-05-29T02:10:00+00:00.
- Dropped rows during cleaning: 77,362.
- Legacy spread rows quarantined: 28,008.
- Inconsistent outcome rows quarantined: 204 from 102 groups.
- Side/event label mismatch rows quarantined: 361.
- Event identity collision rows quarantined: 608 from 11 event ids.
- Exposure rule: one bet per `event`.
- Threshold selection objective: `roi_positive_ci`.
- Recommended strategy: `hybrid_min`.
- Point-in-time feature coverage: 97.08%.
- Guarded PIT fair rows used for `sharp_fair`: 91,352; raw observation `sharp_fair` is not trusted when PIT features are enabled.
- Source-clock guard dropped rows with no safe PIT fair: 2,746.
- Market-residual shrinkage lambda selected on validation log loss: 0.50.
- Post-hoc probability calibration: `isotonic` selected on validation log loss/ECE.

## Test Performance

| Strategy | Val threshold | Test bets | Test events | Test ROI | Event bootstrap 95% CI | Test P&L |
| --- | ---: | ---: | ---: | ---: | --- | ---: |
| Sharp EV baseline | 0.4400 | 14 | 14 | 202.01% | 21.73% to 449.56% | $2,828.18 |
| ML model | 0.8500 | 31 | 31 | 87.92% | -43.67% to 255.56% | $2,725.48 |
| Market-anchored residual ML | 0.1000 | 364 | 364 | 2.93% | -16.61% to 24.08% | $1,065.18 |
| Hybrid min(ML, sharp) | 0.0600 | 315 | 315 | -4.45% | -24.98% to 17.98% | $-1,403.00 |
| Hybrid geometric EV | 0.1000 | 355 | 355 | 2.67% | -17.67% to 24.38% | $947.86 |

## Classification Metrics

| Split | AUC | Brier | Log loss | ECE-10 |
| --- | ---: | ---: | ---: | ---: |
| train | 0.7062 | 0.2164 | 0.6200 | 0.0335 |
| val | 0.6414 | 0.2313 | 0.6532 | 0.0000 |
| test | 0.6366 | 0.2331 | 0.6592 | 0.0150 |

## Prediction-Market Diagnostics

The primary benchmark is Polymarket price, not a soft-book line. Sportsbook closing-line diagnostics are retained only as a secondary sanity check.

- Average calibrated edge vs Polymarket price: `n/a`.
- Average quarter-Kelly fraction, capped at 2% bankroll/outcome: `1.56%`.
- Bias-zone share (longshot/favorite price regimes): `19.37%`.
- Extreme-price share below 3c or above 97c: `0.00%`.
- Selected price regimes: `balanced=154, favorite_bias_zone=1, high_mid=6, longshot_bias_zone=60, low_mid=94`.

### Calibration By Polymarket Price Regime

| Price regime | Rows | Market price | Calibrated prob | Observed win | Abs calibration gap |
| --- | ---: | ---: | ---: | ---: | ---: |
| balanced | 12,827 | 49.71% | 49.83% | 49.68% | 0.15% |
| favorite_bias_zone | 419 | 80.01% | 79.67% | 75.18% | 4.49% |
| high_mid | 625 | 69.32% | 68.81% | 66.08% | 2.73% |
| longshot_bias_zone | 334 | 12.00% | 17.58% | 14.37% | 3.21% |
| low_mid | 3,809 | 25.69% | 25.34% | 26.91% | 1.57% |


## Recommended Test Bets By Segment

| Sport / league | Market | Bets | Events | ROI | Win rate |
| --- | --- | ---: | ---: | ---: | ---: |
| MLB | Moneyline | 59 | 59 | 17.36% | 40.68% |
| MLB | Total | 35 | 35 | -5.19% | 40.00% |
| French Open Tennis | Moneyline | 32 | 32 | -78.61% | 9.38% |
| Copa Libertadores | 3-way moneyline | 31 | 31 | -7.31% | 12.90% |
| Brazil Serie A | 3-way moneyline | 26 | 26 | -13.42% | 34.62% |
| Spanish La Liga | 3-way moneyline | 21 | 21 | -66.48% | 14.29% |
| Italian Serie A | 3-way moneyline | 21 | 21 | 39.78% | 33.33% |
| French Ligue 1 | 3-way moneyline | 17 | 17 | 20.32% | 17.65% |
| German Bundesliga | 3-way moneyline | 15 | 15 | 30.19% | 33.33% |
| WNBA | Moneyline | 15 | 15 | 44.88% | 26.67% |
| English Premier League | 3-way moneyline | 14 | 14 | -14.90% | 14.29% |
| Italian Serie B | 3-way moneyline | 9 | 9 | 3.85% | 22.22% |

## Gates

- Research gate: `False`.
- Live-capital gate: `False`.
- Selected source-clock violations: `0`.
- Required live gate: test bets >= 100 and qualified bets >= 250 and test CI lower > 0 and selected source-clock violations = 0.

## Files

- Summary JSON: `data/processed/polymarket_ml/20260529T212018Z/summary.json`
- Predictions parquet: `data/processed/polymarket_ml/20260529T212018Z/predictions.parquet`
- Selected test bets parquet: `data/processed/polymarket_ml/20260529T212018Z/selected_test_bets.parquet`
- Model artifact: `data/processed/polymarket_ml/20260529T212018Z/model.joblib`
