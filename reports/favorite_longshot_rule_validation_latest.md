# Favorite-Longshot Rule Validation

- Generated: 2026-05-31T00:05:39.771511+00:00
- Verdict: HOLD: favorite-longshot rule not yet proven out of sample
- Overall gate: False
- Gate reasons: temporal selected rule failed, market-disjoint selected rule failed
- Input rows: 259 settled / 259 markets
- Candidate rules: 15

## Selected Rules

| Validation | Rule | Val bets | Val ROI | Val CI low | Test bets | Test ROI | Test CI low | Gate |
|---|---|---:|---:|---:|---:|---:|---:|---|
| temporal | nba_only | 38 | 7.79% | -1.55% | 7 | 13.10% | 11.50% | False |
| market_disjoint | exclude_last_15m | 73 | 1.45% | -7.75% | 58 | 2.38% | -7.55% | False |

## Candidate Test Summary

| Validation | Rule | Test bets | Test ROI | Test CI low | Test win rate |
|---|---|---:|---:|---:|---:|
| temporal | all_settled | 65 | -1.80% | -10.58% | 86.15% |
| temporal | exclude_last_15m | 65 | -1.80% | -10.58% | 86.15% |
| temporal | entry_15m_to_24h | 65 | -1.80% | -10.58% | 86.15% |
| temporal | exclude_last_1h | 63 | -2.22% | -11.56% | 85.71% |
| temporal | entry_1h_to_24h | 63 | -2.22% | -11.56% | 85.71% |
| temporal | spread_1c_or_better | 58 | -3.82% | -13.47% | 84.48% |
| temporal | spread_1c_15m_to_24h | 58 | -3.82% | -13.47% | 84.48% |
| temporal | ask_85_89 | 58 | -3.38% | -15.44% | 84.48% |
| temporal | entry_12h_to_24h | 55 | -0.46% | -10.96% | 87.27% |
| temporal | soccer_only | 54 | -2.91% | -13.60% | 85.19% |
| temporal | longshot_no_token | 54 | -2.91% | -13.60% | 85.19% |
| temporal | soccer_12h_to_24h | 51 | -1.65% | -11.84% | 86.27% |
| market_disjoint | all_settled | 59 | 0.62% | -9.13% | 88.14% |
| market_disjoint | exclude_last_15m | 58 | 2.38% | -7.55% | 89.66% |
| market_disjoint | entry_15m_to_24h | 55 | 1.64% | -8.83% | 89.09% |
| market_disjoint | exclude_last_1h | 54 | 3.66% | -5.14% | 90.74% |
| market_disjoint | ask_85_89 | 53 | -0.52% | -11.54% | 86.79% |
| market_disjoint | entry_1h_to_24h | 51 | 2.93% | -6.50% | 90.20% |
| market_disjoint | spread_1c_or_better | 51 | -1.63% | -14.96% | 86.27% |
| market_disjoint | spread_1c_15m_to_24h | 50 | 0.38% | -11.05% | 88.00% |
| market_disjoint | entry_12h_to_24h | 44 | 3.85% | -7.97% | 90.91% |
| market_disjoint | soccer_only | 37 | -1.14% | -13.86% | 86.49% |
| market_disjoint | longshot_no_token | 37 | -1.14% | -13.86% | 86.49% |
| market_disjoint | soccer_12h_to_24h | 35 | 1.33% | -11.59% | 88.57% |

## Interpretation

- This validator does not tune on the final test slice.
- A rule only clears if validation and test both have enough markets, positive ROI, and positive cluster-bootstrap CI lower bound.
- Failure here means the favorite-longshot bucket remains a research lead, not a deployable trading rule.
