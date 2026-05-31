# Telonex Model Monitor

- Generated: 2026-05-30T22:00:42.330141+00:00
- Latest run: `20260530T215450Z` / `base_odds`
- Latest selection score: `convergence_prob_lower`
- Monitor verdict: HOLD: latest research gate failed; latest external validation gate failed; latest test ROI is not positive; latest test CI lower bound is not positive

## Run Ablations

Legacy rows are shown for audit continuity only; the hardened comparable runs are the ones with a concrete feature set.

| Run | Feature set | Recent | Selection | Internal gate | Label gate | External gate | Val ROI | Test ROI | 95% CI | Trades | Markets | ECE | q90 |
|---|---|---:|---|---:|---:|---:|---:|---:|---|---:|---:|---:|---:|
| 20260530T163238Z | base_odds | False | convergence_prob_lower | True | True | False | 10.69% | 12.10% | 9.85% to 14.50% | 689 | 30 | 0.59% | 5.87% |
| 20260530T193847Z | base_odds | False | convergence_prob_lower | False | True | False | n/a | n/a | n/a | 0 | 0 | 0.01% | 0.00% |
| 20260530T195425Z | base | False | convergence_prob_lower | False | True | False | n/a | n/a | n/a | 0 | 0 | 0.00% | 0.05% |
| 20260530T204923Z | base | False | convergence_prob_lower | False | True | False | n/a | n/a | n/a | 0 | 0 | 0.09% | 0.15% |
| 20260530T211425Z | base | False | convergence_prob_lower | False | False | False | n/a | n/a | n/a | 0 | 0 | 0.09% | 0.15% |
| 20260530T213938Z | base | False | convergence_prob_lower | False | False | False | n/a | n/a | n/a | 0 | 0 | 0.01% | 0.00% |
| 20260530T214959Z | base | False | convergence_prob_lower | False | False | False | n/a | n/a | n/a | 0 | 0 | 0.02% | 0.07% |
| 20260530T215220Z | base | False | convergence_prob_lower | False | True | False | n/a | n/a | n/a | 0 | 0 | 0.02% | 0.02% |
| 20260530T215450Z | base_odds | False | convergence_prob_lower | False | True | False | n/a | n/a | n/a | 0 | 0 | 0.02% | 0.04% |

## Label Coverage

| Run | Trade-fill target | Label gate | Reasons |
|---|---:|---:|---|
| 20260530T163238Z | False | True | ok |
| 20260530T193847Z | False | True | ok |
| 20260530T195425Z | False | True | ok |
| 20260530T204923Z | False | True | ok |
| 20260530T211425Z | True | False | calibration split has zero positive `maker_trade_fill_positive` rows; calibration split has zero trade-feature rows for trade-confirmed fill target; calibration split has zero queue-confirmed maker fill rows; calibration split has zero nonzero `maker_trade_fill_pnl_per_share` rows; val split has zero positive `maker_trade_fill_positive` rows; val split has zero trade-feature rows for trade-confirmed fill target; val split has zero queue-confirmed maker fill rows; val split has zero nonzero `maker_trade_fill_pnl_per_share` rows; test split has zero positive `maker_trade_fill_positive` rows; test split has zero trade-feature rows for trade-confirmed fill target; test split has zero queue-confirmed maker fill rows; test split has zero nonzero `maker_trade_fill_pnl_per_share` rows |
| 20260530T213938Z | True | False | val split has zero positive `maker_trade_fill_positive` rows |
| 20260530T214959Z | True | False | val split has zero positive `maker_trade_fill_positive` rows |
| 20260530T215220Z | True | True | ok |
| 20260530T215450Z | True | True | ok |

## External Validation

External validation is run-level attribution against the latest market-disjoint and strict temporal reports. A run can pass its internal holdout gate and still fail this gate if the report is older, the ensemble differs, or either validation gate fails.

| Run | Feature set | Recent weight | External gate | Reasons |
|---|---|---:|---:|---|
| 20260530T163238Z | base_odds | 0.0 | False | market_disjoint validation target_col mismatch: expected maker_positive, got maker_trade_fill_positive; market_disjoint validation pnl_col mismatch: expected maker_pnl_per_share, got maker_trade_fill_pnl_per_share; market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_base_odds_latest.json; temporal validation target_col mismatch: expected maker_positive, got maker_trade_fill_positive; temporal validation pnl_col mismatch: expected maker_pnl_per_share, got maker_trade_fill_pnl_per_share; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_base_odds_latest.json |
| 20260530T193847Z | base_odds | 0.0 | False | market_disjoint validation target_col mismatch: expected lev_positive, got maker_trade_fill_positive; market_disjoint validation pnl_col mismatch: expected pnl_per_share, got maker_trade_fill_pnl_per_share; market_disjoint validation stake_col mismatch: expected entry_ask, got entry_bid; market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_base_odds_latest.json; temporal validation target_col mismatch: expected lev_positive, got maker_trade_fill_positive; temporal validation pnl_col mismatch: expected pnl_per_share, got maker_trade_fill_pnl_per_share; temporal validation stake_col mismatch: expected entry_ask, got entry_bid; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_base_odds_latest.json |
| 20260530T195425Z | base | 0.0 | False | market_disjoint validation target_col mismatch: expected lev_positive, got maker_trade_fill_positive; market_disjoint validation pnl_col mismatch: expected pnl_per_share, got maker_trade_fill_pnl_per_share; market_disjoint validation stake_col mismatch: expected entry_ask, got entry_bid; market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_latest.json; temporal validation target_col mismatch: expected lev_positive, got maker_trade_fill_positive; temporal validation pnl_col mismatch: expected pnl_per_share, got maker_trade_fill_pnl_per_share; temporal validation stake_col mismatch: expected entry_ask, got entry_bid; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_latest.json |
| 20260530T204923Z | base | 0.0 | False | market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_latest.json; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_latest.json |
| 20260530T211425Z | base | 0.0 | False | market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_latest.json; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_latest.json |
| 20260530T213938Z | base | 0.0 | False | market_disjoint validation report is older than the model artifact: telonex_walk_forward_latest.json; market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_latest.json; temporal validation report is older than the model artifact: telonex_temporal_validation_latest.json; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_latest.json |
| 20260530T214959Z | base | 0.0 | False | market_disjoint validation report is older than the model artifact: telonex_walk_forward_latest.json; market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_latest.json; temporal validation report is older than the model artifact: telonex_temporal_validation_latest.json; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_latest.json |
| 20260530T215220Z | base | 0.0 | False | market_disjoint validation report is older than the model artifact: telonex_walk_forward_latest.json; market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_latest.json; temporal validation report is older than the model artifact: telonex_temporal_validation_latest.json; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_latest.json |
| 20260530T215450Z | base_odds | 0.0 | False | market_disjoint validation gate failed: market_disjoint_gate=false in telonex_walk_forward_base_odds_latest.json; temporal validation gate failed: temporal_gate=false in telonex_temporal_validation_base_odds_latest.json |

## Odds Feature Validation

| Run | Uses odds | Performance gate | Odds gate | Test odds coverage | Test matched markets |
|---|---:|---:|---:|---:|---:|
| 20260530T163238Z | True | True | True | 0.00% | 0 |
| 20260530T193847Z | True | False | False | 0.00% | 0 |
| 20260530T195425Z | False | False | True | n/a | 0 |
| 20260530T204923Z | False | False | True | n/a | 0 |
| 20260530T211425Z | False | False | True | n/a | 0 |
| 20260530T213938Z | False | False | True | n/a | 0 |
| 20260530T214959Z | False | False | True | n/a | 0 |
| 20260530T215220Z | False | False | True | n/a | 0 |
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
