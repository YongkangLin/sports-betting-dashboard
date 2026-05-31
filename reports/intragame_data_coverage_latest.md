# Intragame Trading Data Coverage

This audit checks the partitioned fact store for post-commence price rows. It also checks Telonex historical CLOB coverage. Telonex can certify public bid/ask/depth/trade presence, but not private fills or queue position.

## Source Summary

| Source | Rows | Events | Post-start rows | Post-start events | Event coverage |
|---|---:|---:|---:|---:|---:|

## Telonex Historical CLOB

| Existing files | Missing files | Manifest files | Rows | Quote rows | Depth rows | Trade rows | Depth files | Date span |
|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 1,136 | 5,189 | 6,325 | 51,344,670 | 7,618,994 | 42,864,676 | 861,000 | 380 | 2025-10-26 to 2026-05-29 |

## Interpretation

- Current data can draw a proxy Polymarket price path and compare it with the model's pregame fair value.
- Telonex is the canonical historical executable quote/depth/trade source for LEV/convergence labels.
- Current data still cannot prove a live trading bot end-to-end because it has no authenticated private order lifecycle, actual fills, true queue-ahead, or realized market impact from our orders.
- Odds API rows after commence are only useful if they represent true live/in-play snapshots; this audit measures their presence, not bookmaker coverage quality.

## Top Post-start Segments

| Source | Sport | Market | Rows | Events | Post-start events | Coverage |
|---|---|---|---:|---:|---:|---:|
