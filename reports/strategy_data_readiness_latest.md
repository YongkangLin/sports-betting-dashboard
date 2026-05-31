# Strategy And Data Readiness

- Generated: 2026-05-31T14:45:59.047403+00:00
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

- Labels/markets/tokens: 5,418,878 / 632 / 1,261
- Time span: 2025-10-26 00:01:00+00:00 to 2026-05-29 23:59:00+00:00
- Sports: {'soccer': 2625089, 'baseball_mlb': 1731351, 'basketball_nba': 900769, 'americanfootball_nfl': 66302, 'basketball_wnba': 55474, 'tennis': 26200, 'icehockey_nhl': 13693}
- Telonex quote/depth/trade rows: 15,595,425 / 105,207,694 / 1,164,464
- Telonex manifest files existing/missing/total: 6,625 / 0 / 6,625
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
| train | 2,060,552 | 220 | 439 | 1,948,779 | 1,749,456 | 6,751 | 65,912 | 33,418 | 2,009 | 70.84% |
| val | 959,378 | 47 | 94 | 823,070 | 648,626 | 3,573 | 21,848 | 8,566 | 1,084 | 64.74% |
| test | 852,668 | 48 | 96 | 730,124 | 544,884 | 1,509 | 18,488 | 4,403 | 311 | 46.22% |

## Odds Strategy Coverage

- Gate: True
- Mode: strategy_eligible
- Full test coverage: 46.22%
- Strategy-eligible test rows: 463,902
- Strategy-eligible test coverage: 84.95%
- Strategy-eligible matched test markets: 22
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

- Test markets: 48
- Usable train/val/test markets: 315
- Test market ratio: 15.24%
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
