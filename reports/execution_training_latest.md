# Execution Training Set

- Generated: 2026-05-31T01:14:01.548580+00:00
- Rows: 294
- Output: /Users/yongkanglin/Documents/Codex/2026-05-28/i-have-this-repo-git-github-3/Sports-Betting-ml/data/processed/execution_training/execution_training_latest.parquet
- Retention deleted/kept snapshots: 1 / 24

## Gate

This table trains convergence/LEV models. It must grow to hundreds or thousands of fills before any profitability claim is credible.

## Summary

```text
              strategy  horizon_sec  rows positive_rate  mean_pnl_usd
 data_collection_probe           30     3           0.0     -0.248140
 data_collection_probe          300    51      0.102041     -0.076868
favorite_longshot_bias           30     7      0.142857     -1.886190
favorite_longshot_bias           60   106      0.056604     -3.971289
favorite_longshot_bias          120    74      0.347222     -5.775728
favorite_longshot_bias          300    53      0.226415     -5.079332
```
