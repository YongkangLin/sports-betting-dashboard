# Telonex Model Monitor

- Generated: 2026-05-31T15:35:53.023038+00:00
- Latest run: `20260531T153530Z` / `base_odds`
- Latest selection score: `convergence_prob_lower`
- Monitor verdict: HOLD: latest research gate failed; latest external validation gate failed; latest test ROI is not positive; latest test CI lower bound is not positive

## Run Ablations

Legacy rows are shown for audit continuity only; the hardened comparable runs are the ones with a concrete feature set.

| Run | Feature set | Recent | Selection | Internal gate | Label gate | External gate | Val ROI | Test ROI | 95% CI | Trades | Markets | ECE | q90 |
|---|---|---:|---|---:|---:|---:|---:|---:|---|---:|---:|---:|---:|
| 20260530T215450Z | base_odds | False | convergence_prob_lower | False | True | False | n/a | n/a | n/a | 0 | 0 | 0.02% | 0.04% |
| 20260531T153530Z | base_odds | False | convergence_prob_lower | False | True | False | n/a | n/a | n/a | 0 | 0 | 0.00% | 0.03% |

## Label Coverage

| Run | Trade-fill target | Label gate | Reasons |
|---|---:|---:|---|
| 20260530T215450Z | True | True | ok |
| 20260531T153530Z | True | True | ok |

## External Validation

External validation is run-level attribution against the latest market-disjoint and strict temporal reports. A run can pass its internal holdout gate and still fail this gate if the report is older, the ensemble differs, or either validation gate fails.

| Run | Feature set | Recent weight | External gate | Reasons |
|---|---|---:|---:|---|
| 20260530T215450Z | base_odds | 0.0 | False | market_disjoint validation feature_count mismatch: expected 82, got 83; market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_base_odds_latest.json; temporal validation feature_count mismatch: expected 82, got 83; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_base_odds_latest.json |
| 20260531T153530Z | base_odds | 0.0 | False | market_disjoint validation report is older than the model artifact: telonex_walk_forward_base_odds_latest.json; market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_base_odds_latest.json; temporal validation report is older than the model artifact: telonex_temporal_validation_base_odds_latest.json; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_base_odds_latest.json |

## Odds Feature Validation

| Run | Uses odds | Performance gate | Odds gate | Test odds coverage | Test matched markets |
|---|---:|---:|---:|---:|---:|
| 20260530T215450Z | True | False | True | 29.77% | 5 |
| 20260531T153530Z | True | False | True | 60.43% | 34 |

## Temporal Buckets

| Bucket | Rows | Markets | ECE | Positive | Avg prob | Trades | ROI |
|---|---:|---:|---:|---:|---:|---:|---:|
| 2026-05-17 00:00:00+00:00 | 24,386 | 5 | 0.21% | 0.30% | 0.09% | 0 | n/a |
| 2026-05-18 00:00:00+00:00 | 166 | 2 | 0.01% | 0.00% | 0.01% | 0 | n/a |
| 2026-05-19 00:00:00+00:00 | 1,242 | 4 | 1.07% | 0.40% | 1.48% | 0 | n/a |
| 2026-05-20 00:00:00+00:00 | 20,802 | 4 | 0.00% | 0.00% | 0.00% | 0 | n/a |
| 2026-05-21 00:00:00+00:00 | 15,520 | 4 | 0.01% | 0.02% | 0.02% | 0 | n/a |
| 2026-05-22 00:00:00+00:00 | 52,826 | 9 | 0.01% | 0.01% | 0.01% | 0 | n/a |
| 2026-05-23 00:00:00+00:00 | 30,320 | 8 | 0.15% | 0.72% | 0.57% | 0 | n/a |
| 2026-05-24 00:00:00+00:00 | 107,692 | 22 | 0.01% | 0.02% | 0.02% | 0 | n/a |
| 2026-05-25 00:00:00+00:00 | 110,130 | 24 | 0.01% | 0.04% | 0.05% | 0 | n/a |
| 2026-05-26 00:00:00+00:00 | 116,166 | 28 | 0.03% | 0.06% | 0.08% | 0 | n/a |
| 2026-05-27 00:00:00+00:00 | 127,946 | 30 | 0.00% | 0.00% | 0.01% | 0 | n/a |
| 2026-05-28 00:00:00+00:00 | 250,834 | 43 | 0.01% | 0.02% | 0.02% | 0 | n/a |
| 2026-05-29 00:00:00+00:00 | 233,510 | 32 | 0.01% | 0.04% | 0.04% | 0 | n/a |

## Drift And Risk

- ECE Page-Hinkley alerts: 0 / max score 0.007536
- ROI Page-Hinkley alerts: 0 / max score 0.000000
- Bootstrap bankroll median/p05/p95: None / None / None
- Bootstrap max drawdown median/p95: n/a / n/a
- 50% drawdown rate: n/a
- Correlated time-block p05 bankroll: None with quality shock std None
- Selected-trade avg future-mid move: None / favorable rate n/a

This is a monitoring report, not a model-selection loop. It reads existing run artifacts and applies fixed diagnostics only.
