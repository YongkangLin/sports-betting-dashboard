# Replay Sportsbook Gap Audit

- Generated: 2026-05-31T08:39:21.570862+00:00
- Replay events audited: 277
- Events with sportsbook overlay points: 273
- Events with matched Odds API event but no usable sportsbook line: 0
- Events needing data/action review: 4

## Interpretation

- Polymarket CLOB series can run to settlement, where prices become 0/100.
- Sportsbook series are quoted fair probabilities only. They normally stop at the last offered line when the book suspends or removes the market; they do not settle to 0/100.
- A late sportsbook start is only a data problem when the Odds API event was already listed and our quote pull/side matching still has no usable line.
- Internal quote gaps with complete raw cache are source/book availability gaps, not local missing-download gaps.
- End gaps with complete raw cache mean the book stopped offering a usable complete line before the Polymarket market settled.

## Classification Counts

| Classification | Events |
|---|---:|
| has_sportsbook_overlay | 273 |
| sportsbook_event_not_listed_until_after_clob_start | 8 |
| no_odds_event_match | 4 |
| sportsbook_last_quote_not_settlement | 4 |
| source_quote_gap_cache_complete | 3 |
| sportsbook_starts_after_clob | 2 |
| source_ended_before_market_end_cache_complete | 1 |

## Events Needing Review

| Event | Sport | Points | Classifications | Diagnostic |
|---|---|---:|---|---|
| Bragantino vs Ceará | soccer | 0 | no_odds_event_match |  |
| Tottenham Hotspur vs Sporting Lisbon | soccer | 0 | no_odds_event_match |  |
| Sporting Lisbon vs Barcelona | soccer | 0 | no_odds_event_match |  |
| Barcelona vs BM | soccer | 0 | no_odds_event_match |  |

## Largest Late Starts

| Event | Sport | Start gap | First seen gap | Points | Classification |
|---|---|---:|---:|---:|---|
| Vålerenga vs Kristiansund BK total 1.5 | soccer | 7.8d | 6.2d | 2 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Knicks vs Grizzlies | basketball_nba | 5.5d | 6.5d | 101 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Wizards vs Magic | basketball_nba | 5.5d | 5.5d | 104 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| 76ers vs Nuggets | basketball_nba | 5.4d | 5.5d | 115 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Pacers vs Knicks | basketball_nba | 5.4d | 5.4d | 107 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Warriors vs Knicks | basketball_nba | 5.4d | 6.3d | 126 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Rockets vs Wizards | basketball_nba | 5.4d | 6.5d | 116 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Fredrikstad FK vs IK Start spread away-1.5 | soccer | 22.9h | 6.2d | 346 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start, source_quote_gap_cache_complete, sportsbook_last_quote_not_settlement, source_ended_before_market_end_cache_complete |
| Jazz vs Spurs | basketball_nba | 36.6m | 36.6m | 97 | has_sportsbook_overlay, sportsbook_starts_after_clob |
| Pacers vs Hornets | basketball_nba | 25.6m | 25.6m | 98 | has_sportsbook_overlay, sportsbook_starts_after_clob |
| Lanus vs LDU Quito | soccer | 10.6m | 21.7h | 103 | has_sportsbook_overlay |
| Cavaliers vs Mavericks | basketball_nba | 10.6m | 23.9h | 105 | has_sportsbook_overlay |

## Largest Internal Quote Gaps

| Event | Sport | Max gap | Cache missing | Median gap | Points |
|---|---|---:|---:|---:|---:|
| Fredrikstad FK vs IK Start spread away-1.5 | soccer | 2.6d | 0 / 251 | 15.0m | 346 |
| LEE vs Burnley | soccer | 1.3h | 0 / 5 | 15.0m | 85 |
| Suns vs Thunder | basketball_nba | 45.0m | 0 / 3 | 15.0m | 91 |
| PAR vs Juventus | soccer | 30.0m | 0 / 2 | 15.0m | 90 |
| SAS vs Inter Milan | soccer | 25.0m | 0 / 2 | 15.0m | 78 |
| RC Lens vs Nantes | soccer | 18.0m | 0 / 1 | 15.0m | 88 |
| CAG vs Juventus | soccer | 15.2m | 0 / 1 | 15.0m | 93 |
| ATA vs TOR | soccer | 15.1m | 0 / 1 | 15.0m | 94 |
| Nottingham Forest vs Arsenal | soccer | 15.1m | 0 / 1 | 15.0m | 68 |
| ROM vs SAS | soccer | 15.1m | 0 / 1 | 15.0m | 81 |
| Villarreal vs Alavés | soccer | 15.1m | 0 / 1 | 15.0m | 73 |
| Napoli vs SAS | soccer | 15.1m | 0 / 1 | 15.0m | 87 |

## Cited Examples

| Event | Sportsbook match | Points | Start gap | Last quote to final | Last selected fair | Notes |
|---|---|---:|---:|---:|---:|---|
| 76ers vs Nuggets | Denver Nuggets vs Philadelphia 76ers 2026-03-18T01:10:00+00:00 | 115 | 5.4d | 5.1m | 97.1% | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Oilers vs Ducks total 4.5 | Anaheim Ducks vs Edmonton Oilers 2026-04-25T02:10:00+00:00 | 11 | 38s | 1.7h | 84.6% | has_sportsbook_overlay, sportsbook_last_quote_not_settlement |
