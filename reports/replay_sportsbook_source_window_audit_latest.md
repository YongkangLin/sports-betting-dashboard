# Replay Sportsbook Source Window Audit

- Generated: 2026-05-31T12:40:58.584575+00:00
- Replay events audited: 277
- Events with visible sportsbook gap windows: 123
- Gap windows audited: 8,121
- Materialization bug windows: 0
- Missing raw-cache windows: 8,105

## Verdict

- No raw-cache materialization bug was found, but some gaps still have missing 5-minute Odds API cache. Those can be backfilled if quota allows.

## Window Verdict Counts

| Verdict | Windows |
|---|---:|
| missing_raw_cache | 8,105 |
| source_event_not_listed_before_first_seen | 11 |
| mixed_source_availability | 4 |
| source_stale_payload_no_new_quote | 1 |

## Source Status Counts

| Raw source status | 5m snapshots |
|---|---:|
| missing_cache | 17,072 |
| event_not_listed_before_first_seen | 11,462 |
| stale_payload_at_or_before_gap_start | 8,123 |
| requested_point_absent | 502 |
| no_odds_event_match | 261 |
| event_not_listed | 6 |

## Events With Materialization Bugs

| Event | Sport | Windows | Statuses |
|---|---|---:|---|
| None |  | 0 |  |

## Events With Missing Raw Cache

| Event | Sport | Missing-cache windows | Statuses |
|---|---|---:|---|
| ATA vs GEN | soccer | 78 | {'stale_payload_at_or_before_gap_start': 78, 'missing_cache': 156} |
| ATA vs TOR | soccer | 82 | {'stale_payload_at_or_before_gap_start': 82, 'missing_cache': 163} |
| Angers vs Paris Saint Germain | soccer | 71 | {'stale_payload_at_or_before_gap_start': 71, 'missing_cache': 142} |
| CRE vs COM | soccer | 74 | {'stale_payload_at_or_before_gap_start': 74, 'missing_cache': 148} |
| Elche CF vs Barcelona | soccer | 83 | {'stale_payload_at_or_before_gap_start': 83, 'missing_cache': 166} |
| LAZ vs CRE | soccer | 72 | {'stale_payload_at_or_before_gap_start': 72, 'missing_cache': 143} |
| Le Havre vs Paris Saint Germain | soccer | 82 | {'stale_payload_at_or_before_gap_start': 82, 'missing_cache': 164} |
| Newcastle United vs PSV Eindhoven | soccer | 82 | {'stale_payload_at_or_before_gap_start': 82, 'missing_cache': 164} |
| Paris Saint Germain vs Lyon | soccer | 77 | {'event_not_listed_before_first_seen': 3, 'stale_payload_at_or_before_gap_start': 77, 'missing_cache': 154} |
| RB Leipzig vs Borussia Monchengladbach | soccer | 57 | {'stale_payload_at_or_before_gap_start': 57, 'missing_cache': 114} |
| ROM vs FIO | soccer | 76 | {'stale_payload_at_or_before_gap_start': 76, 'missing_cache': 152} |
| Real Madrid vs Celta Vigo | soccer | 84 | {'stale_payload_at_or_before_gap_start': 84, 'missing_cache': 168} |
| AS Monaco vs Paris Saint Germain | soccer | 84 | {'stale_payload_at_or_before_gap_start': 84, 'missing_cache': 167} |
| Atlético Madrid vs Bodø/Glimt | soccer | 83 | {'stale_payload_at_or_before_gap_start': 83, 'missing_cache': 166} |
| Bayer Leverkusen vs Arsenal | soccer | 75 | {'stale_payload_at_or_before_gap_start': 75, 'missing_cache': 149} |
| Bayern Munich vs VfB Stuttgart | soccer | 63 | {'stale_payload_at_or_before_gap_start': 63, 'missing_cache': 126} |
| CAG vs MIL | soccer | 82 | {'stale_payload_at_or_before_gap_start': 82, 'missing_cache': 164} |
| Frosinone vs Padova | soccer | 63 | {'stale_payload_at_or_before_gap_start': 63, 'missing_cache': 126} |
| GEN vs Inter Milan | soccer | 70 | {'stale_payload_at_or_before_gap_start': 70, 'missing_cache': 140} |
| Liverpool vs Galatasaray | soccer | 81 | {'stale_payload_at_or_before_gap_start': 81, 'missing_cache': 162} |
| Modena vs Carrarese | soccer | 60 | {'stale_payload_at_or_before_gap_start': 60, 'missing_cache': 119} |
| PIS vs MIL | soccer | 82 | {'stale_payload_at_or_before_gap_start': 82, 'missing_cache': 164} |
| Paris Saint Germain vs Marseille | soccer | 80 | {'stale_payload_at_or_before_gap_start': 80, 'missing_cache': 160} |
| RC Lens vs Nantes | soccer | 78 | {'stale_payload_at_or_before_gap_start': 78, 'missing_cache': 156} |
| RC Lens vs Toulouse | soccer | 78 | {'stale_payload_at_or_before_gap_start': 78, 'missing_cache': 156} |
| ROM vs GEN | soccer | 78 | {'stale_payload_at_or_before_gap_start': 78, 'missing_cache': 155} |
| Real Madrid vs Alavés | soccer | 82 | {'stale_payload_at_or_before_gap_start': 82, 'missing_cache': 163} |
| Real Madrid vs Oviedo | soccer | 83 | {'stale_payload_at_or_before_gap_start': 83, 'missing_cache': 164} |
| Venezia vs Mantova | soccer | 56 | {'stale_payload_at_or_before_gap_start': 56, 'missing_cache': 111} |
| Villarreal vs Getafe | soccer | 55 | {'stale_payload_at_or_before_gap_start': 55, 'missing_cache': 109} |
| Werder Bremen vs Bayern Munich | soccer | 62 | {'stale_payload_at_or_before_gap_start': 62, 'missing_cache': 123} |
| AS Monaco vs Nantes | soccer | 84 | {'stale_payload_at_or_before_gap_start': 84, 'missing_cache': 167} |
| Bayer Leverkusen vs VfL Wolfsburg | soccer | 56 | {'stale_payload_at_or_before_gap_start': 56, 'missing_cache': 112} |
| Lille vs Nice | soccer | 80 | {'stale_payload_at_or_before_gap_start': 80, 'missing_cache': 160} |
| Napoli vs UDI | soccer | 64 | {'stale_payload_at_or_before_gap_start': 64, 'missing_cache': 128} |
| PAR vs Napoli | soccer | 55 | {'stale_payload_at_or_before_gap_start': 55, 'missing_cache': 110} |
| PAR vs ROM | soccer | 22 | {'stale_payload_at_or_before_gap_start': 22, 'missing_cache': 44} |
| Palermo vs Avellino | soccer | 71 | {'stale_payload_at_or_before_gap_start': 71, 'missing_cache': 142} |
| ROM vs SAS | soccer | 72 | {'stale_payload_at_or_before_gap_start': 72, 'missing_cache': 143} |
| Real Madrid vs Real Betis | soccer | 63 | {'stale_payload_at_or_before_gap_start': 63, 'missing_cache': 126} |
| SC Freiburg vs Bayern Munich | soccer | 57 | {'stale_payload_at_or_before_gap_start': 57, 'missing_cache': 114} |
| TSG Hoffenheim vs VfL Wolfsburg | soccer | 62 | {'stale_payload_at_or_before_gap_start': 62, 'missing_cache': 123} |
| VER vs MIL | soccer | 55 | {'stale_payload_at_or_before_gap_start': 55, 'missing_cache': 110} |
| Vålerenga vs Kristiansund BK total 1.5 | soccer | 1 | {'event_not_listed_before_first_seen': 1800, 'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 291, 'requested_point_absent': 145} |
| 1. FC Köln vs Bayern Munich | soccer | 82 | {'stale_payload_at_or_before_gap_start': 82, 'missing_cache': 164} |
| AS Monaco vs Angers | soccer | 74 | {'stale_payload_at_or_before_gap_start': 74, 'missing_cache': 148} |
| Atlético Madrid vs Club Brugge | soccer | 73 | {'stale_payload_at_or_before_gap_start': 73, 'missing_cache': 146} |
| Barcelona vs Celta Vigo | soccer | 83 | {'stale_payload_at_or_before_gap_start': 83, 'missing_cache': 166} |
| Bayer Leverkusen vs FC St. Pauli | soccer | 60 | {'stale_payload_at_or_before_gap_start': 60, 'missing_cache': 119} |
| Bayern Munich vs SPO | soccer | 73 | {'stale_payload_at_or_before_gap_start': 73, 'missing_cache': 146} |
| Bayern Munich vs TSG Hoffenheim | soccer | 68 | {'stale_payload_at_or_before_gap_start': 68, 'missing_cache': 136} |
| CRE vs MIL | soccer | 50 | {'stale_payload_at_or_before_gap_start': 50, 'missing_cache': 99} |
| Inter Milan vs Bodø/Glimt | soccer | 82 | {'stale_payload_at_or_before_gap_start': 82, 'missing_cache': 164} |
| Juventus vs BOL | soccer | 76 | {'stale_payload_at_or_before_gap_start': 76, 'missing_cache': 152} |
| LEC vs Juventus | soccer | 79 | {'stale_payload_at_or_before_gap_start': 79, 'missing_cache': 157} |
| MAD vs Espanyol | soccer | 81 | {'stale_payload_at_or_before_gap_start': 81, 'missing_cache': 162} |
| Manchester City vs Galatasaray | soccer | 83 | {'stale_payload_at_or_before_gap_start': 83, 'missing_cache': 166} |
| Marseille vs Auxerre | soccer | 83 | {'stale_payload_at_or_before_gap_start': 83, 'missing_cache': 165} |
| RB Leipzig vs Union Berlin | soccer | 75 | {'stale_payload_at_or_before_gap_start': 75, 'missing_cache': 150} |
| Real Sociedad vs Oviedo | soccer | 55 | {'stale_payload_at_or_before_gap_start': 55, 'missing_cache': 110} |
| SAS vs Inter Milan | soccer | 68 | {'stale_payload_at_or_before_gap_start': 68, 'missing_cache': 137, 'event_not_listed': 1} |
| TOR vs Inter Milan | soccer | 67 | {'stale_payload_at_or_before_gap_start': 67, 'missing_cache': 134} |
| TOR vs Juventus | soccer | 78 | {'stale_payload_at_or_before_gap_start': 78, 'missing_cache': 156} |
| Tottenham Hotspur vs Slavia Praha | soccer | 81 | {'stale_payload_at_or_before_gap_start': 81, 'missing_cache': 162} |
| VER vs Napoli | soccer | 71 | {'stale_payload_at_or_before_gap_start': 71, 'missing_cache': 142} |
| Villarreal vs Alavés | soccer | 64 | {'stale_payload_at_or_before_gap_start': 64, 'missing_cache': 127} |
| ATA vs PAR | soccer | 58 | {'stale_payload_at_or_before_gap_start': 58, 'missing_cache': 116} |
| Barcelona vs Villarreal | soccer | 64 | {'stale_payload_at_or_before_gap_start': 64, 'missing_cache': 128} |
| Bayern Munich vs Atalanta BC | soccer | 81 | {'stale_payload_at_or_before_gap_start': 81, 'missing_cache': 162} |
| Borussia Dortmund vs SC Freiburg | soccer | 64 | {'stale_payload_at_or_before_gap_start': 64, 'missing_cache': 128} |
| Club Brugge vs Arsenal | soccer | 82 | {'stale_payload_at_or_before_gap_start': 82, 'missing_cache': 163} |
| Elche CF vs Barcelona | soccer | 83 | {'stale_payload_at_or_before_gap_start': 83, 'missing_cache': 166} |
| FC St. Pauli vs Bayern Munich | soccer | 66 | {'stale_payload_at_or_before_gap_start': 66, 'missing_cache': 132} |
| Inter Milan vs BOL | soccer | 81 | {'stale_payload_at_or_before_gap_start': 81, 'missing_cache': 162} |
| LEC vs Inter Milan | soccer | 70 | {'stale_payload_at_or_before_gap_start': 70, 'missing_cache': 140} |
| MIL vs SAS | soccer | 49 | {'stale_payload_at_or_before_gap_start': 49, 'missing_cache': 98} |
| Mallorca vs Oviedo | soccer | 79 | {'stale_payload_at_or_before_gap_start': 79, 'missing_cache': 158} |
| Metz vs AS Monaco | soccer | 70 | {'stale_payload_at_or_before_gap_start': 70, 'missing_cache': 140} |
| PAR vs Juventus | soccer | 80 | {'stale_payload_at_or_before_gap_start': 80, 'missing_cache': 162, 'event_not_listed': 1} |
| PIS vs Juventus | soccer | 82 | {'stale_payload_at_or_before_gap_start': 82, 'missing_cache': 164} |

## Cited Examples

| Event | Sport | Windows | Verdicts | Statuses |
|---|---|---:|---|---|
| Oilers vs Ducks total 4.5 | icehockey_nhl | 1 | {'mixed_source_availability': 1} | {'stale_payload_at_or_before_gap_start': 1, 'requested_point_absent': 19} |
| 76ers vs Nuggets | basketball_nba | 1 | {'source_event_not_listed_before_first_seen': 1} | {'event_not_listed_before_first_seen': 1568} |

## Largest Gap Windows

| Event | Type | Duration | Verdict | Statuses |
|---|---|---:|---|---|
| Vålerenga vs Kristiansund BK total 1.5 | early_gap_before_event_first_seen | 6.2d | source_event_not_listed_before_first_seen | {'event_not_listed_before_first_seen': 1800} |
| Knicks vs Grizzlies | early_gap_before_event_first_seen | 5.5d | source_event_not_listed_before_first_seen | {'event_not_listed_before_first_seen': 1590} |
| Wizards vs Magic | early_gap_before_event_first_seen | 5.5d | source_event_not_listed_before_first_seen | {'event_not_listed_before_first_seen': 1570} |
| 76ers vs Nuggets | early_gap_before_event_first_seen | 5.4d | source_event_not_listed_before_first_seen | {'event_not_listed_before_first_seen': 1568} |
| Pacers vs Knicks | early_gap_before_event_first_seen | 5.4d | source_event_not_listed_before_first_seen | {'event_not_listed_before_first_seen': 1555} |
| Warriors vs Knicks | early_gap_before_event_first_seen | 5.4d | source_event_not_listed_before_first_seen | {'event_not_listed_before_first_seen': 1549} |
| Rockets vs Wizards | early_gap_before_event_first_seen | 5.3d | source_event_not_listed_before_first_seen | {'event_not_listed_before_first_seen': 1540} |
| Fredrikstad FK vs IK Start spread away-1.5 | internal_gap_between_sportsbook_quotes | 2.6d | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 493, 'requested_point_absent': 259} |
| Vålerenga vs Kristiansund BK total 1.5 | early_gap_before_first_sportsbook_quote | 1.5d | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 291, 'requested_point_absent': 145} |
| Fredrikstad FK vs IK Start spread away-1.5 | early_gap_before_event_first_seen | 22.9h | source_event_not_listed_before_first_seen | {'event_not_listed_before_first_seen': 275} |
| Barcelona vs Bayern Munich | no_sportsbook_overlay | 21.7h | mixed_source_availability | {'no_odds_event_match': 261} |
| Fredrikstad FK vs IK Start spread away-1.5 | internal_gap_between_sportsbook_quotes | 9.8h | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 76, 'requested_point_absent': 40} |
| Fredrikstad FK vs IK Start spread away-1.5 | late_gap_after_last_sportsbook_quote | 2.8h | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 21, 'requested_point_absent': 12} |
| Oilers vs Ducks total 4.5 | late_gap_after_last_sportsbook_quote | 1.7h | mixed_source_availability | {'stale_payload_at_or_before_gap_start': 1, 'requested_point_absent': 19} |
| LEE vs Burnley | internal_gap_between_sportsbook_quotes | 1.3h | source_stale_payload_no_new_quote | {'stale_payload_at_or_before_gap_start': 15} |
| Ducks vs Oilers total 4.5 | internal_gap_between_sportsbook_quotes | 1.2h | mixed_source_availability | {'stale_payload_at_or_before_gap_start': 1, 'requested_point_absent': 13} |
| Hamburger SV vs Bayern Munich | late_gap_after_last_sportsbook_quote | 1.1h | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 7, 'event_not_listed': 4} |
| Fredrikstad FK vs IK Start spread away-1.5 | internal_gap_between_sportsbook_quotes | 60.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 8, 'requested_point_absent': 3} |
| Ducks vs Oilers total 4.5 | late_gap_after_last_sportsbook_quote | 44.4m | mixed_source_availability | {'stale_payload_at_or_before_gap_start': 1, 'requested_point_absent': 8} |
| Fredrikstad FK vs IK Start spread away-1.5 | internal_gap_between_sportsbook_quotes | 30.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 4, 'requested_point_absent': 1} |
| PAR vs Juventus | internal_gap_between_sportsbook_quotes | 30.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 4, 'event_not_listed': 1} |
| Fredrikstad FK vs IK Start spread away-1.5 | internal_gap_between_sportsbook_quotes | 30.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 4, 'requested_point_absent': 1} |
| Fredrikstad FK vs IK Start spread away-1.5 | internal_gap_between_sportsbook_quotes | 30.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 4, 'requested_point_absent': 1} |
| Jazz vs Spurs | early_gap_before_event_first_seen | 26.6m | source_event_not_listed_before_first_seen | {'event_not_listed_before_first_seen': 6} |
| Pacers vs Hornets | early_gap_before_event_first_seen | 25.6m | source_event_not_listed_before_first_seen | {'event_not_listed_before_first_seen': 6} |
| SAS vs Inter Milan | internal_gap_between_sportsbook_quotes | 25.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 3, 'event_not_listed': 1} |
| RC Lens vs Nantes | internal_gap_between_sportsbook_quotes | 18.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| RC Lens vs Nantes | internal_gap_between_sportsbook_quotes | 15.5m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| ATA vs TOR | internal_gap_between_sportsbook_quotes | 15.1m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| ROM vs SAS | internal_gap_between_sportsbook_quotes | 15.1m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Villarreal vs Alavés | internal_gap_between_sportsbook_quotes | 15.1m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| MAD vs Espanyol | internal_gap_between_sportsbook_quotes | 15.1m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Real Sociedad vs Oviedo | internal_gap_between_sportsbook_quotes | 15.1m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| LEC vs Inter Milan | internal_gap_between_sportsbook_quotes | 15.1m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Bayern Munich vs SPO | internal_gap_between_sportsbook_quotes | 15.1m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Tottenham Hotspur vs Slavia Praha | internal_gap_between_sportsbook_quotes | 15.1m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| ATA vs TOR | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| ATA vs TOR | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| ATA vs TOR | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| CRE vs COM | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Elche CF vs Barcelona | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| LAZ vs CRE | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Le Havre vs Paris Saint Germain | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Newcastle United vs PSV Eindhoven | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| ROM vs FIO | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Real Madrid vs Celta Vigo | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Atlético Madrid vs Bodø/Glimt | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| CAG vs MIL | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Frosinone vs Padova | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Frosinone vs Padova | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Frosinone vs Padova | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| PIS vs MIL | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| RC Lens vs Nantes | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| RC Lens vs Toulouse | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| RC Lens vs Toulouse | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| ROM vs GEN | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Real Madrid vs Oviedo | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Venezia vs Mantova | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Venezia vs Mantova | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Villarreal vs Getafe | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Villarreal vs Getafe | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Villarreal vs Getafe | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| AS Monaco vs Nantes | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Napoli vs UDI | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| PAR vs Napoli | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Palermo vs Avellino | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Palermo vs Avellino | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Palermo vs Avellino | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| ROM vs SAS | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| ROM vs SAS | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| TSG Hoffenheim vs VfL Wolfsburg | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| TSG Hoffenheim vs VfL Wolfsburg | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| 1. FC Köln vs Bayern Munich | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| AS Monaco vs Angers | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Atlético Madrid vs Club Brugge | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Atlético Madrid vs Club Brugge | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Atlético Madrid vs Club Brugge | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Atlético Madrid vs Club Brugge | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Barcelona vs Celta Vigo | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
| Inter Milan vs Bodø/Glimt | internal_gap_between_sportsbook_quotes | 15.0m | missing_raw_cache | {'stale_payload_at_or_before_gap_start': 1, 'missing_cache': 2} |
