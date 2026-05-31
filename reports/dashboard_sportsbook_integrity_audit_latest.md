# Dashboard Sportsbook Integrity Audit

- Generated: 2026-05-31T18:21:31.157440+00:00
- Replay events audited: 277
- Polymarket one-minute CLOB complete: 277 / 277
- Sportsbook event matches: 276 / 277
- Sportsbook overlays with complete side math: 276 / 277
- Polymarket actual two-sided CLOB events: 277 / 277
- Complete on both Polymarket CLOB and sportsbook side math: 276 / 277
- Sportsbook timestamps inside the plotted CLOB replay window: 276 / 276
- Raw 15-minute Odds cache complete: 276 / 276
- Native 5-minute Odds cache complete: 167 / 276
- Events with visible sportsbook gaps over 10 minutes: 120
- Visible gap windows audited: 8,063
- Visible gap windows caused by missing raw 5-minute cache: 8,047
- Raw complete-line materialization bugs: 0
- Unique missing native 5-minute snapshots: 14,224
- Estimated credits to finish all missing native 5-minute snapshots: 1,280,160
- Paid Odds API credits remaining locally: 126
- By-sport missing snapshot counts below are per-event sums; unique cache snapshots are lower because multiple replay events can share the same sport/timestamp API response.

## Verdict

- No replay materialization bug was found. Some visible sportsbook gaps are real missing native 5-minute cache and can only be reduced by more Odds API backfill.
- The random-looking sportsbook breaks are not all the same thing: most current long gap windows are missing raw 5-minute cache, while a smaller set are legitimate source behavior such as Odds API listing the event late or no longer offering the exact total/spread point.
- Sportsbook lines are quote series, not settlement series. They should not be forced to end at 0/100 when books stop offering a line or change a total/spread point.
- Timestamp alignment passes at the replay boundary: sportsbook points that are plotted are inside the same UTC window as the Polymarket CLOB series.

## Event Categories

| Category | Events | Meaning |
|---|---:|---|
| complete_or_no_large_gap | 157 | No visible gap beyond normal quote cadence. |
| missing_native_5m_cache | 108 | Backfillable 5-minute Odds API snapshots are missing. |
| source_event_not_listed_yet | 8 | The source did not list the event until after the CLOB opened. |
| source_market_or_point_absent | 2 | Raw source exists, but the requested market/point is absent. |
| no_odds_event_match | 1 | No Odds API event match. |
| source_stale_or_no_new_quote | 1 | Raw source exists, but no fresh quote is available. |

## By Sport

| Sport | Events | Matched | Overlay | Complete 5m cache | Missing 5m snapshots | Materialization bugs |
|---|---:|---:|---:|---:|---:|---:|
| americanfootball_nfl | 9 | 9 | 9 | 9 | 0 | 0 |
| basketball_nba | 89 | 89 | 89 | 88 | 1 | 0 |
| basketball_wnba | 2 | 2 | 2 | 2 | 0 | 0 |
| icehockey_nhl | 2 | 2 | 2 | 2 | 0 | 0 |
| soccer | 175 | 174 | 174 | 66 | 18,668 | 0 |

## Sportsbook Quote End Checks

| Check | Events | Meaning |
|---|---:|---|
| Last sportsbook quote more than 10m before Polymarket listed close | 2 | Book stopped offering a complete usable line before the listed market close/start timestamp. Do not force-fill past this point. |
| Last sportsbook quote more than 1h before Polymarket listed close | 1 | Large late gap; check source status before using this interval for model labels. |
| Last sportsbook quote after Polymarket listed close | 274 | The source still had quotes after Polymarket's listed close/start timestamp, usually because live/pre-final quote windows differ by venue. |
| Last sportsbook quote more than 10m before Polymarket final/settlement | 4 | The sportsbook source stopped before the replay's final settlement timestamp. This is expected when books suspend/remove lines. |
| Last sportsbook quote more than 1h before Polymarket final/settlement | 3 | Large gap to settlement; do not treat the last sportsbook quote as a game-ending probability. |
| Last sportsbook quote after Polymarket final/settlement | 0 | Unexpected timing edge case if nonzero; inspect before using these rows. |
| Last sportsbook fair probability was non-terminal | 179 | Expected: sportsbook odds are quotes, not settlement prices, so they do not need to end at 0/100. |

## Checked Examples

| Event | Verdict | Points | Start gap | Max internal gap | Last quote to final | Detail |
|---|---|---:|---:|---:|---:|---|
| 76ers vs Nuggets | source_event_not_listed_yet | 327 | 5.4d | 5.1m | 5.1m | Odds event first seen 2026-03-17T00:55:38+00:00; pre-listing CLOB window is not backfillable. |
| Barcelona vs Bayern Munich | no_odds_event_match | 0 | -- | -- | -- | No matching Odds API event was found, so no sportsbook overlay can be trusted. |
| Ducks vs Oilers total 4.5 | source_market_or_point_absent | 22 | 47s | 1.2h | 44.6m | Raw cache is present; requested 4.5 total is absent/stale in the gap window. |
| Oilers vs Ducks total 4.5 | source_market_or_point_absent | 21 | 38s | 5.0m | 1.7h | Raw cache is present; requested 4.5 total is absent/stale in the gap window. |

## Largest Backfillable Native 5m Gaps

| Event | Sport | Missing / Expected 5m snapshots | Category |
|---|---|---:|---|
| Vålerenga vs Kristiansund BK total 1.5 | soccer | 1,479 / 2,238 | missing_native_5m_cache |
| Fredrikstad FK vs IK Start spread away-1.5 | soccer | 1,471 / 2,226 | missing_native_5m_cache |
| Real Madrid vs Celta Vigo | soccer | 171 / 264 | missing_native_5m_cache |
| AS Monaco vs Nantes | soccer | 170 / 264 | missing_native_5m_cache |
| Barcelona vs Celta Vigo | soccer | 170 / 263 | missing_native_5m_cache |
| Girona vs Barcelona | soccer | 170 / 264 | missing_native_5m_cache |
| Elche CF vs Barcelona | soccer | 169 / 263 | missing_native_5m_cache |
| Le Havre vs Paris Saint Germain | soccer | 169 / 264 | missing_native_5m_cache |
| AS Monaco vs Paris Saint Germain | soccer | 169 / 263 | missing_native_5m_cache |
| Atlético Madrid vs Bodø/Glimt | soccer | 169 / 265 | missing_native_5m_cache |
| Manchester City vs Galatasaray | soccer | 169 / 263 | missing_native_5m_cache |
| Elche CF vs Barcelona | soccer | 169 / 262 | missing_native_5m_cache |
| Real Madrid vs Real Sociedad | soccer | 169 / 263 | missing_native_5m_cache |
| Slavia Praha vs Barcelona | soccer | 169 / 262 | missing_native_5m_cache |
| Paris Saint Germain vs AS Monaco | soccer | 169 / 263 | missing_native_5m_cache |
| Borussia Dortmund vs Bodø/Glimt | soccer | 168 / 263 | missing_native_5m_cache |
| Villarreal vs Ajax | soccer | 168 / 264 | missing_native_5m_cache |
| BOL vs CRE | soccer | 168 / 261 | missing_native_5m_cache |
| Newcastle United vs PSV Eindhoven | soccer | 167 / 259 | missing_native_5m_cache |
| CAG vs MIL | soccer | 167 / 260 | missing_native_5m_cache |
| PIS vs MIL | soccer | 167 / 260 | missing_native_5m_cache |
| 1. FC Köln vs Bayern Munich | soccer | 167 / 259 | missing_native_5m_cache |
| Inter Milan vs Bodø/Glimt | soccer | 167 / 263 | missing_native_5m_cache |
| Marseille vs Auxerre | soccer | 167 / 259 | missing_native_5m_cache |
| PIS vs Juventus | soccer | 167 / 260 | missing_native_5m_cache |
| Nice vs Paris Saint Germain | soccer | 167 / 259 | missing_native_5m_cache |
| ATA vs TOR | soccer | 166 / 260 | missing_native_5m_cache |
| Real Madrid vs Alavés | soccer | 166 / 258 | missing_native_5m_cache |
| MAD vs Espanyol | soccer | 166 / 259 | missing_native_5m_cache |
| Tottenham Hotspur vs Slavia Praha | soccer | 166 / 259 | missing_native_5m_cache |
