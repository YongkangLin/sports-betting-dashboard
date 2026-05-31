# Telonex Odds API Features

- Generated: 2026-05-31T18:29:18.445927+00:00
- Label rows: 5,392,062
- Candidate markets/tokens: 1257 / 2513
- Matched markets: 1257
- Mapped tokens: 2493
- Feature rows: 5,097,400
- Feature markets/tokens: 1225 / 2449
- Feature coverage: 94.54%
- Max odds age hours: 168.0
- Output: `/private/tmp/telonex_odds_features_latest.parquet`

## Coverage By Sport

| Sport | Rows | Markets | Tokens |
|---|---:|---:|---:|
| americanfootball_nfl | 415,814 | 80 | 160 |
| basketball_nba | 231,094 | 266 | 532 |
| basketball_wnba | 191,728 | 60 | 120 |
| icehockey_nhl | 1,217,522 | 249 | 498 |
| soccer_brazil_campeonato | 262,476 | 60 | 120 |
| soccer_conmebol_copa_libertadores | 53,636 | 6 | 12 |
| soccer_epl | 808,328 | 138 | 276 |
| soccer_france_ligue_one | 233,766 | 54 | 108 |
| soccer_germany_bundesliga | 338,706 | 69 | 138 |
| soccer_italy_serie_a | 412,806 | 75 | 150 |
| soccer_italy_serie_b | 48,744 | 21 | 42 |
| soccer_spain_la_liga | 472,702 | 89 | 177 |
| soccer_spain_segunda_division | 29,984 | 11 | 22 |
| soccer_uefa_champs_league | 380,094 | 47 | 94 |

## Coverage By Split

| Split | Rows | Matched rows | Coverage | Eligible rows | Eligible coverage | Eligible matched markets |
|---|---:|---:|---:|---:|---:|---:|
| test | 810,914 | 782,836 | 96.54% | 810,914 | 96.54% | 172 |
| train | 3,123,944 | 2,872,556 | 91.95% | 3,073,098 | 93.47% | 815 |
| unobserved | 531,302 | 531,302 | 100.00% | 531,302 | 100.00% | 74 |
| val | 925,902 | 910,706 | 98.36% | 925,902 | 98.36% | 164 |

## Coverage By Split And Sport

| Split | Sport | Rows | Matched rows | Coverage | Eligible rows | Eligible coverage |
|---|---|---:|---:|---:|---:|---:|
| test | baseball_mlb | 28,078 | 0 | 0.00% | 28,078 | 0.00% |
| test | basketball_nba | 17,070 | 17,070 | 100.00% | 17,070 | 100.00% |
| test | basketball_wnba | 164,694 | 164,694 | 100.00% | 164,694 | 100.00% |
| test | icehockey_nhl | 294,420 | 294,420 | 100.00% | 294,420 | 100.00% |
| test | soccer | 306,652 | 306,652 | 100.00% | 306,652 | 100.00% |
| train | americanfootball_nfl | 415,814 | 415,814 | 100.00% | 415,814 | 100.00% |
| train | baseball_mlb | 5,280 | 0 | 0.00% | 5,280 | 0.00% |
| train | basketball_nba | 199,482 | 180,146 | 90.31% | 199,482 | 90.31% |
| train | icehockey_nhl | 227,972 | 223,216 | 97.91% | 227,972 | 97.91% |
| train | soccer | 2,275,396 | 2,053,380 | 90.24% | 2,224,550 | 92.31% |
| unobserved | basketball_wnba | 1,660 | 1,660 | 100.00% | 1,660 | 100.00% |
| unobserved | soccer | 529,642 | 529,642 | 100.00% | 529,642 | 100.00% |
| val | baseball_mlb | 15,196 | 0 | 0.00% | 15,196 | 0.00% |
| val | basketball_nba | 33,878 | 33,878 | 100.00% | 33,878 | 100.00% |
| val | basketball_wnba | 25,374 | 25,374 | 100.00% | 25,374 | 100.00% |
| val | icehockey_nhl | 699,886 | 699,886 | 100.00% | 699,886 | 100.00% |
| val | soccer | 151,568 | 151,568 | 100.00% | 151,568 | 100.00% |

## Coverage By Split And Market Type

| Split | Market type | Rows | Matched rows | Coverage | Eligible rows | Eligible coverage |
|---|---|---:|---:|---:|---:|---:|
| test | h2h | 810,914 | 782,836 | 96.54% | 810,914 | 96.54% |
| train | h2h | 3,123,944 | 2,872,556 | 91.95% | 3,073,098 | 93.47% |
| unobserved | h2h | 531,302 | 531,302 | 100.00% | 531,302 | 100.00% |
| val | h2h | 925,902 | 910,706 | 98.36% | 925,902 | 98.36% |

## Top Uncovered Test Events

| Sport | Market type | Event | Rows |
|---|---|---|---:|
| baseball_mlb | h2h | San Francisco Giants vs. Arizona Diamondbacks | 24,330 |
| baseball_mlb | h2h | Arizona Diamondbacks vs. Colorado Rockies | 1,562 |
| baseball_mlb | h2h | Baltimore Orioles vs. Tampa Bay Rays | 1,322 |
| baseball_mlb | h2h | New York Mets vs. Miami Marlins | 864 |

## Diagnostics

- Match diagnostics: `{'markets': 1257, 'source': 'asset_plan', 'missing_odds_mapping': 0}`
- Mapping diagnostics: `{'tokens': 2513, 'mapped_tokens': 2493, 'unsupported_market_type': 0, 'unsupported_market_types': {}, 'unmapped_side': 20}`
- Join diagnostics: `{'mapped_label_rows': 5341216, 'mapped_label_markets': 1247, 'mapped_label_tokens': 2493, 'join_groups': 1916, 'groups_with_fair': 1916, 'candidate_rows_with_fair_group': 5341216, 'matched_feature_rows': 5097400, 'rows_before_first_odds_snapshot': 243816, 'rows_after_last_allowed_snapshot': 0, 'rows_without_fair_group': 0}`
- Validation checks: `{'probabilities_in_bounds': True, 'causal_snapshots': True, 'pre_commence_snapshots': True, 'non_negative_quote_age': True}`
- Odds quote age hours quantiles: `{'0.0': 0.0, '0.01': 0.006111111111111111, '0.05': 0.023055555555555555, '0.5': 2.3394444444444447, '0.95': 11.973055555555556, '0.99': 29.80655555555183, '1.0': 66.67277777777778}`
- Odds fair probability quantiles: `{'0.0': 0.04054252378007664, '0.01': 0.10964648765180662, '0.05': 0.13388401927079185, '0.5': 0.4672635054426733, '0.95': 0.8661159807292081, '0.99': 0.8903535123481934, '1.0': 0.9594574762199234}`

Only pre-commence Odds API snapshots are used, and each feature row requires odds_snapshot_ts <= asof_ts. Unsupported or unmatched markets remain quarantined from sharp-consensus/line-lag strategy eligibility rather than silently treated as missing sportsbook signal.
