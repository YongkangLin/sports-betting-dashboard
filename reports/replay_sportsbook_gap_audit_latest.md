# Replay Sportsbook Gap Audit

- Generated: 2026-05-31T11:13:10.945718+00:00
- Replay events audited: 277
- Events with sportsbook overlay points: 276
- Events with matched Odds API event but no usable sportsbook line: 0
- Events needing data/action review: 1

## Interpretation

- Polymarket CLOB series can run to settlement, where prices become 0/100.
- Sportsbook series are quoted fair probabilities only. They normally stop at the last offered line when the book suspends or removes the market; they do not settle to 0/100.
- A late sportsbook start is only a data problem when the Odds API event was already listed and our quote pull/side matching still has no usable line.
- Internal quote gaps with complete raw cache are source/book availability gaps, not local missing-download gaps.
- End gaps with complete raw cache mean the book stopped offering a usable complete line before the Polymarket market settled.
- The dashboard CLOB line is a one-minute replay series. Sportsbook overlays are historical Odds API snapshots; this audit treats 15-minute raw-cache coverage as the current dashboard completeness gate and separately reports how much five-minute native coverage is still uncached.

## Cache And Series Completeness

| Check | Result |
|---|---:|
| CLOB one-minute replay events with no missing minutes | 277 / 277 |
| Odds matched events with complete 15m raw cache | 276 / 276 |
| Unique 15m raw cache snapshots cached / expected / missing | 17,026 / 17,026 / 0 |
| Odds matched events with complete 5m raw cache | 155 / 276 |
| Odds matched events with any missing 5m cache | 121 |
| Unique 5m raw cache snapshots cached / expected / missing | 31,133 / 46,443 / 15,310 |
| Warehouse all-partition replay-window checks | 276 / 276 |
| Events with extra non-replay sportsbook timestamps inside replay window | 0 |
| Extra non-replay sportsbook timestamps inside replay windows | 0 |

## Cache Coverage By Sport

| Sport | Events | Sportsbook overlay | Complete 15m cache | Complete 5m cache | Missing 5m cache | Needs review |
|---|---:|---:|---:|---:|---:|---:|
| americanfootball_nfl | 9 | 9 | 9 | 9 | 0 | 0 |
| basketball_nba | 89 | 89 | 89 | 88 | 1 | 0 |
| basketball_wnba | 2 | 2 | 2 | 2 | 0 | 0 |
| icehockey_nhl | 2 | 2 | 2 | 2 | 0 | 0 |
| soccer | 175 | 174 | 174 | 54 | 120 | 1 |

## Classification Counts

| Classification | Events |
|---|---:|
| has_sportsbook_overlay | 276 |
| sportsbook_event_not_listed_until_after_clob_start | 8 |
| source_quote_gap_cache_complete | 3 |
| sportsbook_last_quote_not_settlement | 3 |
| sportsbook_starts_after_clob | 2 |
| internal_quote_gap_missing_5m_api_cache | 1 |
| no_odds_event_match | 1 |
| sportsbook_end_gap_missing_5m_api_cache | 1 |

## Events Needing Review

| Event | Sport | Points | Classifications | Diagnostic |
|---|---|---:|---|---|
| Barcelona vs Bayern Munich | soccer | 0 | no_odds_event_match |  |

## Missing 5m Raw Cache

These are collection/credit gaps at native Odds API granularity. The 15-minute cache is complete, so the dashboard can still show sportsbook overlays, but not full 5-minute density for these events.

| Event | Sport | Missing / Expected | Points | Classifications |
|---|---|---:|---:|---|
| ATA vs GEN | soccer | 159 / 248 | 89 | has_sportsbook_overlay |
| ATA vs TOR | soccer | 166 / 260 | 94 | has_sportsbook_overlay |
| Angers vs Paris Saint Germain | soccer | 145 / 226 | 79 | has_sportsbook_overlay |
| COM vs TOR | soccer | 119 / 187 | 67 | has_sportsbook_overlay |
| CRE vs COM | soccer | 154 / 248 | 93 | has_sportsbook_overlay |
| Elche CF vs Barcelona | soccer | 169 / 263 | 93 | has_sportsbook_overlay |
| LAZ vs CRE | soccer | 145 / 227 | 82 | has_sportsbook_overlay |
| Le Havre vs Paris Saint Germain | soccer | 169 / 264 | 95 | has_sportsbook_overlay |
| Newcastle United vs PSV Eindhoven | soccer | 167 / 259 | 91 | has_sportsbook_overlay |
| Paris Saint Germain vs Lyon | soccer | 157 / 249 | 92 | has_sportsbook_overlay |
| RB Leipzig vs Borussia Monchengladbach | soccer | 117 / 185 | 68 | has_sportsbook_overlay |
| ROM vs FIO | soccer | 155 / 241 | 86 | has_sportsbook_overlay |
| Real Madrid vs Celta Vigo | soccer | 171 / 264 | 93 | has_sportsbook_overlay |
| AS Monaco vs Paris Saint Germain | soccer | 169 / 263 | 94 | has_sportsbook_overlay |
| Atlético Madrid vs Bodø/Glimt | soccer | 169 / 265 | 95 | has_sportsbook_overlay |
| Bayer Leverkusen vs Arsenal | soccer | 151 / 236 | 85 | has_sportsbook_overlay |
| Bayern Munich vs VfB Stuttgart | soccer | 129 / 202 | 72 | has_sportsbook_overlay |
| CAG vs MIL | soccer | 167 / 260 | 93 | has_sportsbook_overlay |
| CRE vs Napoli | soccer | 120 / 189 | 69 | has_sportsbook_overlay |
| Frosinone vs Padova | soccer | 130 / 204 | 74 | has_sportsbook_overlay |
| GEN vs Inter Milan | soccer | 144 / 227 | 83 | has_sportsbook_overlay |
| Liverpool vs Galatasaray | soccer | 165 / 257 | 92 | has_sportsbook_overlay |
| Modena vs Carrarese | soccer | 122 / 192 | 69 | has_sportsbook_overlay |
| PIS vs MIL | soccer | 167 / 260 | 93 | has_sportsbook_overlay |
| Paris Saint Germain vs Marseille | soccer | 163 / 254 | 91 | has_sportsbook_overlay |
| RC Lens vs Nantes | soccer | 159 / 247 | 88 | has_sportsbook_overlay |
| RC Lens vs Toulouse | soccer | 159 / 248 | 89 | has_sportsbook_overlay |
| ROM vs GEN | soccer | 158 / 246 | 88 | has_sportsbook_overlay |
| Real Madrid vs Alavés | soccer | 166 / 258 | 92 | has_sportsbook_overlay |
| Real Madrid vs Oviedo | soccer | 165 / 256 | 91 | has_sportsbook_overlay |
| Venezia vs Mantova | soccer | 114 / 179 | 65 | has_sportsbook_overlay |
| VfB Stuttgart vs VfL Wolfsburg | soccer | 117 / 185 | 68 | has_sportsbook_overlay |
| Villarreal vs Getafe | soccer | 111 / 173 | 62 | has_sportsbook_overlay |
| Werder Bremen vs Bayern Munich | soccer | 125 / 196 | 71 | has_sportsbook_overlay |
| AS Monaco vs Nantes | soccer | 170 / 264 | 94 | has_sportsbook_overlay |
| Bayer Leverkusen vs VfL Wolfsburg | soccer | 116 / 183 | 66 | has_sportsbook_overlay |
| Lille vs Nantes | soccer | 139 / 218 | 79 | has_sportsbook_overlay |
| Lille vs Nice | soccer | 163 / 253 | 89 | has_sportsbook_overlay |
| Napoli vs UDI | soccer | 134 / 216 | 81 | has_sportsbook_overlay |
| PAR vs Napoli | soccer | 113 / 179 | 66 | has_sportsbook_overlay |
| PAR vs ROM | soccer | 137 / 217 | 79 | has_sportsbook_overlay |
| Palermo vs Avellino | soccer | 146 / 229 | 83 | has_sportsbook_overlay |
| ROM vs SAS | soccer | 145 / 226 | 81 | has_sportsbook_overlay |
| Real Madrid vs Real Betis | soccer | 130 / 204 | 73 | has_sportsbook_overlay |
| SC Freiburg vs Bayern Munich | soccer | 118 / 187 | 68 | has_sportsbook_overlay |
| TSG Hoffenheim vs VfL Wolfsburg | soccer | 126 / 198 | 72 | has_sportsbook_overlay |
| VER vs MIL | soccer | 114 / 180 | 65 | has_sportsbook_overlay |
| Vålerenga vs Kristiansund BK total 1.5 | soccer | 1,479 / 2,238 | 2 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| 1. FC Köln vs Bayern Munich | soccer | 167 / 259 | 92 | has_sportsbook_overlay |
| AS Monaco vs Angers | soccer | 152 / 237 | 85 | has_sportsbook_overlay |
| Atlético Madrid vs Club Brugge | soccer | 149 / 233 | 84 | has_sportsbook_overlay |
| Barcelona vs Celta Vigo | soccer | 170 / 263 | 93 | has_sportsbook_overlay |
| Bayer Leverkusen vs FC St. Pauli | soccer | 121 / 190 | 68 | has_sportsbook_overlay |
| Bayern Munich vs SPO | soccer | 149 / 233 | 83 | has_sportsbook_overlay |
| Bayern Munich vs TSG Hoffenheim | soccer | 139 / 217 | 78 | has_sportsbook_overlay |
| CRE vs MIL | soccer | 101 / 160 | 59 | has_sportsbook_overlay |
| Inter Milan vs Bodø/Glimt | soccer | 167 / 263 | 96 | has_sportsbook_overlay |
| Juventus vs BOL | soccer | 157 / 246 | 89 | has_sportsbook_overlay |
| LEC vs Juventus | soccer | 159 / 248 | 89 | has_sportsbook_overlay |
| MAD vs Espanyol | soccer | 166 / 259 | 93 | has_sportsbook_overlay |

## Largest Late Starts

| Event | Sport | Start gap | First seen gap | Points | Classification |
|---|---|---:|---:|---:|---|
| Vålerenga vs Kristiansund BK total 1.5 | soccer | 7.8d | 6.2d | 2 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Knicks vs Grizzlies | basketball_nba | 5.5d | 6.5d | 287 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Wizards vs Magic | basketball_nba | 5.5d | 5.5d | 290 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| 76ers vs Nuggets | basketball_nba | 5.4d | 5.5d | 327 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Pacers vs Knicks | basketball_nba | 5.4d | 5.4d | 311 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Warriors vs Knicks | basketball_nba | 5.4d | 6.3d | 332 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Rockets vs Wizards | basketball_nba | 5.3d | 6.5d | 320 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Fredrikstad FK vs IK Start spread away-1.5 | soccer | 22.9h | 6.2d | 346 | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start, internal_quote_gap_missing_5m_api_cache, sportsbook_last_quote_not_settlement, sportsbook_end_gap_missing_5m_api_cache |
| Jazz vs Spurs | basketball_nba | 26.6m | 36.6m | 282 | has_sportsbook_overlay, sportsbook_starts_after_clob |
| Pacers vs Hornets | basketball_nba | 25.6m | 25.6m | 283 | has_sportsbook_overlay, sportsbook_starts_after_clob |
| Paris Saint Germain vs Lyon | soccer | 10.6m | 13.2h | 92 | has_sportsbook_overlay |
| Napoli vs SAS | soccer | 4.7m | -6.9h | 87 | has_sportsbook_overlay |

## Largest Internal Quote Gaps

| Event | Sport | Max gap | Cache missing | Median gap | Points |
|---|---|---:|---:|---:|---:|
| Fredrikstad FK vs IK Start spread away-1.5 | soccer | 2.6d | 493 / 753 | 15.0m | 346 |
| LEE vs Burnley | soccer | 1.3h | 0 / 15 | 5.0m | 234 |
| Ducks vs Oilers total 4.5 | icehockey_nhl | 1.2h | 0 / 14 | 5.0m | 22 |
| Suns vs Thunder | basketball_nba | 30.1m | 0 / 6 | 5.0m | 251 |
| PAR vs Juventus | soccer | 30.0m | 4 / 6 | 15.0m | 90 |
| SAS vs Inter Milan | soccer | 25.0m | 3 / 5 | 15.0m | 78 |
| RC Lens vs Nantes | soccer | 18.0m | 2 / 3 | 15.0m | 88 |
| CAG vs Juventus | soccer | 15.2m | 2 / 3 | 15.0m | 93 |
| ATA vs TOR | soccer | 15.1m | 2 / 3 | 15.0m | 94 |
| ROM vs SAS | soccer | 15.1m | 2 / 3 | 15.0m | 81 |
| Villarreal vs Alavés | soccer | 15.1m | 2 / 3 | 15.0m | 73 |
| Napoli vs SAS | soccer | 15.1m | 2 / 3 | 15.0m | 87 |

## Cited Examples

| Event | Sportsbook match | Points | Start gap | Last quote to final | Last selected fair | Notes |
|---|---|---:|---:|---:|---:|---|
| 76ers vs Nuggets | Denver Nuggets vs Philadelphia 76ers 2026-03-18T01:10:00+00:00 | 327 | 5.4d | 5.1m | 97.1% | has_sportsbook_overlay, sportsbook_event_not_listed_until_after_clob_start |
| Oilers vs Ducks total 4.5 | Anaheim Ducks vs Edmonton Oilers 2026-04-25T02:10:00+00:00 | 21 | 38s | 1.7h | 84.6% | has_sportsbook_overlay, sportsbook_last_quote_not_settlement |
