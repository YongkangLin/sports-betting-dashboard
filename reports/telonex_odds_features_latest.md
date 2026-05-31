# Telonex Odds API Features

- Generated: 2026-05-31T14:44:17.331623+00:00
- Label rows: 5,418,878
- Candidate markets/tokens: 632 / 1261
- Matched markets: 534
- Mapped tokens: 993
- Feature rows: 3,650,416
- Feature markets/tokens: 484 / 966
- Feature coverage: 67.36%
- Max odds age hours: 168.0
- Output: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/execution_training/telonex_odds_features_latest.parquet`

## Coverage By Sport

| Sport | Rows | Markets | Tokens |
|---|---:|---:|---:|
| americanfootball_nfl | 66,302 | 14 | 28 |
| baseball_mlb | 768,020 | 61 | 121 |
| basketball_nba | 670,184 | 184 | 367 |
| basketball_wnba | 38,740 | 5 | 10 |
| icehockey_nhl | 5,412 | 7 | 14 |
| soccer_brazil_campeonato | 508,516 | 23 | 46 |
| soccer_chile_campeonato | 22,172 | 1 | 2 |
| soccer_conmebol_copa_libertadores | 127,698 | 9 | 18 |
| soccer_epl | 242,528 | 32 | 64 |
| soccer_france_ligue_one | 177,138 | 25 | 50 |
| soccer_germany_bundesliga | 149,272 | 20 | 40 |
| soccer_italy_serie_a | 371,330 | 50 | 100 |
| soccer_italy_serie_b | 26,752 | 5 | 10 |
| soccer_norway_eliteserien | 130,462 | 6 | 12 |
| soccer_spain_la_liga | 185,194 | 23 | 46 |
| soccer_uefa_champs_league | 160,696 | 19 | 38 |

## Coverage By Split

| Split | Rows | Matched rows | Coverage | Eligible rows | Eligible coverage | Eligible matched markets |
|---|---:|---:|---:|---:|---:|---:|
| test | 852,668 | 394,094 | 46.22% | 463,902 | 84.95% | 22 |
| train | 2,060,552 | 1,459,594 | 70.84% | 1,841,900 | 79.24% | 205 |
| unobserved | 1,546,280 | 1,175,658 | 76.03% | 1,222,613 | 96.16% | 226 |
| val | 959,378 | 621,070 | 64.74% | 801,976 | 77.44% | 31 |

## Coverage By Split And Sport

| Split | Sport | Rows | Matched rows | Coverage | Eligible rows | Eligible coverage |
|---|---|---:|---:|---:|---:|---:|
| test | baseball_mlb | 202,402 | 119,822 | 59.20% | 167,936 | 71.35% |
| test | basketball_wnba | 30,558 | 17,130 | 56.06% | 30,558 | 56.06% |
| test | soccer | 619,708 | 257,142 | 41.49% | 265,408 | 96.89% |
| train | americanfootball_nfl | 9,466 | 9,466 | 100.00% | 9,466 | 100.00% |
| train | baseball_mlb | 661,011 | 269,872 | 40.83% | 451,737 | 59.74% |
| train | basketball_nba | 735,477 | 535,380 | 72.79% | 735,477 | 72.79% |
| train | soccer | 654,598 | 644,876 | 98.51% | 645,220 | 99.95% |
| unobserved | americanfootball_nfl | 56,836 | 56,836 | 100.00% | 56,836 | 100.00% |
| unobserved | baseball_mlb | 533,398 | 229,330 | 42.99% | 237,528 | 96.55% |
| unobserved | basketball_nba | 165,292 | 134,804 | 81.56% | 165,280 | 81.56% |
| unobserved | basketball_wnba | 11,904 | 11,904 | 100.00% | 11,904 | 100.00% |
| unobserved | icehockey_nhl | 13,693 | 5,412 | 39.52% | 13,693 | 39.52% |
| unobserved | soccer | 738,957 | 737,372 | 99.79% | 737,372 | 100.00% |
| unobserved | tennis | 26,200 | 0 | 0.00% | 0 | 0.00% |
| val | baseball_mlb | 334,540 | 148,996 | 44.54% | 303,300 | 49.12% |
| val | basketball_wnba | 13,012 | 9,706 | 74.59% | 13,012 | 74.59% |
| val | soccer | 611,826 | 462,368 | 75.57% | 485,664 | 95.20% |

## Coverage By Split And Market Type

| Split | Market type | Rows | Matched rows | Coverage | Eligible rows | Eligible coverage |
|---|---|---:|---:|---:|---:|---:|
| test | exact_score | 5,666 | 0 | 0.00% | 0 | 0.00% |
| test | h2h | 789,822 | 373,682 | 47.31% | 443,318 | 84.29% |
| test | nrfi | 34,466 | 0 | 0.00% | 0 | 0.00% |
| test | spreads | 6,708 | 4,406 | 65.68% | 4,578 | 96.24% |
| test | totals | 16,006 | 16,006 | 100.00% | 16,006 | 100.00% |
| train | h2h | 1,851,278 | 1,459,594 | 78.84% | 1,841,900 | 79.24% |
| train | nrfi | 209,274 | 0 | 0.00% | 0 | 0.00% |
| unobserved | h2h | 1,203,601 | 1,101,714 | 91.53% | 1,136,946 | 96.90% |
| unobserved | nrfi | 257,012 | 0 | 0.00% | 0 | 0.00% |
| unobserved | spreads | 42,286 | 42,286 | 100.00% | 42,286 | 100.00% |
| unobserved | totals | 43,381 | 31,658 | 72.98% | 43,381 | 72.98% |
| val | corners | 700 | 0 | 0.00% | 0 | 0.00% |
| val | h2h | 878,562 | 606,422 | 69.02% | 767,448 | 79.02% |
| val | halftime | 13,672 | 0 | 0.00% | 0 | 0.00% |
| val | nrfi | 31,240 | 0 | 0.00% | 0 | 0.00% |
| val | spreads | 6,036 | 0 | 0.00% | 6,036 | 0.00% |
| val | totals | 29,168 | 14,648 | 50.22% | 28,492 | 51.41% |

## Top Uncovered Test Events

| Sport | Market type | Event | Rows |
|---|---|---|---:|
| soccer | h2h | Switzerland vs. Jordan | 71,258 |
| soccer | h2h | Japan vs. Iceland | 42,908 |
| soccer | h2h | Germany vs. Finland | 39,726 |
| soccer | h2h | Singapore vs. Mongolia | 35,198 |
| soccer | h2h | NJ/NY Gotham FC vs. Houston Dash | 34,990 |
| soccer | h2h | Brazil vs. Panama | 34,600 |
| soccer | h2h | Chicago Stars FC vs. San Diego Wave FC | 20,108 |
| soccer | h2h | Luxembourg vs. Italy | 19,884 |
| baseball_mlb | nrfi | Tampa Bay Rays vs. New York Yankees | 17,270 |
| baseball_mlb | nrfi | Arizona Diamondbacks vs. Seattle Mariners | 17,196 |
| baseball_mlb | h2h | Minnesota Twins vs. Chicago White Sox | 13,996 |
| soccer | h2h | Netherlands vs. Algeria | 13,644 |
| basketball_wnba | h2h | Phoenix Mercury vs. New York Liberty | 13,428 |
| baseball_mlb | h2h | Tampa Bay Rays vs. New York Yankees | 11,910 |
| soccer | h2h | Austria vs. Tunisia | 9,074 |
| soccer | h2h | Slovakia vs. Malta | 8,904 |
| soccer | h2h | Türkiye vs. North Macedonia | 8,398 |
| baseball_mlb | h2h | Seattle Mariners vs. Athletics | 8,136 |
| soccer | h2h | Clube do Remo vs. São Paulo FC | 8,124 |
| soccer | h2h | Korea Republic vs. El Salvador | 7,048 |

## Diagnostics

- Match diagnostics: `{'markets': 632, 'no_slug_date': 0, 'no_title_parse': 0, 'no_sport_pool': 5, 'no_odds_event_match': 93}`
- Mapping diagnostics: `{'tokens': 1261, 'mapped_tokens': 993, 'unsupported_market_type': 70, 'unsupported_market_types': {'nrfi': 64, 'halftime': 4, 'corners': 2}, 'unmapped_side': 3}`
- Join diagnostics: `{'mapped_label_rows': 4330391, 'mapped_label_markets': 498, 'mapped_label_tokens': 993, 'join_groups': 755, 'groups_with_fair': 737, 'candidate_rows_with_fair_group': 4299627, 'matched_feature_rows': 3650416, 'rows_before_first_odds_snapshot': 640743, 'rows_after_last_allowed_snapshot': 8468, 'rows_without_fair_group': 30764}`
- Validation checks: `{'probabilities_in_bounds': True, 'causal_snapshots': True, 'pre_commence_snapshots': True, 'non_negative_quote_age': True}`
- Odds quote age hours quantiles: `{'0.0': 0.0, '0.01': 0.006111111111111111, '0.05': 0.006388888888888889, '0.5': 0.23972222222222223, '0.95': 18.323055555555555, '0.99': 26.00583333333333, '1.0': 167.95638888888888}`
- Odds fair probability quantiles: `{'0.0': 0.06962685755698608, '0.01': 0.1038952450868161, '0.05': 0.11843945231496976, '0.5': 0.5, '0.95': 0.8815605476850302, '0.99': 0.8961047549131839, '1.0': 0.930373142443014}`

Only pre-commence Odds API snapshots are used, and each feature row requires odds_snapshot_ts <= asof_ts. Unsupported or unmatched markets remain quarantined from sharp-consensus/line-lag strategy eligibility rather than silently treated as missing sportsbook signal.
