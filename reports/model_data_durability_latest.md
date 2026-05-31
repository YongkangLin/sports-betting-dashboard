# Model Data Durability

Generated: 2026-05-31

## What is safe if this machine dies

The repo now tracks the curated, model-ready replay-aligned sportsbook dataset:

- Dataset: `data/warehouse/odds_api/quotes_partitioned/**/part-replay-aligned-*.parquet`
- Files: 187 Parquet shards
- Rows: 44,824,626 sportsbook quote rows
- Size: 123,613,804 bytes in the tracked shards
- Manifest: `data/warehouse/odds_api/replay_aligned_quotes_manifest_latest.json`
- Pull manifest: `data/warehouse/odds_api/replay_aligned_snapshot_pull_latest.json`
- Human report: `reports/odds_api_replay_aligned_quotes_manifest_latest.md`

These are the shards the replay/dashboard/model pipeline can use directly. They are intentionally smaller than the raw API cache and are suitable for normal Git storage.

## What is intentionally not in normal Git

The raw Odds API JSON cache is local and reproducible:

- Path: `data/cache/odds_api_historical`
- Size at generation time: about 9.2 GB

Normal Git is the wrong storage layer for that cache. If raw cache durability becomes required, use Git LFS, a GitHub Release artifact, or object storage such as S3/R2. Until then, the curated Parquet shards plus pull manifests are the durable source for model/replay work.

## Current replay data backed by the durable shards

- Settled replay events: 277
- Two-sided CLOB-complete events: 265
- CLOB one-minute points: 329,406
- Sportsbook snapshots in replay: 24,163
- Sportsbook-matched events: 273

Remaining sportsbook gaps are treated as real missing market availability, not patched with fabricated interpolation.
