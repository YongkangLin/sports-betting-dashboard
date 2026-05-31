# Telonex + Odds H2H Target Plan

- Generated: 2026-05-31T14:49:48.112759+00:00
- Eligible H2H assets with CLOB/trades: 71,358
- Eligible H2H markets: 35,679
- Matched target assets: 10,000
- Matched target markets: 5,000
- Matched Odds API events: 2,125
- Target asset parquet: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/execution_training/telonex_odds_h2h_target_assets_latest.parquet`

## By Sport

| Sport | Assets | Markets | Odds events | Avg match score |
|---|---:|---:|---:|---:|
| soccer | 8,616 | 4,308 | 1,439 | 98.8% |
| basketball_nba | 538 | 269 | 268 | 95.0% |
| icehockey_nhl | 498 | 249 | 249 | 95.0% |
| americanfootball_nfl | 160 | 80 | 80 | 95.0% |
| basketball_wnba | 120 | 60 | 59 | 100.0% |
| baseball_mlb | 68 | 34 | 30 | 100.0% |

## Sample Targets

| Sport | Slug | Outcome | Odds event | From | To | Match |
|---|---|---|---|---|---|---:|
| basketball_wnba | `wnba-phx-nyl-2026-05-27` | New York Liberty | Phoenix Mercury @ New York Liberty | 2026-05-20 | 2026-05-28 | 100.0% |
| basketball_wnba | `wnba-phx-nyl-2026-05-27` | Phoenix Mercury | Phoenix Mercury @ New York Liberty | 2026-05-20 | 2026-05-28 | 100.0% |
| basketball_wnba | `wnba-conn-gsv-2026-05-25` | Connecticut Sun | Connecticut Sun @ Golden State Valkyries | 2026-05-19 | 2026-05-27 | 100.0% |
| basketball_wnba | `wnba-conn-gsv-2026-05-25` | Golden State Valkyries | Connecticut Sun @ Golden State Valkyries | 2026-05-19 | 2026-05-27 | 100.0% |
| basketball_wnba | `wnba-gsv-ind-2026-05-22` | Golden State Valkyries | Golden State Valkyries @ Indiana Fever | 2026-05-15 | 2026-05-23 | 100.0% |
| basketball_wnba | `wnba-gsv-ind-2026-05-22` | Indiana Fever | Golden State Valkyries @ Indiana Fever | 2026-05-15 | 2026-05-23 | 100.0% |
| basketball_wnba | `wnba-dal-chi-2026-05-20` | Chicago Sky | Dallas Wings @ Chicago Sky | 2026-05-14 | 2026-05-22 | 100.0% |
| basketball_wnba | `wnba-dal-chi-2026-05-20` | Dallas Wings | Dallas Wings @ Chicago Sky | 2026-05-14 | 2026-05-22 | 100.0% |
| basketball_wnba | `wnba-conn-por-2026-05-18` | Connecticut Sun | Connecticut Sun @ Portland Fire | 2026-05-12 | 2026-05-20 | 100.0% |
| basketball_wnba | `wnba-conn-por-2026-05-18` | Portland Fire | Connecticut Sun @ Portland Fire | 2026-05-12 | 2026-05-20 | 100.0% |
| basketball_wnba | `wnba-chi-min-2026-05-17` | Chicago Sky | Chicago Sky @ Minnesota Lynx | 2026-05-10 | 2026-05-18 | 100.0% |
| basketball_wnba | `wnba-chi-min-2026-05-17` | Minnesota Lynx | Chicago Sky @ Minnesota Lynx | 2026-05-10 | 2026-05-18 | 100.0% |
| basketball_wnba | `wnba-chi-por-2026-05-09` | Chicago Sky | Chicago Sky @ Portland Fire | 2026-05-03 | 2026-05-11 | 100.0% |
| basketball_wnba | `wnba-chi-por-2026-05-09` | Portland Fire | Chicago Sky @ Portland Fire | 2026-05-03 | 2026-05-11 | 100.0% |
| soccer | `sud-bra-car-2026-05-27-car` | No | Carabobo FC @ Bragantino-SP | 2026-05-21 | 2026-05-29 | 100.0% |
| soccer | `sud-bra-car-2026-05-27-car` | Yes | Carabobo FC @ Bragantino-SP | 2026-05-21 | 2026-05-29 | 100.0% |
| soccer | `sud-sao-bor-2026-05-26-sao` | No | CA Boston River @ Sao Paulo | 2026-05-19 | 2026-05-27 | 100.0% |
| soccer | `sud-sao-bor-2026-05-26-sao` | Yes | CA Boston River @ Sao Paulo | 2026-05-19 | 2026-05-27 | 100.0% |
| soccer | `lal-vil-mad-2026-05-24-draw` | No | Atlético Madrid @ Villarreal | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `lal-vil-mad-2026-05-24-draw` | Yes | Atlético Madrid @ Villarreal | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `lal-vil-mad-2026-05-24-mad` | No | Atlético Madrid @ Villarreal | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `lal-vil-mad-2026-05-24-mad` | Yes | Atlético Madrid @ Villarreal | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `lal-vil-mad-2026-05-24-vil` | No | Atlético Madrid @ Villarreal | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `lal-vil-mad-2026-05-24-vil` | Yes | Atlético Madrid @ Villarreal | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `nor-kbk-vik-2026-05-24-kbk` | No | Viking FK @ Kristiansund BK | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `nor-kbk-vik-2026-05-24-kbk` | Yes | Viking FK @ Kristiansund BK | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `nor-kbk-vik-2026-05-24-vik` | No | Viking FK @ Kristiansund BK | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `nor-kbk-vik-2026-05-24-vik` | Yes | Viking FK @ Kristiansund BK | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `epl-bri-mun-2026-05-24-bri` | No | Manchester United @ Brighton and Hove Albion | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `epl-bri-mun-2026-05-24-bri` | Yes | Manchester United @ Brighton and Hove Albion | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `epl-bri-mun-2026-05-24-draw` | No | Manchester United @ Brighton and Hove Albion | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `epl-bri-mun-2026-05-24-draw` | Yes | Manchester United @ Brighton and Hove Albion | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `epl-bri-mun-2026-05-24-mun` | No | Manchester United @ Brighton and Hove Albion | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `epl-bri-mun-2026-05-24-mun` | Yes | Manchester United @ Brighton and Hove Albion | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `epl-bur-wol-2026-05-24-bur` | No | Wolverhampton Wanderers @ Burnley | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `epl-bur-wol-2026-05-24-bur` | Yes | Wolverhampton Wanderers @ Burnley | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `epl-bur-wol-2026-05-24-draw` | No | Wolverhampton Wanderers @ Burnley | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `epl-bur-wol-2026-05-24-draw` | Yes | Wolverhampton Wanderers @ Burnley | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `epl-bur-wol-2026-05-24-wol` | No | Wolverhampton Wanderers @ Burnley | 2026-05-17 | 2026-05-25 | 100.0% |
| soccer | `epl-bur-wol-2026-05-24-wol` | Yes | Wolverhampton Wanderers @ Burnley | 2026-05-17 | 2026-05-25 | 100.0% |
