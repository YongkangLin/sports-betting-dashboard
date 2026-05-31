# Queue / Fill Training

- Generated: 2026-05-31T00:05:46.973103+00:00
- Rows: 2127
- Sources: {'live_paper_order': 2127}
- Authenticated lifecycle queue rows: 0
- Live paper queue rows: 2127
- Label horizon seconds: 60
- Output: /Users/yongkanglin/Documents/Codex/2026-05-28/i-have-this-repo-git-github-3/Sports-Betting-ml/data/processed/execution_training/queue_fill_training_latest.parquet

Rows include live paper-order queue labels plus authenticated user-channel lifecycle labels when available. True production queue position still requires authenticated order IDs and real fills.

## Summary

```text
          source               strategy liquidity_tier  rows  fill_rate  mean_queue_ahead  mean_spread
live_paper_order favorite_longshot_bias           dead    14   0.000000          0.000000     0.047143
live_paper_order favorite_longshot_bias           deep  1027   0.722493          0.000000     0.009925
live_paper_order favorite_longshot_bias       standard   119   0.588235          0.000000     0.019244
live_paper_order favorite_longshot_bias           thin     7   1.000000          0.000000     0.030000
live_paper_order    passive_queue_probe           dead     6   0.000000          8.660000     0.010000
live_paper_order    passive_queue_probe           deep   919   0.008705     183958.445277     0.010000
live_paper_order    passive_queue_probe       standard    34   0.000000       1547.415000     0.017353
live_paper_order    passive_queue_probe            NaN     1   0.000000      24531.740000          NaN
```

## Label Sources

```text
      fill_label_source  rows
no_cross_within_horizon  1300
         paper_fill_log   421
      future_book_cross   406
```
