# Queue / Fill Training

- Generated: 2026-05-31T00:21:42.710955+00:00
- Rows: 2171
- Sources: {'live_paper_order': 2171}
- Authenticated lifecycle queue rows: 0
- Live paper queue rows: 2171
- Label horizon seconds: 60
- Output: /Users/yongkanglin/Documents/Codex/2026-05-28/i-have-this-repo-git-github-3/Sports-Betting-ml/data/processed/execution_training/queue_fill_training_latest.parquet

Rows include live paper-order queue labels plus authenticated user-channel lifecycle labels when available. True production queue position still requires authenticated order IDs and real fills.

## Summary

```text
          source               strategy liquidity_tier  rows  fill_rate  mean_queue_ahead  mean_spread
live_paper_order favorite_longshot_bias           dead    14   0.000000          0.000000     0.047143
live_paper_order favorite_longshot_bias           deep  1034   0.721470          0.000000     0.009926
live_paper_order favorite_longshot_bias       standard   120   0.591667          0.000000     0.019250
live_paper_order favorite_longshot_bias           thin     7   1.000000          0.000000     0.030000
live_paper_order    passive_queue_probe           dead     6   0.000000          8.660000     0.010000
live_paper_order    passive_queue_probe           deep   953   0.012592     180738.076264     0.010000
live_paper_order    passive_queue_probe       standard    36   0.000000       1510.801389     0.016944
live_paper_order    passive_queue_probe            NaN     1   0.000000      24531.740000          NaN
```

## Label Sources

```text
      fill_label_source  rows
no_cross_within_horizon  1335
         paper_fill_log   421
      future_book_cross   415
```
