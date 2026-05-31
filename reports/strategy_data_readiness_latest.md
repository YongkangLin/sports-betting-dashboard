# Strategy And Data Readiness

- Generated: 2026-05-31T10:37:50.307823+00:00
- Overall gate: False
- Verdict: HOLD: strategy is defined, but dataset is not complete enough to prove the bot
- Gate reasons: Odds API point-in-time features have insufficient test coverage

## Active Strategy

- Name: trade_confirmed_passive_maker_convergence
- Venue: Polymarket CLOB sports markets
- Target: `maker_trade_fill_positive`
- Entry policy: Post/quote passively near the current best bid only when the calibrated convergence score lower bound clears validation-selected threshold and liquidity caps.
- Exit/mark policy: Mark or exit against future best bid over 30/60/120/300/900 second horizons after Polymarket fee and spread friction; live version must cancel if edge decays.
- Secondary strategies: favorite_longshot_bias, stale_price_convergence, hedge_underpricing, post_event_overreaction_fade

## Dataset Extent

- Labels/markets/tokens: 2,888,585 / 216 / 429
- Time span: 2026-03-02 00:03:00+00:00 to 2026-05-29 23:59:00+00:00
- Sports: {'baseball_mlb': 1731351, 'soccer': 1108317, 'basketball_wnba': 43570, 'icehockey_nhl': 5347}
- Telonex quote/depth/trade rows: 14,538,432 / 105,207,694 / 1,064,811
- Telonex manifest files existing/missing/total: 6,325 / 0 / 6,325
- Telonex downloaded date span: 2025-10-26 to 2026-05-29
- Telonex catalog quote span: 2025-10-11 to 2026-05-29

## Two-Sided Market Data

- Gate: True
- Polymarket actual both-side CLOB events: 277 / 277
- Polymarket derived opposite-token lines: 0
- Complete on both CLOB and sportsbook overlays: 276 / 277 (99.64%)
- Sportsbook missing/incomplete overlay events: 1
- Completeness reasons: none

## Split Coverage

| Split | Rows | Markets | Tokens | Target observed | Past trade rows | Taker+ | Maker+ | Fill queue | Fill+ | Odds coverage |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| train | 1,776,863 | 75 | 149 | 1,513,571 | 1,177,192 | 9,036 | 68,137 | 19,156 | 2,820 | 51.40% |
| val | 345,750 | 16 | 32 | 312,014 | 230,990 | 934 | 7,298 | 2,716 | 208 | 50.35% |
| test | 226,224 | 18 | 36 | 159,230 | 116,762 | 538 | 6,798 | 1,093 | 97 | 32.44% |

## Gates

| Gate | Status |
|---|---:|
| download_manifest_integrity_gate | True |
| historical_l2_scale_gate | True |
| heldout_market_extent_gate | True |
| trade_confirmed_fill_holdout_gate | True |
| odds_holdout_coverage_gate | False |
| complete_side_market_data_gate | True |
| quality_gate | True |
| overall_gate | False |

## Held-Out Market Gate

- Test markets: 18
- Usable train/val/test markets: 109
- Test market ratio: 16.51%
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
