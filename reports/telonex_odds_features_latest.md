# Telonex Odds API Features

- Generated: 2026-05-30T21:48:12.821697+00:00
- Label rows: 2,888,585
- Candidate markets/tokens: 216 / 429
- Matched markets: 117
- Mapped tokens: 163
- Feature rows: 1,414,160
- Feature markets/tokens: 79 / 157
- Feature coverage: 48.96%
- Max odds age hours: 168.0
- Output: `/Users/yongkanglin/Documents/Codex/2026-05-28/i-have-this-repo-git-github-3/Sports-Betting-ml/data/processed/execution_training/telonex_odds_features_latest.parquet`

## Coverage By Sport

| Sport | Rows | Markets | Tokens |
|---|---:|---:|---:|
| baseball_mlb | 792,020 | 61 | 121 |
| basketball_wnba | 26,836 | 2 | 4 |
| soccer_brazil_campeonato | 377,170 | 8 | 16 |
| soccer_chile_campeonato | 22,172 | 1 | 2 |
| soccer_conmebol_copa_libertadores | 65,500 | 1 | 2 |
| soccer_norway_eliteserien | 130,462 | 6 | 12 |

## Coverage By Split

| Split | Rows | Matched rows | Coverage | Matched markets | Matched tokens |
|---|---:|---:|---:|---:|---:|
| test | 226,224 | 73,604 | 32.54% | 5 | 10 |
| train | 1,776,863 | 936,300 | 52.69% | 44 | 87 |
| unobserved | 539,748 | 229,330 | 42.49% | 24 | 48 |
| val | 345,750 | 174,926 | 50.59% | 6 | 12 |

## Diagnostics

- Match diagnostics: `{'markets': 216, 'no_slug_date': 0, 'no_title_parse': 0, 'no_sport_pool': 8, 'no_odds_event_match': 91}`
- Mapping diagnostics: `{'tokens': 429, 'mapped_tokens': 163, 'unsupported_market_type': 70, 'unsupported_market_types': {'nrfi': 64, 'halftime': 4, 'corners': 2}, 'unmapped_side': 0}`
- Join diagnostics: `{'mapped_label_rows': 1830923, 'mapped_label_markets': 82, 'mapped_label_tokens': 163, 'join_groups': 128, 'groups_with_fair': 122, 'candidate_rows_with_fair_group': 1802933, 'matched_feature_rows': 1414160, 'rows_before_first_odds_snapshot': 380649, 'rows_after_last_allowed_snapshot': 8124, 'rows_without_fair_group': 27990}`
- Validation checks: `{'probabilities_in_bounds': True, 'causal_snapshots': True, 'pre_commence_snapshots': True, 'non_negative_quote_age': True}`
- Odds quote age hours quantiles: `{'0.0': 0.005555555555555556, '0.01': 0.006388888888888889, '0.05': 0.05638888888888889, '0.5': 3.156388888888889, '0.95': 22.10638888888889, '0.99': 105.13972222222222, '1.0': 167.95638888888888}`
- Odds fair probability quantiles: `{'0.0': 0.06937064517986813, '0.01': 0.08136472775925196, '0.05': 0.18167614015939362, '0.5': 0.5, '0.95': 0.8183238598406064, '0.99': 0.918635272240748, '1.0': 0.9306293548201319}`

Only pre-commence Odds API snapshots are used, and each feature row requires odds_snapshot_ts <= asof_ts. Unsupported markets remain unmapped rather than imputed.
