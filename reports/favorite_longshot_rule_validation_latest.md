# Favorite-Longshot Rule Validation

- Generated: 2026-05-31T11:18:00.053695+00:00
- Verdict: HOLD: favorite-longshot rule not yet proven out of sample
- Overall gate: False
- Gate reasons: temporal selected rule failed, market-disjoint selected rule failed
- Input rows: 277 settled / 277 markets
- Candidate rules: 15

## Selected Rules

| Validation | Rule | Val bets | Val ROI | Val CI low | Test bets | Test ROI | Test CI low | Gate |
|---|---|---:|---:|---:|---:|---:|---:|---|
| temporal | nba_only | 39 | 7.47% | -1.67% | 6 | 13.49% | 11.62% | False |
| market_disjoint | entry_15m_to_24h | 76 | 0.39% | -7.23% | 57 | 1.99% | -6.16% | False |

## Data Quality Split

| Validation | Quality tier | Test bets | Test markets | Test ROI | Test CI low | Test win rate |
|---|---|---:|---:|---:|---:|---:|
| temporal | complete_5m | 5 | 5 | 13.78% | 11.54% | 100.00% |
| temporal | complete_5m_source_quote_gap | 1 | 1 | 12.03% | n/a | 100.00% |
| market_disjoint | complete_5m | 30 | 30 | 2.37% | -9.37% | 90.00% |
| market_disjoint | complete_15m_partial_5m | 27 | 27 | 1.57% | -15.29% | 88.89% |

## Candidate Test Summary

| Validation | Rule | Test bets | Test ROI | Test CI low | Test win rate |
|---|---|---:|---:|---:|---:|
| temporal | all_settled | 70 | -0.85% | -10.89% | 87.14% |
| temporal | exclude_last_15m | 70 | -0.85% | -10.89% | 87.14% |
| temporal | entry_15m_to_24h | 68 | -1.18% | -11.44% | 86.76% |
| temporal | exclude_last_1h | 67 | -1.42% | -11.61% | 86.57% |
| temporal | entry_1h_to_24h | 65 | -1.79% | -12.18% | 86.15% |
| temporal | ask_85_89 | 61 | -0.60% | -10.17% | 86.89% |
| temporal | spread_1c_or_better | 60 | -1.28% | -12.91% | 86.67% |
| temporal | spread_1c_15m_to_24h | 60 | -1.28% | -12.91% | 86.67% |
| temporal | soccer_only | 60 | -1.46% | -12.19% | 86.67% |
| temporal | entry_12h_to_24h | 58 | -1.86% | -13.65% | 86.21% |
| temporal | soccer_12h_to_24h | 54 | -3.09% | -16.00% | 85.19% |
| temporal | nba_only | 6 | 13.49% | 11.62% | 100.00% |
| market_disjoint | all_settled | 61 | 0.98% | -8.54% | 88.52% |
| market_disjoint | exclude_last_15m | 60 | 2.69% | -6.62% | 90.00% |
| market_disjoint | entry_15m_to_24h | 57 | 1.99% | -6.16% | 89.47% |
| market_disjoint | exclude_last_1h | 56 | 3.95% | -4.33% | 91.07% |
| market_disjoint | ask_85_89 | 54 | -0.28% | -12.97% | 87.04% |
| market_disjoint | entry_1h_to_24h | 53 | 3.26% | -5.53% | 90.57% |
| market_disjoint | spread_1c_or_better | 53 | -1.12% | -13.08% | 86.79% |
| market_disjoint | spread_1c_15m_to_24h | 52 | 0.81% | -10.01% | 88.46% |
| market_disjoint | entry_12h_to_24h | 46 | 4.18% | -6.14% | 91.30% |
| market_disjoint | soccer_only | 39 | -0.48% | -15.08% | 87.18% |
| market_disjoint | soccer_12h_to_24h | 37 | 1.89% | -10.56% | 89.19% |
| market_disjoint | nba_only | 19 | 1.95% | -16.39% | 89.47% |

## Interpretation

- This validator does not tune on the final test slice.
- A rule only clears if validation and test both have enough markets, positive ROI, and positive cluster-bootstrap CI lower bound.
- Failure here means the favorite-longshot bucket remains a research lead, not a deployable trading rule.
