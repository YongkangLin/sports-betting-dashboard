# Two-Sided Market Data Completeness

- Generated: 2026-05-31T07:54:48.865120+00:00
- Replay events audited: 277
- Polymarket CLOB actual two-sided events: 277 / 277 (100.0%)
- Polymarket derived-opposite events: 0
- Actual opposite-token CLOB minutes: 329,406
- Sportsbook complete-side events: 265 / 277 (95.7%)
- Sportsbook complete-side fair-probability points: 23,511
- Complete on both venues: 265 / 277 (95.7%)

Sportsbook fair probabilities now require complete sides in each bookmaker snapshot: h2h needs both competitors, soccer 3-way needs team/team/draw when draw is present, totals need Over and Under, and spreads need both competitors at the same point.

## Missing Examples

| Event | Market | Outcome | CLOB actual both sides | Sportsbook complete points | Odds match |
|---|---|---|---:|---:|---|
| Oilers vs Ducks total 4.5 | NHL | Over | yes | 0 | icehockey_nhl |
| Palmeiras vs Grêmio | Soccer | No | yes | 0 | soccer_brazil_campeonato |
| AS Monaco vs Paris Saint Germain | Soccer | No | yes | 0 | soccer_uefa_champs_league |
| Bayer Leverkusen vs Arsenal | Soccer | No | yes | 0 | soccer_uefa_champs_league |
| Bragantino vs Ceará | Soccer | No | yes | 0 | none |
| Nets vs Heat | NBA | Heat | yes | 0 | basketball_nba |
| Nottingham Forest vs Burnley | Soccer | No | yes | 0 | soccer_epl |
| Tottenham Hotspur vs Sporting Lisbon | Soccer | No | yes | 0 | none |
| Qarabağ FK vs Newcastle United | Soccer | No | yes | 0 | soccer_uefa_champs_league |
| Sporting Lisbon vs Barcelona | Soccer | No | yes | 0 | none |
| Barcelona vs BM | Soccer | No | yes | 0 | none |
| Fredrikstad FK vs IK Start spread away-1.5 | Soccer | Fredrikstad FK | yes | 0 | soccer_norway_eliteserien |
