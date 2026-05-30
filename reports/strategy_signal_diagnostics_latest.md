# Strategy Signal Diagnostics

- Generated: 2026-05-30T22:21:54.057264+00:00
- Model run: 20260530T215450Z
- Strategy decision gate: False
- Recommended action: Do not promote passive maker convergence as the primary strategy until a segment has positive raw fill PnL and the identity-risk features are removed or proven harmless in market-disjoint validation.

## Raw Maker-Fill P&L

- Verdict: FAIL: raw observed maker fills are negative at every audited horizon
- Observed target rows: 1,984,815
- Fill rows: 22,965

| Horizon | Observed rows | Fill rows | Fill rate | Mean P&L/share | Fill ROI | Profitable fills |
|---:|---:|---:|---:|---:|---:|---:|
| 30s | 402,759 | 1,521 | 0.38% | -0.0260 | -5.05% | 6.84% |
| 60s | 399,544 | 2,315 | 0.58% | -0.0273 | -5.36% | 9.50% |
| 120s | 393,968 | 3,427 | 0.87% | -0.0297 | -5.86% | 12.43% |
| 300s | 398,682 | 5,591 | 1.40% | -0.0328 | -6.57% | 15.49% |
| 900s | 389,862 | 10,111 | 2.59% | -0.0374 | -7.57% | 14.92% |

## Held-Out Market Gate

- Usable markets: 109
- Test markets: 18
- Test ratio: 16.51%
- Percentage gate pass: True
- Legacy absolute 100-market gate pass: False

## SHAP Identity Audit

- Available: True
- Verdict: FAIL: top SHAP features include stable context/team-like categories that can encode market identity
- Direct identity features in model: none
- Stable context features in top 10: sport_family, odds_base_outcome

| Rank | Feature | Mean abs SHAP |
|---:|---|---:|
| 1 | sport_family | 0.485030 |
| 2 | bid_size_best | 0.301545 |
| 3 | horizon_sec | 0.238432 |
| 4 | odds_source_minutes_to_commence | 0.176878 |
| 5 | trade_count_300s | 0.144561 |
| 6 | trade_sell_count_300s | 0.097085 |
| 7 | odds_base_outcome | 0.080227 |
| 8 | last_trade_price_delta_mid | 0.040781 |
| 9 | bid_depth_3c | 0.033641 |
| 10 | last_trade_age_sec | 0.032917 |
| 11 | trade_buy_size_300s | 0.031196 |
| 12 | obi_3c_delta_30s | 0.030993 |
| 13 | trade_buy_count_300s | 0.030022 |
| 14 | trade_sell_size_300s | 0.022459 |
| 15 | odds_poly_gap_bid | 0.018604 |
| 16 | entry_spread | 0.014985 |
| 17 | odds_quote_age_sec | 0.014682 |
| 18 | odds_poly_gap_ask | 0.014562 |
| 19 | lag_quote_age_60s | 0.013606 |
| 20 | ask_depth_1c | 0.013324 |

## Next Focus

- Use raw PnL segmentation to find narrower positive buckets before model training.
- Strip or isolate implicit identity categorical features such as sport_family and odds_base_outcome in the next validation run.
- Keep the percentage-based held-out market gate; the old 100-market absolute gate is not valid for a 109-market usable universe.
