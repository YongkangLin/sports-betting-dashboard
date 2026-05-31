# Queue / Fill Training

- Generated: 2026-05-31T01:14:16.183800+00:00
- Rows: 2287
- Sources: {'live_paper_order': 2287}
- Authenticated lifecycle queue rows: 0
- Live paper queue rows: 2287
- Label horizon seconds: 60
- Output: /Users/yongkanglin/Documents/Codex/2026-05-28/i-have-this-repo-git-github-3/Sports-Betting-ml/data/processed/execution_training/queue_fill_training_latest.parquet

Rows include live paper-order queue labels plus authenticated user-channel lifecycle labels when available. True production queue position still requires authenticated order IDs and real fills.

## Summary

```text
          source               strategy liquidity_tier  rows  fill_rate  mean_queue_ahead  mean_spread
live_paper_order favorite_longshot_bias           dead    14   0.000000          0.000000     0.047143
live_paper_order favorite_longshot_bias           deep  1041   0.720461          0.000000     0.009926
live_paper_order favorite_longshot_bias       standard   121   0.595041          0.000000     0.019256
live_paper_order favorite_longshot_bias           thin     7   1.000000          0.000000     0.030000
live_paper_order    passive_queue_probe           dead     6   0.000000          8.660000     0.010000
live_paper_order    passive_queue_probe           deep  1051   0.011418     172769.083853     0.010000
live_paper_order    passive_queue_probe       standard    46   0.000000       1182.366304     0.017609
live_paper_order    passive_queue_probe            NaN     1   0.000000      24531.740000          NaN
```

## Label Sources

```text
      fill_label_source  rows
no_cross_within_horizon  1446
         paper_fill_log   421
      future_book_cross   420
```
