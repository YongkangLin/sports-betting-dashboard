# Telonex + Odds H2H Time-Series Completeness

- Generated: 2026-05-31T17:25:47.762618+00:00
- Target assets: 10,000
- Source-complete assets: 2,531 (25.3%)
- Target markets: 5,000
- Source-complete markets: 1,265 (25.3%)
- Polymarket book rows: 222,687,557
- Polymarket trade rows: 4,291,970
- Sportsbook quote rows: 55,740,114
- Sportsbook snapshots: 676,684
- Zero-row source files: 0

## By Sport

| Sport | Markets | Complete | Complete rate | Polymarket book rows | Sportsbook quote rows |
|---|---:|---:|---:|---:|---:|
| soccer | 4,308 | 581 | 13.5% | 48,312,589 | 26,765,349 |
| basketball_nba | 269 | 267 | 99.3% | 91,187,264 | 520,362 |
| icehockey_nhl | 249 | 249 | 100.0% | 52,357,142 | 181,494 |
| americanfootball_nfl | 80 | 80 | 100.0% | 12,066,606 | 378,264 |
| basketball_wnba | 60 | 60 | 100.0% | 14,048,112 | 13,132 |
| baseball_mlb | 34 | 28 | 82.4% | 4,715,844 | 11,456 |

## Granularity

- book_snapshot_5 top-5 CLOB snapshots; model labels are materialized on a 60-second grid from this source.
- Odds API snapshots are point-in-time quotes, joined backward onto the model grid with quote_age recorded. Do not treat forward-filled sportsbook rows as independent minute observations.
