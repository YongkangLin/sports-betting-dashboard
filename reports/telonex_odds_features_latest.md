# Telonex Odds API Features

- Generated: 2026-05-31T15:28:36.152251+00:00
- Label rows: 5,768,529
- Candidate markets/tokens: 725 / 1436
- Matched markets: 626
- Mapped tokens: 1166
- Feature rows: 3,998,455
- Feature markets/tokens: 576 / 1139
- Feature coverage: 69.31%
- Max odds age hours: 168.0
- Output: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/execution_training/telonex_odds_features_latest.parquet`

## Coverage By Sport

| Sport | Rows | Markets | Tokens |
|---|---:|---:|---:|
| americanfootball_nfl | 384,029 | 73 | 145 |
| baseball_mlb | 790,164 | 80 | 156 |
| basketball_nba | 677,818 | 197 | 386 |
| basketball_wnba | 39,274 | 6 | 12 |
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
| test | 1,265,120 | 731,772 | 57.84% | 843,968 | 86.71% | 34 |
| train | 2,195,358 | 1,613,531 | 73.50% | 1,975,150 | 81.69% | 272 |
| unobserved | 1,510,528 | 1,139,906 | 75.46% | 1,186,861 | 96.04% | 223 |
| val | 797,523 | 513,246 | 64.36% | 672,451 | 76.32% | 47 |

## Coverage By Split And Sport

| Split | Sport | Rows | Matched rows | Coverage | Eligible rows | Eligible coverage |
|---|---|---:|---:|---:|---:|---:|
| test | baseball_mlb | 270,832 | 146,372 | 54.05% | 236,366 | 61.93% |
| test | basketball_wnba | 30,558 | 17,130 | 56.06% | 30,558 | 56.06% |
| test | soccer | 963,730 | 568,270 | 58.97% | 577,044 | 98.48% |
| train | americanfootball_nfl | 368,541 | 368,541 | 100.00% | 368,541 | 100.00% |
| train | baseball_mlb | 624,868 | 252,602 | 40.42% | 413,982 | 61.02% |
| train | basketball_nba | 700,191 | 500,296 | 71.45% | 700,191 | 71.45% |
| train | soccer | 501,758 | 492,092 | 98.07% | 492,436 | 99.93% |
| unobserved | americanfootball_nfl | 15,488 | 15,488 | 100.00% | 15,488 | 100.00% |
| unobserved | baseball_mlb | 537,920 | 233,852 | 43.47% | 242,050 | 96.61% |
| unobserved | basketball_nba | 166,366 | 135,878 | 81.67% | 166,354 | 81.68% |
| unobserved | basketball_wnba | 11,904 | 11,904 | 100.00% | 11,904 | 100.00% |
| unobserved | icehockey_nhl | 13,693 | 5,412 | 39.52% | 13,693 | 39.52% |
| unobserved | soccer | 738,957 | 737,372 | 99.79% | 737,372 | 100.00% |
| unobserved | tennis | 26,200 | 0 | 0.00% | 0 | 0.00% |
| val | baseball_mlb | 321,487 | 157,338 | 48.94% | 290,247 | 54.21% |
| val | basketball_nba | 41,846 | 41,644 | 99.52% | 41,846 | 99.52% |
| val | basketball_wnba | 13,546 | 10,240 | 75.59% | 13,546 | 75.59% |
| val | soccer | 420,644 | 304,024 | 72.28% | 326,812 | 93.03% |

## Coverage By Split And Market Type

| Split | Market type | Rows | Matched rows | Coverage | Eligible rows | Eligible coverage |
|---|---|---:|---:|---:|---:|---:|
| test | exact_score | 5,666 | 0 | 0.00% | 0 | 0.00% |
| test | h2h | 1,189,762 | 711,360 | 59.79% | 823,384 | 86.39% |
| test | halftime | 12,512 | 0 | 0.00% | 0 | 0.00% |
| test | nrfi | 34,466 | 0 | 0.00% | 0 | 0.00% |
| test | spreads | 6,708 | 4,406 | 65.68% | 4,578 | 96.24% |
| test | totals | 16,006 | 16,006 | 100.00% | 16,006 | 100.00% |
| train | h2h | 1,986,084 | 1,613,531 | 81.24% | 1,975,150 | 81.69% |
| train | nrfi | 209,274 | 0 | 0.00% | 0 | 0.00% |
| unobserved | h2h | 1,167,849 | 1,065,962 | 91.28% | 1,101,194 | 96.80% |
| unobserved | nrfi | 257,012 | 0 | 0.00% | 0 | 0.00% |
| unobserved | spreads | 42,286 | 42,286 | 100.00% | 42,286 | 100.00% |
| unobserved | totals | 43,381 | 31,658 | 72.98% | 43,381 | 72.98% |
| val | corners | 700 | 0 | 0.00% | 0 | 0.00% |
| val | h2h | 729,219 | 498,598 | 68.37% | 637,923 | 78.16% |
| val | halftime | 1,160 | 0 | 0.00% | 0 | 0.00% |
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
| baseball_mlb | h2h | Texas Rangers vs. Los Angeles Angels | 28,174 |
| soccer | h2h | Chicago Stars FC vs. San Diego Wave FC | 20,108 |
| soccer | h2h | Luxembourg vs. Italy | 19,884 |
| soccer | h2h | Club Universitario de Deportes vs. CS Huancayo | 19,874 |
| baseball_mlb | h2h | Seattle Mariners vs. Kansas City Royals | 17,490 |
| baseball_mlb | nrfi | Tampa Bay Rays vs. New York Yankees | 17,270 |
| baseball_mlb | nrfi | Arizona Diamondbacks vs. Seattle Mariners | 17,196 |
| baseball_mlb | h2h | Minnesota Twins vs. Chicago White Sox | 13,996 |
| soccer | h2h | Netherlands vs. Algeria | 13,644 |
| basketball_wnba | h2h | Phoenix Mercury vs. New York Liberty | 13,428 |
| soccer | halftime | Clube do Remo vs. São Paulo FC - Halftime Result | 12,512 |
| baseball_mlb | h2h | Tampa Bay Rays vs. New York Yankees | 11,910 |
| soccer | h2h | Austria vs. Tunisia | 9,074 |
| soccer | h2h | Slovakia vs. Malta | 8,904 |

## Diagnostics

- Match diagnostics: `{'markets': 725, 'no_slug_date': 0, 'no_title_parse': 0, 'no_sport_pool': 5, 'no_odds_event_match': 94}`
- Mapping diagnostics: `{'tokens': 1436, 'mapped_tokens': 1166, 'unsupported_market_type': 70, 'unsupported_market_types': {'nrfi': 64, 'halftime': 4, 'corners': 2}, 'unmapped_side': 3}`
- Join diagnostics: `{'mapped_label_rows': 4678430, 'mapped_label_markets': 590, 'mapped_label_tokens': 1166, 'join_groups': 923, 'groups_with_fair': 905, 'candidate_rows_with_fair_group': 4647666, 'matched_feature_rows': 3998455, 'rows_before_first_odds_snapshot': 640743, 'rows_after_last_allowed_snapshot': 8468, 'rows_without_fair_group': 30764}`
- Validation checks: `{'probabilities_in_bounds': True, 'causal_snapshots': True, 'pre_commence_snapshots': True, 'non_negative_quote_age': True}`
- Odds quote age hours quantiles: `{'0.0': 0.0, '0.01': 0.006111111111111111, '0.05': 0.006388888888888889, '0.5': 0.7061111111111111, '0.95': 17.739722222222223, '0.99': 25.823055555555555, '1.0': 167.95638888888888}`
- Odds fair probability quantiles: `{'0.0': 0.06962685755698608, '0.01': 0.10394674010167473, '0.05': 0.11970770931941636, '0.5': 0.49962323423100946, '0.95': 0.8802922906805837, '0.99': 0.8960532598983253, '1.0': 0.930373142443014}`

Only pre-commence Odds API snapshots are used, and each feature row requires odds_snapshot_ts <= asof_ts. Unsupported or unmatched markets remain quarantined from sharp-consensus/line-lag strategy eligibility rather than silently treated as missing sportsbook signal.
