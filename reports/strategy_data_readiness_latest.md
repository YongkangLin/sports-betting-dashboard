# Strategy And Data Readiness

- Generated: 2026-05-31T15:30:37.703705+00:00
- Overall gate: False
- Verdict: HOLD: strategy is defined, but dataset is not complete enough to prove the bot
- Gate reasons: sportsbook native 5-minute density gate failed: complete 5m replay cache 167 / 276 = 60.51% < 95%

## Active Strategy

- Name: trade_confirmed_passive_maker_convergence
- Venue: Polymarket CLOB sports markets
- Target: `maker_trade_fill_positive`
- Entry policy: Post/quote passively near the current best bid only when the calibrated convergence score lower bound clears validation-selected threshold and liquidity caps.
- Exit/mark policy: Mark or exit against future best bid over 30/60/120/300/900 second horizons after Polymarket fee and spread friction; live version must cancel if edge decays.
- Secondary strategies: favorite_longshot_bias, stale_price_convergence, hedge_underpricing, post_event_overreaction_fade

## Dataset Extent

- Labels/markets/tokens: 5,768,529 / 725 / 1,436
- Time span: 2025-10-26 00:01:00+00:00 to 2026-05-29 23:59:00+00:00
- Sports: {'soccer': 2625089, 'baseball_mlb': 1755107, 'basketball_nba': 908403, 'americanfootball_nfl': 384029, 'basketball_wnba': 56008, 'tennis': 26200, 'icehockey_nhl': 13693}
- Telonex quote/depth/trade rows: 35,604,122 / 203,679,373 / 3,430,854
- Telonex manifest files existing/missing/total: 8,712 / 0 / 8,712
- Telonex downloaded date span: 2025-10-23 to 2026-05-29
- Telonex catalog quote span: 2025-10-11 to 2026-05-29

## Two-Sided Market Data

- Gate: True
- Polymarket actual both-side CLOB events: 277 / 277
- Polymarket derived opposite-token lines: 0
- Complete on both CLOB and sportsbook overlays: 276 / 277 (99.64%)
- Sportsbook missing/incomplete overlay events: 1
- Completeness reasons: none

## Replay Sportsbook Gap Audit

- 15m cache gate: True
- Native 5m density gate: False
- Matched events with complete 15m cache: 276 / 276
- Matched events with complete 5m cache: 167 / 276 (60.51%)
- Unique 5m snapshots cached rate: 69.37%
- Unique 5m snapshots missing: 14,224 / 46,443
- Warehouse replay-window cross-checks: 276
- Extra non-replay timestamps inside replay windows: 1,379
- Gap reasons: complete 5m replay cache 167 / 276 = 60.51% < 95%

## Split Coverage

| Split | Rows | Markets | Tokens | Target observed | Past trade rows | Taker+ | Maker+ | Fill queue | Fill+ | Odds coverage |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| train | 2,195,358 | 287 | 567 | 2,090,788 | 1,904,142 | 9,064 | 65,870 | 40,554 | 2,794 | 73.50% |
| val | 797,523 | 62 | 123 | 704,029 | 588,788 | 4,068 | 21,876 | 10,888 | 1,299 | 64.36% |
| test | 1,265,120 | 62 | 123 | 1,091,540 | 830,090 | 2,486 | 25,620 | 6,275 | 574 | 57.84% |

## Odds Strategy Coverage

- Gate: True
- Mode: strategy_eligible
- Full test coverage: 57.84%
- Strategy-eligible test rows: 843,968
- Strategy-eligible test coverage: 86.71%
- Strategy-eligible matched test markets: 34
- Policy: For Odds-dependent strategies, unsupported or unmatched markets are quarantined from the denominator. The gate measures rows where the token can actually map to a causal h2h/spreads/totals sportsbook outcome.

## Gates

| Gate | Status |
|---|---:|
| download_manifest_integrity_gate | True |
| historical_l2_scale_gate | True |
| heldout_market_extent_gate | True |
| trade_confirmed_fill_holdout_gate | True |
| odds_holdout_coverage_gate | True |
| complete_side_market_data_gate | True |
| sportsbook_native_5m_density_gate | False |
| quality_gate | True |
| overall_gate | False |

## Held-Out Market Gate

- Test markets: 62
- Usable train/val/test markets: 411
- Test market ratio: 15.09%
- Minimum required ratio: 15.00%
- Legacy absolute 100-market gate would pass: False

## Accuracy Checks

| Check | Status |
|---|---:|
| prices_in_bounds | True |
| entry_books_not_crossed | True |
| future_books_not_crossed | True |
| future_after_asof | True |
| target_after_asof | True |
| non_negative_quote_age | True |
| market_disjoint_splits | True |

This report is deliberately strict. It can say the historical L2 dataset is large while still blocking the trading bot because the held-out data lacks trade-confirmed fills, Odds API coverage, or enough unique markets to prove the active strategy.
