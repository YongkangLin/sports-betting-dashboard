# Odds API Replay-Aligned Snapshot Pull

- Generated: 2026-05-31T10:06:02.075686+00:00
- Replay manifest: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/execution_training/favorite_longshot_event_replays_latest.json`
- Step minutes: 5
- Markets: h2h,spreads,totals
- Regions: us,uk,eu
- Workers: 24
- Dry run: False
- Planned snapshots: 29,535
- Cached before run: 16,908
- Attempted: 29,535
- Successful: 14,225
- Empty: 0
- Failed: 15,310
- Warehouse events/quotes returned: 0 / 0
- Quota after: `{'paid:df93': {'remaining': 97866, 'used': 4902134}}`

## Plan By Sport

| Sport | Replay events | Snapshots | Cached | Success | Empty | Failed | Events | Quotes |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| americanfootball_nfl | 9 | 887 | 503 | 887 | 0 | 0 | 17,104 | 2,809,294 |
| basketball_nba | 89 | 6,556 | 3,878 | 6,555 | 0 | 1 | 64,841 | 11,954,118 |
| basketball_wnba | 2 | 52 | 43 | 52 | 0 | 0 | 302 | 41,696 |
| icehockey_nhl | 2 | 46 | 40 | 46 | 0 | 0 | 375 | 68,354 |
| soccer_brazil_campeonato | 11 | 1,420 | 795 | 1,420 | 0 | 0 | 25,625 | 4,212,042 |
| soccer_conmebol_copa_libertadores | 7 | 1,127 | 630 | 1,127 | 0 | 0 | 23,586 | 2,854,541 |
| soccer_epl | 31 | 3,305 | 1,887 | 3,305 | 0 | 0 | 64,797 | 12,013,149 |
| soccer_france_ligue_one | 23 | 3,213 | 1,824 | 833 | 0 | 2,380 | 13,049 | 2,158,035 |
| soccer_germany_bundesliga | 20 | 2,275 | 1,304 | 0 | 0 | 2,275 | 0 | 0 |
| soccer_italy_serie_a | 38 | 4,417 | 2,549 | 0 | 0 | 4,417 | 0 | 0 |
| soccer_italy_serie_b | 5 | 493 | 286 | 0 | 0 | 493 | 0 | 0 |
| soccer_norway_eliteserien | 2 | 1,481 | 761 | 0 | 0 | 1,481 | 0 | 0 |
| soccer_spain_la_liga | 18 | 2,461 | 1,384 | 0 | 0 | 2,461 | 0 | 0 |
| soccer_uefa_champs_league | 19 | 1,802 | 1,024 | 0 | 0 | 1,802 | 0 | 0 |

## Errors

- `basketball_nba` `2026-02-25T03:35:00Z`: HTTPSConnectionPool(host='api.the-odds-api.com', port=443): Max retries exceeded with url: /v4/historical/sports/basketball_nba/odds?date=2026-02-25T03%3A35%3A00Z&markets=h2h%2Cspreads%2Ctotals&regions=us%2Cuk%2Ceu&oddsFormat=american&apiKey=<redacted> (Caused by NameResolution
- `soccer_france_ligue_one` `2026-01-30T12:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T12:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T12:55:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T13:05:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T13:10:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T13:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T13:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T13:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T13:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T14:05:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T13:55:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T14:10:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T14:20:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T14:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T14:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T14:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T14:55:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T15:05:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T14:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T15:10:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T15:20:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T15:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T15:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T15:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T15:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T16:05:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T16:10:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T15:55:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T16:20:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T16:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T16:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T16:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T16:55:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T16:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T17:10:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T17:05:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T17:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T17:20:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T17:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T17:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99486, 'used': 4900514}
- `soccer_france_ligue_one` `2026-01-30T17:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T18:10:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T18:05:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99486, 'used': 4900514}
- `soccer_france_ligue_one` `2026-01-30T18:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99486, 'used': 4900514}
- `soccer_france_ligue_one` `2026-01-30T17:55:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T18:20:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T18:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99486, 'used': 4900514}
- `soccer_france_ligue_one` `2026-01-30T18:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99666, 'used': 4900334}
- `soccer_france_ligue_one` `2026-01-30T18:55:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T18:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99576, 'used': 4900424}
- `soccer_france_ligue_one` `2026-01-30T19:05:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T19:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99576, 'used': 4900424}
- `soccer_france_ligue_one` `2026-01-30T19:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T19:10:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99486, 'used': 4900514}
- `soccer_france_ligue_one` `2026-01-30T19:20:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99666, 'used': 4900334}
- `soccer_france_ligue_one` `2026-01-30T19:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T19:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99576, 'used': 4900424}
- `soccer_france_ligue_one` `2026-01-30T19:55:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T20:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-01-30T20:10:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99666, 'used': 4900334}
- `soccer_france_ligue_one` `2026-01-30T20:20:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T20:05:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99486, 'used': 4900514}
- `soccer_france_ligue_one` `2026-01-30T20:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99576, 'used': 4900424}
- `soccer_france_ligue_one` `2026-01-30T20:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99666, 'used': 4900334}
- `soccer_france_ligue_one` `2026-01-30T20:55:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T21:05:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99486, 'used': 4900514}
- `soccer_france_ligue_one` `2026-01-30T21:10:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99576, 'used': 4900424}
- `soccer_france_ligue_one` `2026-01-30T20:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-02-08T00:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99396, 'used': 4900604}
- `soccer_france_ligue_one` `2026-01-30T21:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-01-30T21:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99486, 'used': 4900514}
- `soccer_france_ligue_one` `2026-01-30T21:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99756, 'used': 4900244}
- `soccer_france_ligue_one` `2026-02-08T00:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99576, 'used': 4900424}
- `soccer_france_ligue_one` `2026-02-08T00:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-02-08T01:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-02-08T00:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99396, 'used': 4900604}
- `soccer_france_ligue_one` `2026-02-08T00:55:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-02-08T01:10:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99486, 'used': 4900514}
- `soccer_france_ligue_one` `2026-02-08T01:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99576, 'used': 4900424}
- `soccer_france_ligue_one` `2026-01-30T21:20:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99666, 'used': 4900334}
- `soccer_france_ligue_one` `2026-02-08T01:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-02-08T01:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99396, 'used': 4900604}
- `soccer_france_ligue_one` `2026-02-08T01:55:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-02-08T02:05:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99486, 'used': 4900514}
- `soccer_france_ligue_one` `2026-02-08T02:10:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99576, 'used': 4900424}
- `soccer_france_ligue_one` `2026-02-08T02:20:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99666, 'used': 4900334}
- `soccer_france_ligue_one` `2026-02-08T02:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-02-08T01:20:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99756, 'used': 4900244}
- `soccer_france_ligue_one` `2026-02-08T02:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99396, 'used': 4900604}
- `soccer_france_ligue_one` `2026-02-08T02:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-02-08T02:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99486, 'used': 4900514}
- `soccer_france_ligue_one` `2026-02-08T02:55:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99576, 'used': 4900424}
- `soccer_france_ligue_one` `2026-02-08T03:05:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99666, 'used': 4900334}
- `soccer_france_ligue_one` `2026-02-08T03:20:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99756, 'used': 4900244}
- `soccer_france_ligue_one` `2026-02-08T03:25:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99396, 'used': 4900604}
- `soccer_france_ligue_one` `2026-02-08T03:35:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99846, 'used': 4900154}
- `soccer_france_ligue_one` `2026-02-08T03:40:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99486, 'used': 4900514}
- `soccer_france_ligue_one` `2026-02-08T03:10:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99936, 'used': 4900064}
- `soccer_france_ligue_one` `2026-02-08T03:50:00Z`: paid Odds API remaining below stop threshold: {'remaining': 99576, 'used': 4900424}
