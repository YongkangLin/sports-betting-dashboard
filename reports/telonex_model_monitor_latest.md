# Telonex Model Monitor

- Generated: 2026-05-31T18:57:12.604245+00:00
- Latest run: `20260531T175018Z` / `base_odds`
- Latest selection score: `convergence_prob_lower`
- Monitor verdict: HOLD: latest research gate failed; latest external validation gate failed; latest test ROI is not positive; latest test CI lower bound is not positive

## Run Ablations

Legacy rows are shown for audit continuity only; the hardened comparable runs are the ones with a concrete feature set.

| Run | Feature set | Recent | Selection | Internal gate | Label gate | External gate | Val ROI | Test ROI | 95% CI | Trades | Markets | ECE | q90 |
|---|---|---:|---|---:|---:|---:|---:|---:|---|---:|---:|---:|---:|
| 20260530T215450Z | base_odds | False | convergence_prob_lower | False | True | False | n/a | n/a | n/a | 0 | 0 | 0.02% | 0.04% |
| 20260531T153530Z | base_odds | False | convergence_prob_lower | False | True | False | n/a | n/a | n/a | 0 | 0 | 0.00% | 0.03% |
| 20260531T175018Z | base_odds | False | convergence_prob_lower | False | True | False | n/a | n/a | n/a | 0 | 0 | 0.00% | 0.00% |

## Label Coverage

| Run | Trade-fill target | Label gate | Reasons |
|---|---:|---:|---|
| 20260530T215450Z | True | True | ok |
| 20260531T153530Z | True | True | ok |
| 20260531T175018Z | True | True | ok |

## External Validation

External validation is run-level attribution against the latest market-disjoint and strict temporal reports. A run can pass its internal holdout gate and still fail this gate if the report is older, the ensemble differs, or either validation gate fails.

| Run | Feature set | Recent weight | External gate | Reasons |
|---|---|---:|---:|---|
| 20260530T215450Z | base_odds | 0.0 | False | market_disjoint validation feature_count mismatch: expected 82, got 83; market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_base_odds_latest.json; temporal validation feature_count mismatch: expected 82, got 83; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_base_odds_latest.json |
| 20260531T153530Z | base_odds | 0.0 | False | market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_base_odds_latest.json; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_base_odds_latest.json |
| 20260531T175018Z | base_odds | 0.0 | False | market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_base_odds_latest.json; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_base_odds_latest.json |

## Odds Feature Validation

| Run | Uses odds | Performance gate | Odds gate | Test odds coverage | Test matched markets |
|---|---:|---:|---:|---:|---:|
| 20260530T215450Z | True | False | True | 29.77% | 5 |
| 20260531T153530Z | True | False | True | 60.43% | 34 |
| 20260531T175018Z | True | False | True | 69.32% | 166 |

## Temporal Buckets

| Bucket | Rows | Markets | ECE | Positive | Avg prob | Trades | ROI |
|---|---:|---:|---:|---:|---:|---:|---:|
| 2026-05-09 00:00:00+00:00 | 18,736 | 2 | 0.01% | 0.00% | 0.01% | 0 | n/a |
| 2026-05-10 00:00:00+00:00 | 21,965 | 9 | 0.03% | 0.00% | 0.03% | 0 | n/a |
| 2026-05-11 00:00:00+00:00 | 11,084 | 2 | 0.01% | 0.00% | 0.01% | 0 | n/a |
| 2026-05-12 00:00:00+00:00 | 1,584 | 2 | 0.01% | 0.00% | 0.01% | 0 | n/a |
| 2026-05-14 00:00:00+00:00 | 11,366 | 2 | 0.01% | 0.00% | 0.01% | 0 | n/a |
| 2026-05-15 00:00:00+00:00 | 14,306 | 4 | 0.04% | 0.08% | 0.05% | 0 | n/a |
| 2026-05-16 00:00:00+00:00 | 11,062 | 6 | 0.01% | 0.00% | 0.01% | 0 | n/a |
| 2026-05-17 00:00:00+00:00 | 63,662 | 15 | 0.06% | 0.14% | 0.08% | 0 | n/a |
| 2026-05-18 00:00:00+00:00 | 8,466 | 3 | 0.00% | 0.00% | 0.00% | 0 | n/a |
| 2026-05-19 00:00:00+00:00 | 24,182 | 9 | 0.09% | 0.23% | 0.28% | 0 | n/a |
| 2026-05-20 00:00:00+00:00 | 49,275 | 9 | 0.04% | 0.10% | 0.07% | 0 | n/a |
| 2026-05-21 00:00:00+00:00 | 57,208 | 10 | 0.02% | 0.06% | 0.04% | 0 | n/a |
| 2026-05-22 00:00:00+00:00 | 88,502 | 22 | 0.05% | 0.25% | 0.22% | 0 | n/a |
| 2026-05-23 00:00:00+00:00 | 63,368 | 17 | 0.07% | 0.39% | 0.33% | 0 | n/a |
| 2026-05-24 00:00:00+00:00 | 134,680 | 32 | 0.01% | 0.02% | 0.02% | 0 | n/a |
| 2026-05-25 00:00:00+00:00 | 121,236 | 32 | 0.01% | 0.04% | 0.05% | 0 | n/a |
| 2026-05-26 00:00:00+00:00 | 127,826 | 36 | 0.02% | 0.06% | 0.07% | 0 | n/a |
| 2026-05-27 00:00:00+00:00 | 150,048 | 38 | 0.00% | 0.01% | 0.00% | 0 | n/a |
| 2026-05-28 00:00:00+00:00 | 304,358 | 55 | 0.01% | 0.02% | 0.02% | 0 | n/a |
| 2026-05-29 00:00:00+00:00 | 290,386 | 42 | 0.01% | 0.03% | 0.03% | 0 | n/a |

## Drift And Risk

- ECE Page-Hinkley alerts: 0 / max score 0.000000
- ROI Page-Hinkley alerts: 0 / max score 0.000000
- Bootstrap bankroll median/p05/p95: None / None / None
- Bootstrap max drawdown median/p95: n/a / n/a
- 50% drawdown rate: n/a
- Correlated time-block p05 bankroll: None with quality shock std None
- Selected-trade avg future-mid move: None / favorable rate n/a

This is a monitoring report, not a model-selection loop. It reads existing run artifacts and applies fixed diagnostics only.
