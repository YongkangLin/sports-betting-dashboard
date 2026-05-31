# Two-Sided Market Data Completeness

- Generated: 2026-05-31T14:43:56.314682+00:00
- Replay events audited: 277
- Polymarket CLOB actual two-sided events: 277 / 277 (100.0%)
- Polymarket derived-opposite events: 0
- Actual opposite-token CLOB minutes: 329,406
- Sportsbook complete-side events: 276 / 277 (99.6%)
- Sportsbook complete-side fair-probability points: 36,382
- Complete on both venues: 276 / 277 (99.6%)

Sportsbook fair probabilities now require complete sides in each bookmaker snapshot: h2h needs both competitors, soccer 3-way needs team/team/draw when draw is present, totals need Over and Under, and spreads need both competitors at the same point.

## Missing Examples

| Event | Market | Outcome | CLOB actual both sides | Sportsbook complete points | Odds match |
|---|---|---|---:|---:|---|
| Barcelona vs Bayern Munich | Soccer | No | yes | 0 | none |
