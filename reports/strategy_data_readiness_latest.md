# Strategy And Data Readiness

- Generated: 2026-05-31T18:57:14.726550+00:00
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

- Labels/markets/tokens: 5,392,062 / 1,257 / 2,513
- Time span: 2025-11-04 00:01:00+00:00 to 2026-05-29 02:09:00+00:00
- Sports: {'soccer': 3263258, 'icehockey_nhl': 1222278, 'americanfootball_nfl': 415814, 'basketball_nba': 250430, 'basketball_wnba': 191728, 'baseball_mlb': 48554}
- Telonex quote/depth/trade rows: 68,259,463 / 299,087,418 / 5,125,961
- Telonex manifest files existing/missing/total: 13,362 / 0 / 13,362
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
| train | 3,123,944 | 828 | 1,655 | 3,119,178 | 2,976,794 | 3,471 | 24,753 | 80,603 | 1,171 | 91.95% |
| val | 925,902 | 177 | 354 | 925,902 | 890,126 | 3,161 | 8,706 | 21,678 | 1,026 | 98.36% |
| test | 810,914 | 178 | 356 | 808,062 | 755,316 | 2,240 | 9,951 | 14,355 | 537 | 96.54% |

## Odds Strategy Coverage

- Gate: True
- Mode: strategy_eligible
- Full test coverage: 96.54%
- Strategy-eligible test rows: 810,914
- Strategy-eligible test coverage: 96.54%
- Strategy-eligible matched test markets: 172
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

- Test markets: 178
- Usable train/val/test markets: 1,183
- Test market ratio: 15.05%
- Minimum required ratio: 15.00%
- Legacy absolute 100-market gate would pass: True

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
