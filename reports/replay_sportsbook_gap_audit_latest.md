# Replay Sportsbook Gap Audit

- Generated: 2026-05-31T08:16:10.936342+00:00
- Replay events audited: 277
- Events with sportsbook overlay points: 267
- Events with matched Odds API event but no usable sportsbook line: 6
- Events needing data/action review: 48

## Interpretation

- Polymarket CLOB series can run to settlement, where prices become 0/100.
- Sportsbook series are quoted fair probabilities only. They normally stop at the last offered line when the book suspends or removes the market; they do not settle to 0/100.
- A late sportsbook start is only a data problem when the Odds API event was already listed and our quote pull/side matching still has no usable line.

## Classification Counts

| Classification | Events |
|---|---:|
| has_sportsbook_overlay | 267 |
| internal_quote_gap_over_30m | 38 |
| sportsbook_event_not_listed_until_after_clob_start | 7 |
| matched_event_no_quotes_in_warehouse | 5 |
| no_odds_event_match | 4 |
| sportsbook_last_quote_not_settlement | 3 |
| sportsbook_starts_after_clob | 2 |
| quotes_present_but_incomplete_sides_or_target | 1 |

## Events Needing Review

| Event | Sport | Points | Classifications | Diagnostic |
|---|---|---:|---|---|
| Manchester United vs Crystal Palace | soccer | 144 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Newcastle United vs PSV Eindhoven | soccer | 187 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Palmeiras vs Grêmio | soccer | 0 | matched_event_no_quotes_in_warehouse | matched_event_no_quotes_in_warehouse |
| Paris Saint Germain vs Lyon | soccer | 182 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Real Madrid vs Celta Vigo | soccer | 157 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Wizards vs Bulls | basketball_nba | 35 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Wizards vs Hawks | basketball_nba | 74 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| AS Monaco vs Paris Saint Germain | soccer | 0 | matched_event_no_quotes_in_warehouse | matched_event_no_quotes_in_warehouse |
| Bayer Leverkusen vs Arsenal | soccer | 0 | matched_event_no_quotes_in_warehouse | matched_event_no_quotes_in_warehouse |
| Bayern Munich vs VfB Stuttgart | soccer | 141 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| CRE vs Napoli | soccer | 164 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Manchester United vs West Ham United | soccer | 192 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| ROM vs GEN | soccer | 158 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| VfB Stuttgart vs VfL Wolfsburg | soccer | 142 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Bragantino vs Ceará | soccer | 0 | no_odds_event_match |  |
| Lille vs Nantes | soccer | 176 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Lille vs Nice | soccer | 180 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Mirassol vs Chapecoense | soccer | 200 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Nets vs Heat | basketball_nba | 42 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| PAR vs Napoli | soccer | 146 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| PAR vs ROM | soccer | 170 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| RC Lens vs Nice | soccer | 164 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| VER vs MIL | soccer | 146 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| 1. FC Köln vs Bayern Munich | soccer | 185 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Barcelona vs Celta Vigo | soccer | 187 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| CRE vs MIL | soccer | 143 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Jets vs Jaguars | americanfootball_nfl | 89 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Juventus vs BOL | soccer | 169 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Nottingham Forest vs Burnley | soccer | 0 | matched_event_no_quotes_in_warehouse | matched_event_no_quotes_in_warehouse |
| Tottenham Hotspur vs Sporting Lisbon | soccer | 0 | no_odds_event_match |  |
| ATA vs PAR | soccer | 137 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Arsenal vs Fulham | soccer | 164 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Club Brugge vs Arsenal | soccer | 181 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Qarabağ FK vs Newcastle United | soccer | 0 | matched_event_no_quotes_in_warehouse | matched_event_no_quotes_in_warehouse |
| ROM vs CAG | soccer | 172 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Rennes vs Nantes | soccer | 158 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Suns vs Thunder | basketball_nba | 92 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| VER vs COM | soccer | 148 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| VfB Stuttgart vs Hamburger SV | soccer | 154 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| LEE vs Burnley | soccer | 86 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Lille vs Le Havre | soccer | 151 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Sporting Lisbon vs Barcelona | soccer | 0 | no_odds_event_match |  |
| Venezia vs Juve Stabia | soccer | 151 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Borussia Dortmund vs Bodø/Glimt | soccer | 181 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Barcelona vs BM | soccer | 0 | no_odds_event_match |  |
| Fredrikstad FK vs IK Start spread away-1.5 | soccer | 0 | quotes_present_but_incomplete_sides_or_target | quotes_present_but_incomplete_sides_or_target |
| Napoli vs BOL | soccer | 169 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |
| Paris Saint Germain vs AS Monaco | soccer | 193 | has_sportsbook_overlay, internal_quote_gap_over_30m |  |

## Largest Late Starts

| Event | Sport | Start gap | First seen gap | Points | Classification |
|---|---|---:|---:|---:|---|
| Vålerenga vs Kristiansund BK total 1.5 | soccer | 7.8d | 6.2d | 2 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Knicks vs Grizzlies | basketball_nba | 5.5d | 6.5d | 101 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Wizards vs Magic | basketball_nba | 5.5d | 5.5d | 105 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| 76ers vs Nuggets | basketball_nba | 5.4d | 5.5d | 115 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Pacers vs Knicks | basketball_nba | 5.4d | 5.4d | 107 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Warriors vs Knicks | basketball_nba | 5.4d | 6.3d | 127 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Rockets vs Wizards | basketball_nba | 5.4d | 6.5d | 117 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Jazz vs Spurs | basketball_nba | 36.6m | 36.6m | 97 | has_sportsbook_overlay, sportsbook_starts_after_clob |
| Pacers vs Hornets | basketball_nba | 25.6m | 25.6m | 98 | has_sportsbook_overlay, sportsbook_starts_after_clob |
| ATA vs GEN | soccer | -4.4m | -5.3h | 91 | has_sportsbook_overlay |
| ATA vs TOR | soccer | -4.4m | 11.4h | 96 | has_sportsbook_overlay |
| Angers vs Paris Saint Germain | soccer | -4.4m | -5.5d | 80 | has_sportsbook_overlay |

## Largest Internal Quote Gaps

| Event | Sport | Max gap | Median gap | Points |
|---|---|---:|---:|---:|
| Wizards vs Bulls | basketball_nba | 21.0h | 12.5m | 35 |
| Nets vs Heat | basketball_nba | 18.5h | 15.0m | 42 |
| Wizards vs Hawks | basketball_nba | 10.5h | 15.0m | 74 |
| Real Madrid vs Celta Vigo | soccer | 9.5h | 15.0m | 157 |
| Bayern Munich vs VfB Stuttgart | soccer | 8.5h | 15.0m | 141 |
| ATA vs PAR | soccer | 8.5h | 15.0m | 137 |
| ROM vs GEN | soccer | 8.3h | 15.0m | 158 |
| VfB Stuttgart vs VfL Wolfsburg | soccer | 7.5h | 15.0m | 142 |
| Manchester United vs Crystal Palace | soccer | 7.2h | 15.0m | 144 |
| PAR vs Napoli | soccer | 6.0h | 15.0m | 146 |
| VfB Stuttgart vs Hamburger SV | soccer | 6.0h | 15.0m | 154 |
| Napoli vs BOL | soccer | 6.0h | 15.0m | 169 |

## Cited Examples

| Event | Sportsbook match | Points | Start gap | Last quote to final | Last selected fair | Notes |
|---|---|---:|---:|---:|---:|---|
| 76ers vs Nuggets | Denver Nuggets vs Philadelphia 76ers 2026-03-18T01:10:00+00:00 | 115 | 5.4d | 5.1m | 97.1% | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Oilers vs Ducks total 4.5 | Anaheim Ducks vs Edmonton Oilers 2026-04-25T02:10:00+00:00 | 12 | -4.4m | 1.7h | 84.6% | has_sportsbook_overlay, sportsbook_last_quote_not_settlement |
