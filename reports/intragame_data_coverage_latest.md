# Intragame Trading Data Coverage

This audit checks the partitioned fact store for post-commence price rows. It also checks Telonex historical CLOB coverage. Telonex can certify public bid/ask/depth/trade presence, but not private fills or queue position.

## Source Summary

| Source | Rows | Events | Post-start rows | Post-start events | Event coverage |
|---|---:|---:|---:|---:|---:|

## Telonex Historical CLOB

| Files | Rows | Quote rows | Depth rows | Trade rows | Depth files | Date span |
|---:|---:|---:|---:|---:|---:|---|
| 4,437 | 41,463,175 | 6,719,183 | 34,575,311 | 168,681 | 1,745 | None to None |

## Interpretation

- Current data can draw a proxy Polymarket price path and compare it with the model's pregame fair value.
- Telonex is the canonical historical executable quote/depth/trade source for LEV/convergence labels.
- Current data still cannot prove a live trading bot end-to-end because it has no authenticated private order lifecycle, actual fills, true queue-ahead, or realized market impact from our orders.
- Odds API rows after commence are only useful if they represent true live/in-play snapshots; this audit measures their presence, not bookmaker coverage quality.

## Top Post-start Segments

| Source | Sport | Market | Rows | Events | Post-start events | Coverage |
|---|---|---|---:|---:|---:|---:|
