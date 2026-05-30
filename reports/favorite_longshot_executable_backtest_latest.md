# Favorite-Longshot Executable Backtest

- Generated: 2026-05-30T23:16:39.248701+00:00
- Verdict: HOLD: favorite-longshot executable bucket not yet proven
- Executable gate: False
- Gate reasons: need >=200 clear-settlement bets, need >=50 clear-settlement markets
- Target assets with downloaded books: 15 / 848
- Book rows scanned: 2,099,670
- Candidate entry tokens: 7
- Selected entries: 7
- Clear settlement entries: 6
- Output bets: `/Users/yongkanglin/Documents/Codex/2026-05-28/i-have-this-repo-git-github-3/Sports-Betting-ml/data/processed/execution_training/favorite_longshot_executable_bets_latest.parquet`

## Settlement Summary

| Bucket | Bets | Markets | ROI | 95% CI | Win rate | Avg ask | Avg spread |
|---|---:|---:|---:|---|---:|---:|---:|
| high_prob_token_in_favorite_or_longshot_market | 6 | 6 | 15.86% | 14.77% to 16.97% | 100.00% | 86.00% | 3.50% |

## Future-Bid Exit Summary

| Horizon | Bucket | Bets | Markets | ROI | 95% CI | Avg ask | Avg spread |
|---:|---|---:|---:|---:|---|---:|---:|
| 300 | high_prob_token_in_favorite_or_longshot_market | 5 | 5 | -3.40% | -4.54% to -2.22% | 86.60% | 2.80% |
| 900 | high_prob_token_in_favorite_or_longshot_market | 5 | 5 | -7.44% | -14.80% to -3.06% | 86.20% | 2.60% |
| 3600 | high_prob_token_in_favorite_or_longshot_market | 5 | 5 | -8.60% | -14.73% to -4.00% | 86.40% | 3.00% |
| 21600 | high_prob_token_in_favorite_or_longshot_market | 2 | 2 | -0.30% | -0.90% to 0.30% | 85.00% | 3.00% |
| 86400 | high_prob_token_in_favorite_or_longshot_market | 5 | 5 | -2.25% | -5.66% to 0.78% | 86.20% | 2.60% |

## Interpretation

- This is still a CLOB-data proof step, not a live-capital claim.
- Settlement rows require downloaded books that reach a clear post-event 0/1-like state; incomplete windows are excluded from settlement ROI.
- Future-bid rows model a taker buy followed by an executable bid exit after the requested horizon, with conservative entry/exit fee assumptions.
