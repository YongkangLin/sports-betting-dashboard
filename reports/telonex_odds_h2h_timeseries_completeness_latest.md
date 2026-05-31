# Telonex + Odds H2H Time-Series Completeness

- Generated: 2026-05-31T16:10:02.868001+00:00
- Target assets: 10,000
- Source-complete assets: 1,793 (17.9%)
- Target markets: 5,000
- Source-complete markets: 890 (17.8%)
- Polymarket book rows: 197,544,975
- Polymarket trade rows: 3,759,458
- Sportsbook quote rows: 55,740,114
- Sportsbook snapshots: 676,684
- Zero-row source files: 0

## By Sport

| Sport | Markets | Complete | Complete rate | Polymarket book rows | Sportsbook quote rows |
|---|---:|---:|---:|---:|---:|
| soccer | 4,308 | 238 | 5.5% | 26,923,773 | 26,765,349 |
| basketball_nba | 269 | 256 | 95.2% | 89,936,657 | 520,362 |
| icehockey_nhl | 249 | 249 | 100.0% | 52,357,142 | 181,494 |
| americanfootball_nfl | 80 | 69 | 86.2% | 10,247,289 | 378,264 |
| basketball_wnba | 60 | 60 | 100.0% | 14,048,112 | 13,132 |
| baseball_mlb | 34 | 18 | 52.9% | 4,032,002 | 11,456 |

## Granularity

- book_snapshot_5 top-5 CLOB snapshots; model labels are materialized on a 60-second grid from this source.
- Odds API snapshots are point-in-time quotes, joined backward onto the model grid with quote_age recorded. Do not treat forward-filled sportsbook rows as independent minute observations.
