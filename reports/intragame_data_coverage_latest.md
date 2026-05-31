# Intragame Trading Data Coverage

This audit checks the partitioned fact store for post-commence price rows. It also checks Telonex historical CLOB coverage. Telonex can certify public bid/ask/depth/trade presence, but not private fills or queue position.

## Source Summary

| Source | Rows | Events | Post-start rows | Post-start events | Event coverage |
|---|---:|---:|---:|---:|---:|
| odds_api | 46,928,535 | 5,068 | 3,671,454 | 4,001 | 78.9% |
| polymarket | 112,446,925 | 4,992 | 18,782,009 | 4,992 | 100.0% |

## Telonex Historical CLOB

| Files | Rows | Quote rows | Depth rows | Trade rows | Depth files | Date span |
|---:|---:|---:|---:|---:|---:|---|
| 4,437 | 41,463,175 | 6,719,183 | 34,575,311 | 168,681 | 1,745 | n/a to n/a |

## Interpretation

- Current data can draw a proxy Polymarket price path and compare it with the model fair value.
- Telonex is the canonical historical executable quote/depth/trade source for LEV/convergence labels.
- Current data still cannot prove a live trading bot end-to-end because it has no authenticated private order lifecycle, actual fills, true queue-ahead, or realized market impact from our orders.
- Odds API rows after commence are only useful if they represent true live/in-play snapshots; this audit measures their presence, not bookmaker coverage quality.

## Top Post-start Segments

| Source | Sport | Market | Rows | Events | Post-start events | Coverage |
|---|---|---|---:|---:|---:|---:|
| polymarket | icehockey_nhl | h2h | 8,776,950 | 1,386 | 1,386 | 100.0% |
| polymarket | basketball_nba | h2h | 8,056,285 | 1,270 | 1,270 | 100.0% |
| polymarket | basketball_nba | totals | 14,380,453 | 960 | 960 | 100.0% |
| polymarket | basketball_nba | spreads | 13,591,229 | 904 | 904 | 100.0% |
| polymarket | baseball_mlb | h2h | 5,243,419 | 835 | 835 | 100.0% |
| polymarket | baseball_mlb | spreads | 5,824,347 | 811 | 811 | 100.0% |
| polymarket | icehockey_nhl | spreads | 4,249,469 | 793 | 793 | 100.0% |
| polymarket | baseball_mlb | totals | 7,344,161 | 792 | 792 | 100.0% |
| polymarket | icehockey_nhl | totals | 13,963,183 | 784 | 784 | 100.0% |
| polymarket | soccer_epl | h2h | 2,174,775 | 227 | 227 | 100.0% |
| polymarket | soccer_italy_serie_a | h2h | 1,991,434 | 208 | 208 | 100.0% |
| polymarket | soccer_spain_la_liga | h2h | 1,771,075 | 185 | 185 | 100.0% |
| polymarket | soccer_germany_bundesliga | h2h | 1,528,204 | 160 | 160 | 100.0% |
| polymarket | soccer_france_ligue_one | h2h | 1,314,091 | 137 | 137 | 100.0% |
| polymarket | soccer_brazil_campeonato | h2h | 984,423 | 103 | 103 | 100.0% |
| polymarket | americanfootball_nfl | h2h | 667,933 | 104 | 103 | 99.0% |
| polymarket | americanfootball_nfl | totals | 14,384,543 | 91 | 91 | 100.0% |
| polymarket | americanfootball_nfl | spreads | 2,965,968 | 89 | 88 | 98.9% |
| polymarket | soccer_uefa_champs_league | h2h | 738,050 | 77 | 77 | 100.0% |
| polymarket | tennis_atp_french_open | h2h | 662,988 | 55 | 55 | 100.0% |
| polymarket | tennis_wta_french_open | h2h | 641,452 | 53 | 53 | 100.0% |
| polymarket | basketball_wnba | h2h | 329,164 | 53 | 53 | 100.0% |
| polymarket | soccer_conmebol_copa_libertadores | h2h | 436,855 | 46 | 46 | 100.0% |
| polymarket | soccer_italy_serie_b | h2h | 279,445 | 29 | 29 | 100.0% |
| polymarket | baseball_kbo | h2h | 127,919 | 20 | 20 | 100.0% |
| polymarket | mma_mixed_martial_arts | h2h | 12,908 | 2 | 2 | 100.0% |
| polymarket | boxing_boxing | h2h | 6,202 | 1 | 1 | 100.0% |
| odds_api | icehockey_nhl | h2h | 10,079,021 | 1,386 | 1,091 | 78.7% |
| odds_api | icehockey_nhl | h2h_lay | 544,688 | 1,386 | 1,091 | 78.7% |
| odds_api | icehockey_nhl | totals | 2,272,852 | 1,386 | 1,082 | 78.1% |
| odds_api | icehockey_nhl | spreads | 1,965,700 | 1,386 | 1,082 | 78.1% |
| odds_api | basketball_nba | h2h | 6,219,152 | 1,311 | 1,062 | 81.0% |
| odds_api | basketball_nba | h2h_lay | 528,320 | 1,311 | 1,061 | 80.9% |
| odds_api | basketball_nba | totals | 1,937,612 | 1,311 | 1,056 | 80.5% |
| odds_api | basketball_nba | spreads | 1,561,644 | 1,311 | 1,056 | 80.5% |
| odds_api | baseball_mlb | h2h | 4,131,110 | 841 | 737 | 87.6% |
| odds_api | baseball_mlb | h2h_lay | 354,040 | 840 | 737 | 87.7% |
| odds_api | baseball_mlb | totals | 1,412,448 | 841 | 735 | 87.4% |
| odds_api | baseball_mlb | spreads | 1,353,640 | 841 | 735 | 87.4% |
| odds_api | soccer_italy_serie_a | h2h | 1,481,557 | 223 | 216 | 96.9% |
