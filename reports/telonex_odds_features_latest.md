# Telonex Odds API Features

- Generated: 2026-05-31T13:42:55.571889+00:00
- Label rows: 2,888,585
- Candidate markets/tokens: 216 / 429
- Matched markets: 125
- Mapped tokens: 178
- Feature rows: 1,390,146
- Feature markets/tokens: 79 / 157
- Feature coverage: 48.13%
- Max odds age hours: 168.0
- Output: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/execution_training/telonex_odds_features_latest.parquet`

## Coverage By Sport

| Sport | Rows | Markets | Tokens |
|---|---:|---:|---:|
| baseball_mlb | 768,020 | 61 | 121 |
| basketball_wnba | 26,836 | 2 | 4 |
| soccer_brazil_campeonato | 377,170 | 8 | 16 |
| soccer_chile_campeonato | 22,172 | 1 | 2 |
| soccer_conmebol_copa_libertadores | 65,486 | 1 | 2 |
| soccer_norway_eliteserien | 130,462 | 6 | 12 |

## Coverage By Split

| Split | Rows | Matched rows | Coverage | Eligible rows | Eligible coverage | Eligible matched markets |
|---|---:|---:|---:|---:|---:|---:|
| test | 226,224 | 73,398 | 32.44% | 97,114 | 75.58% | 5 |
| train | 1,776,863 | 913,326 | 51.40% | 1,284,221 | 71.12% | 44 |
| unobserved | 539,748 | 229,330 | 42.49% | 242,875 | 94.42% | 24 |
| val | 345,750 | 174,092 | 50.35% | 212,060 | 82.10% | 6 |

## Coverage By Split And Sport

| Split | Sport | Rows | Matched rows | Coverage | Eligible rows | Eligible coverage |
|---|---|---:|---:|---:|---:|---:|
| test | baseball_mlb | 83,752 | 56,268 | 67.18% | 66,556 | 84.54% |
| test | basketball_wnba | 30,558 | 17,130 | 56.06% | 30,558 | 56.06% |
| test | soccer | 111,914 | 0 | 0.00% | 0 | 0.00% |
| train | baseball_mlb | 995,551 | 418,868 | 42.07% | 755,037 | 55.48% |
| train | basketball_wnba | 13,012 | 9,706 | 74.59% | 13,012 | 74.59% |
| train | soccer | 768,300 | 484,752 | 63.09% | 516,172 | 93.91% |
| unobserved | baseball_mlb | 533,398 | 229,330 | 42.99% | 237,528 | 96.55% |
| unobserved | icehockey_nhl | 5,347 | 0 | 0.00% | 5,347 | 0.00% |
| unobserved | soccer | 1,003 | 0 | 0.00% | 0 | 0.00% |
| val | baseball_mlb | 118,650 | 63,554 | 53.56% | 101,380 | 62.69% |
| val | soccer | 227,100 | 110,538 | 48.67% | 110,680 | 99.87% |

## Coverage By Split And Market Type

| Split | Market type | Rows | Matched rows | Coverage | Eligible rows | Eligible coverage |
|---|---|---:|---:|---:|---:|---:|
| test | exact_score | 5,666 | 0 | 0.00% | 0 | 0.00% |
| test | h2h | 196,654 | 68,992 | 35.08% | 92,536 | 74.56% |
| test | nrfi | 17,196 | 0 | 0.00% | 0 | 0.00% |
| test | spreads | 6,708 | 4,406 | 65.68% | 4,578 | 96.24% |
| train | corners | 700 | 0 | 0.00% | 0 | 0.00% |
| train | h2h | 1,470,767 | 882,672 | 60.01% | 1,233,687 | 71.55% |
| train | halftime | 13,672 | 0 | 0.00% | 0 | 0.00% |
| train | nrfi | 240,514 | 0 | 0.00% | 0 | 0.00% |
| train | spreads | 6,036 | 0 | 0.00% | 6,036 | 0.00% |
| train | totals | 45,174 | 30,654 | 67.86% | 44,498 | 68.89% |
| unobserved | h2h | 205,415 | 160,798 | 78.28% | 165,554 | 97.13% |
| unobserved | nrfi | 257,012 | 0 | 0.00% | 0 | 0.00% |
| unobserved | spreads | 42,286 | 42,286 | 100.00% | 42,286 | 100.00% |
| unobserved | totals | 35,035 | 26,246 | 74.91% | 35,035 | 74.91% |
| val | h2h | 328,480 | 174,092 | 53.00% | 212,060 | 82.10% |
| val | nrfi | 17,270 | 0 | 0.00% | 0 | 0.00% |

## Top Uncovered Test Events

| Sport | Market type | Event | Rows |
|---|---|---|---:|
| soccer | h2h | Luxembourg vs. Italy | 19,884 |
| soccer | h2h | Germany vs. Finland | 18,580 |
| soccer | h2h | Singapore vs. Mongolia | 17,822 |
| baseball_mlb | nrfi | Arizona Diamondbacks vs. Seattle Mariners | 17,196 |
| soccer | h2h | Netherlands vs. Algeria | 13,644 |
| basketball_wnba | h2h | Phoenix Mercury vs. New York Liberty | 13,428 |
| soccer | h2h | Austria vs. Tunisia | 9,074 |
| soccer | h2h | Slovakia vs. Malta | 8,904 |
| soccer | h2h | Türkiye vs. North Macedonia | 8,398 |
| soccer | h2h | Korea Republic vs. El Salvador | 7,048 |
| soccer | exact_score | Fenerbahçe SK vs. Samsunspor - Exact Score | 5,666 |
| baseball_mlb | h2h | Arizona Diamondbacks vs. Seattle Mariners | 4,232 |
| baseball_mlb | h2h | Houston Astros vs. Texas Rangers | 3,230 |
| baseball_mlb | h2h | Atlanta Braves vs. Cincinnati Reds | 2,654 |
| soccer | spreads | Luxembourg vs. Italy - More Markets | 1,166 |
| soccer | spreads | Fenerbahçe SK vs. Samsunspor - More Markets | 964 |
| soccer | h2h | France vs. Côte d'Ivoire | 764 |
| baseball_mlb | spreads | Tampa Bay Rays vs. New York Yankees | 172 |

## Diagnostics

- Match diagnostics: `{'markets': 216, 'no_slug_date': 0, 'no_title_parse': 0, 'no_sport_pool': 0, 'no_odds_event_match': 91}`
- Mapping diagnostics: `{'tokens': 429, 'mapped_tokens': 178, 'unsupported_market_type': 70, 'unsupported_market_types': {'nrfi': 64, 'halftime': 4, 'corners': 2}, 'unmapped_side': 0}`
- Join diagnostics: `{'mapped_label_rows': 1836270, 'mapped_label_markets': 90, 'mapped_label_tokens': 178, 'join_groups': 143, 'groups_with_fair': 129, 'candidate_rows_with_fair_group': 1807836, 'matched_feature_rows': 1390146, 'rows_before_first_odds_snapshot': 409566, 'rows_after_last_allowed_snapshot': 8124, 'rows_without_fair_group': 28434}`
- Validation checks: `{'probabilities_in_bounds': True, 'causal_snapshots': True, 'pre_commence_snapshots': True, 'non_negative_quote_age': True}`
- Odds quote age hours quantiles: `{'0.0': 0.005833333333333334, '0.01': 0.07305555555555555, '0.05': 0.37277777777777776, '0.5': 4.539444444444444, '0.95': 22.673055555555557, '0.99': 107.85055555555789, '1.0': 167.95638888888888}`
- Odds fair probability quantiles: `{'0.0': 0.06962685755698608, '0.01': 0.08136472775925196, '0.05': 0.18061360495460507, '0.5': 0.5, '0.95': 0.8193863950453949, '0.99': 0.918635272240748, '1.0': 0.930373142443014}`

Only pre-commence Odds API snapshots are used, and each feature row requires odds_snapshot_ts <= asof_ts. Unsupported or unmatched markets remain quarantined from sharp-consensus/line-lag strategy eligibility rather than silently treated as missing sportsbook signal.
