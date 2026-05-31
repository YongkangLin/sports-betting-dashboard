# Two-Sided Market Data Completeness

- Generated: 2026-05-31T08:36:57.507980+00:00
- Replay events audited: 277
- Polymarket CLOB actual two-sided events: 277 / 277 (100.0%)
- Polymarket derived-opposite events: 0
- Actual opposite-token CLOB minutes: 329,406
- Sportsbook complete-side events: 273 / 277 (98.6%)
- Sportsbook complete-side fair-probability points: 18,926
- Complete on both venues: 273 / 277 (98.6%)

Sportsbook fair probabilities now require complete sides in each bookmaker snapshot: h2h needs both competitors, soccer 3-way needs team/team/draw when draw is present, totals need Over and Under, and spreads need both competitors at the same point.

## Missing Examples

| Event | Market | Outcome | CLOB actual both sides | Sportsbook complete points | Odds match |
|---|---|---|---:|---:|---|
| Bragantino vs Ceará | Soccer | No | yes | 0 | none |
| Tottenham Hotspur vs Sporting Lisbon | Soccer | No | yes | 0 | none |
| Sporting Lisbon vs Barcelona | Soccer | No | yes | 0 | none |
| Barcelona vs BM | Soccer | No | yes | 0 | none |
