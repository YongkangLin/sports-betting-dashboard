# Favorite-Longshot Executable Backtest

- Generated: 2026-05-31T03:22:09.952153+00:00
- Verdict: HOLD: favorite-longshot executable bucket not yet proven
- Executable gate: False
- Gate reasons: clear-settlement cluster bootstrap CI lower bound is not positive
- Plan source: downloaded_manifest
- Target assets with downloaded books: 1,298 / 1,298
- Book rows scanned: 95,516,643
- Candidate entry tokens: 375
- Selected entries: 375
- Clear settlement entries: 277
- Output bets: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/execution_training/favorite_longshot_executable_bets_latest.parquet`

## Settlement Summary

| Bucket | Bets | Markets | ROI | 95% CI | Win rate | Avg ask | Avg spread |
|---|---:|---:|---:|---|---:|---:|---:|
| downloaded_manifest_high_prob_token | 277 | 277 | 1.42% | -3.09% to 5.92% | 89.17% | 87.64% | 1.22% |

## Settlement By Entry Phase

| Entry phase | Bets | Markets | ROI | 95% CI | Win rate | Avg ask |
|---|---:|---:|---:|---|---:|---:|
| at_end | 3 | 3 | -25.32% | -100.00% to 13.28% | 66.67% | 89.00% |
| 0_15m | 2 | 2 | -43.99% | -100.00% to 12.03% | 50.00% | 89.00% |
| 15_60m | 35 | 35 | 3.73% | -6.52% to 13.39% | 91.43% | 87.86% |
| 1_3h | 31 | 31 | 2.83% | -11.89% to 13.89% | 90.32% | 87.55% |
| 3_6h | 3 | 3 | 14.12% | 12.03% to 15.86% | 100.00% | 87.33% |
| 6_12h | 7 | 7 | -2.44% | -35.27% to 15.11% | 85.71% | 87.57% |
| 12_24h | 188 | 188 | 1.07% | -4.51% to 6.27% | 88.83% | 87.60% |
| 24h_plus | 8 | 8 | 14.39% | 11.65% to 16.36% | 100.00% | 87.12% |

## Settlement By Sport

| Sport | Bets | Markets | ROI | 95% CI | Win rate | Avg ask |
|---|---:|---:|---:|---|---:|---:|
| soccer | 175 | 175 | 0.19% | -5.27% to 5.26% | 88.00% | 87.55% |
| basketball_nba | 89 | 89 | 3.25% | -4.34% to 9.87% | 91.01% | 87.87% |
| americanfootball_nfl | 9 | 9 | 13.70% | 12.44% to 15.28% | 100.00% | 87.67% |
| basketball_wnba | 2 | 2 | -42.41% | -100.00% to 15.86% | 50.00% | 86.50% |
| icehockey_nhl | 2 | 2 | 15.86% | 14.55% to 17.20% | 100.00% | 86.00% |

## Future-Bid Exit Summary

| Horizon | Bucket | Bets | Markets | ROI | 95% CI | Avg ask | Avg spread |
|---:|---|---:|---:|---:|---|---:|---:|
| 300 | downloaded_manifest_high_prob_token | 352 | 346 | -2.32% | -2.89% to -1.91% | 87.48% | 1.47% |
| 900 | downloaded_manifest_high_prob_token | 354 | 351 | -2.57% | -3.32% to -1.89% | 87.48% | 1.48% |
| 3600 | downloaded_manifest_high_prob_token | 333 | 333 | -2.03% | -2.61% to -1.45% | 87.62% | 1.38% |
| 21600 | downloaded_manifest_high_prob_token | 237 | 237 | -1.83% | -1.99% to -1.67% | 87.73% | 1.27% |
| 86400 | downloaded_manifest_high_prob_token | 17 | 17 | -4.78% | -7.37% to -2.77% | 88.82% | 3.29% |

## Interpretation

- This is still a CLOB-data proof step, not a live-capital claim.
- Settlement rows require downloaded books that reach a clear post-event 0/1-like state; incomplete windows are excluded from settlement ROI.
- Future-bid rows model a taker buy followed by an executable bid exit after the requested horizon, with conservative entry/exit fee assumptions.
