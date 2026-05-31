# Telonex Taker Strategy Validation

- Generated: 2026-05-31T19:14:34.455691+00:00
- Rows/markets/tokens: 5,392,062 / 1,257 / 2,513
- Splits: `{'train': 3123944, 'val': 925902, 'test': 810914, 'unobserved': 531302}`
- Odds feature coverage: 94.54%
- Selection protocol: validation selects rule; frozen selected rule is reported once on test
- Gate: False
- Gate reasons: favorite_longshot_fade_v2: no validation rule cleared positive cluster-bootstrap CI lower bound, sharp_consensus_clob_mispricing: no validation rule cleared positive cluster-bootstrap CI lower bound, line_lag_clv_capture: no validation rule cleared positive cluster-bootstrap CI lower bound

A strategy here is tradable only if validation picked the rule and the same frozen rule passed test. Test results are not used to choose thresholds, horizon, sport, or market type.

## Strategy Results

| Strategy | Selected | Gate | Val ROI | Val CI | Val rows/markets | Test ROI | Test CI | Test rows/markets | Rule | Reason |
|---|---|---|---:|---|---:|---:|---|---:|---|---|
| favorite_longshot_fade_v2 | no | fail | n/a | n/a | 0/0 | n/a | n/a | 0/0 | `none` | no validation rule cleared positive cluster-bootstrap CI lower bound |
| sharp_consensus_clob_mispricing | no | fail | n/a | n/a | 0/0 | n/a | n/a | 0/0 | `none` | no validation rule cleared positive cluster-bootstrap CI lower bound |
| line_lag_clv_capture | no | fail | n/a | n/a | 0/0 | n/a | n/a | 0/0 | `none` | no validation rule cleared positive cluster-bootstrap CI lower bound |

## Top Validation Candidates

| Strategy | Rule | ROI | CI | Rows | Markets | Positive |
|---|---|---:|---|---:|---:|---:|
| favorite_longshot_fade_v2 | `h60|spr0.03|dep5.0|min_ask=0.85|seg=sport_market:basketball_nba|h2h_or_binary` | -1.69% | -1.84% to -1.53% | 1,221 | 15 | 0.00% |
| favorite_longshot_fade_v2 | `h60|spr0.05|dep5.0|min_ask=0.85|seg=sport:basketball_nba` | -1.69% | -1.85% to -1.54% | 1,221 | 15 | 0.00% |
| favorite_longshot_fade_v2 | `h120|spr0.03|dep5.0|min_ask=0.85|seg=sport_market:basketball_nba|h2h_or_binary` | -1.69% | -1.85% to -1.52% | 1,208 | 15 | 0.00% |
| favorite_longshot_fade_v2 | `h60|spr0.05|dep5.0|min_ask=0.85|seg=sport_market:basketball_nba|h2h_or_binary` | -1.69% | -1.86% to -1.53% | 1,221 | 15 | 0.00% |
| favorite_longshot_fade_v2 | `h60|spr0.03|dep5.0|min_ask=0.85|seg=sport:basketball_nba` | -1.69% | -1.86% to -1.53% | 1,221 | 15 | 0.00% |
| sharp_consensus_clob_mispricing | `h900|spr0.03|dep5.0|edge_threshold=0.02|min_books=3|min_sharp_books=0|seg=all:all` | -7.01% | -11.66% to -5.71% | 1,991 | 18 | 1.31% |
| sharp_consensus_clob_mispricing | `h900|spr0.05|dep5.0|edge_threshold=0.02|min_books=3|min_sharp_books=0|seg=all:all` | -7.01% | -11.75% to -5.69% | 1,991 | 18 | 1.31% |
| sharp_consensus_clob_mispricing | `h900|spr0.05|dep5.0|edge_threshold=0.02|min_books=5|min_sharp_books=1|seg=all:all` | -9.57% | -11.85% to -7.66% | 1,407 | 17 | 1.21% |
| sharp_consensus_clob_mispricing | `h300|spr0.03|dep5.0|edge_threshold=0.02|min_books=3|min_sharp_books=0|seg=all:all` | -7.13% | -11.87% to -5.57% | 2,081 | 24 | 0.58% |
| sharp_consensus_clob_mispricing | `h900|spr0.05|dep5.0|edge_threshold=0.02|min_books=3|min_sharp_books=1|seg=all:all` | -9.57% | -11.99% to -7.67% | 1,407 | 17 | 1.21% |
| line_lag_clv_capture | `h900|spr0.03|dep5.0|min_books=3|window_min=5|fair_delta_threshold=0.02|lag_gap_threshold=0.01|poly_gap_threshold=0.0|seg=all:all` | -7.17% | n/a | 3 | 1 | 0.00% |
| line_lag_clv_capture | `h900|spr0.03|dep5.0|min_books=3|window_min=5|fair_delta_threshold=0.02|lag_gap_threshold=0.01|poly_gap_threshold=0.0|seg=sport:basketball_wnba` | -7.17% | n/a | 3 | 1 | 0.00% |
| line_lag_clv_capture | `h900|spr0.03|dep5.0|min_books=3|window_min=5|fair_delta_threshold=0.02|lag_gap_threshold=0.01|poly_gap_threshold=0.0|seg=sport_market:basketball_wnba|h2h_or_binary` | -7.17% | n/a | 3 | 1 | 0.00% |
| line_lag_clv_capture | `h900|spr0.05|dep5.0|min_books=3|window_min=5|fair_delta_threshold=0.02|lag_gap_threshold=0.01|poly_gap_threshold=0.0|seg=all:all` | -7.17% | n/a | 3 | 1 | 0.00% |
| line_lag_clv_capture | `h900|spr0.05|dep5.0|min_books=3|window_min=5|fair_delta_threshold=0.02|lag_gap_threshold=0.01|poly_gap_threshold=0.0|seg=sport:basketball_wnba` | -7.17% | n/a | 3 | 1 | 0.00% |

## Verdict

No validation-selected taker strategy passed the held-out test gate. Do not route capital from these rules; use this to prune/redirect strategy research.
