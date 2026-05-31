# Telonex Model Monitor

- Generated: 2026-05-31T01:14:45.187604+00:00
- Latest run: `20260530T215450Z` / `base_odds`
- Latest selection score: `convergence_prob_lower`
- Monitor verdict: HOLD: latest research gate failed; latest external validation gate failed; latest test ROI is not positive; latest test CI lower bound is not positive

## Run Ablations

Legacy rows are shown for audit continuity only; the hardened comparable runs are the ones with a concrete feature set.

| Run | Feature set | Recent | Selection | Internal gate | Label gate | External gate | Val ROI | Test ROI | 95% CI | Trades | Markets | ECE | q90 |
|---|---|---:|---|---:|---:|---:|---:|---:|---|---:|---:|---:|---:|
| 20260530T215450Z | base_odds | False | convergence_prob_lower | False | True | False | n/a | n/a | n/a | 0 | 0 | 0.02% | 0.04% |

## Label Coverage

| Run | Trade-fill target | Label gate | Reasons |
|---|---:|---:|---|
| 20260530T215450Z | True | True | ok |

## External Validation

External validation is run-level attribution against the latest market-disjoint and strict temporal reports. A run can pass its internal holdout gate and still fail this gate if the report is older, the ensemble differs, or either validation gate fails.

| Run | Feature set | Recent weight | External gate | Reasons |
|---|---|---:|---:|---|
| 20260530T215450Z | base_odds | 0.0 | False | market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_base_odds_latest.json; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_base_odds_latest.json |

## Odds Feature Validation

| Run | Uses odds | Performance gate | Odds gate | Test odds coverage | Test matched markets |
|---|---:|---:|---:|---:|---:|
| 20260530T215450Z | True | False | True | 29.77% | 5 |

## Temporal Buckets

| Bucket | Rows | Markets | ECE | Positive | Avg prob | Trades | ROI |
|---|---:|---:|---:|---:|---:|---:|---:|
| 2026-05-22 00:00:00+00:00 | 646 | 2 | 0.01% | 0.00% | 0.01% | 0 | n/a |
| 2026-05-23 00:00:00+00:00 | 3,964 | 1 | 0.09% | 0.10% | 0.01% | 0 | n/a |
| 2026-05-24 00:00:00+00:00 | 88 | 2 | 0.00% | 0.00% | 0.00% | 0 | n/a |
| 2026-05-25 00:00:00+00:00 | 1,908 | 7 | 0.01% | 0.00% | 0.01% | 0 | n/a |
| 2026-05-26 00:00:00+00:00 | 8,736 | 6 | 0.02% | 0.00% | 0.02% | 0 | n/a |
| 2026-05-27 00:00:00+00:00 | 17,642 | 8 | 0.01% | 0.01% | 0.01% | 0 | n/a |
| 2026-05-28 00:00:00+00:00 | 74,552 | 16 | 0.00% | 0.01% | 0.01% | 0 | n/a |
| 2026-05-29 00:00:00+00:00 | 51,694 | 11 | 0.06% | 0.16% | 0.12% | 0 | n/a |

## Drift And Risk

- ECE Page-Hinkley alerts: 0 / max score 0.000000
- ROI Page-Hinkley alerts: 0 / max score 0.000000
- Bootstrap bankroll median/p05/p95: None / None / None
- Bootstrap max drawdown median/p95: n/a / n/a
- 50% drawdown rate: n/a
- Correlated time-block p05 bankroll: None with quality shock std None
- Selected-trade avg future-mid move: None / favorable rate n/a

This is a monitoring report, not a model-selection loop. It reads existing run artifacts and applies fixed diagnostics only.
