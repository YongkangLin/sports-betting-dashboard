# Play-By-Play Source Plan

- Generated: 2026-05-31T04:27:17.140407+00:00
- Feature file status: missing_feature_file / rows 0 / markets 0
- Rule: raw text is parser input only; model inputs must be structured state and consequence fields.

## Priority By Current Telonex Labels

| Priority | Sport | Current rows | Source | Role | Status |
|---:|---|---:|---|---|---|
| 1 | MLB | 1,731,351 | MLB Stats API / pybaseball Statcast | Highest current Telonex row count; base/out/count, pitcher/batter, and WPA-style states are mandatory. | ready to build normalizer |
| 2 | Soccer | 1,108,317 | StatsBomb Open Data | High-quality training data for event meaning, xG, red cards, and shot-context features. | ready to build normalizer |
| 3 | WNBA | 43,570 | wehoop | Current Telonex data includes WNBA; use same state contract as NBA where coverage exists. | ready to build normalizer |
| 4 | NHL | 5,347 | fastRhockey / hockeyR | Goal/penalty/strength-state reaction modeling for hockey markets. | ready to build normalizer |
| 5 | NFL | 0 | nflverse / nflfastR | Best first live-state candidate when NFL markets are downloaded: mature down/distance EPA/WP labels. | ready to build normalizer |
| 6 | NBA | 0 | hoopR, with nba_api as live/endpoint fallback | Lineup, substitution, injury, pace, and score-state features for NBA favorite/line-lag filters. | ready to build normalizer |

## Build Order

1. baseball_mlb
2. soccer
3. basketball_wnba
4. icehockey_nhl

## Contract

- Do not feed raw play-by-play text into the model. Normalize events into state_before, event, state_after, and consequence columns first.
- Required join: `event_time <= market_price_time, with market price before/after windows recorded causally.`
- First training targets:
  - `fair_price_after - market_price_after`
  - `reaction_gap = delta_fair_price - delta_market_price`
  - `future executable LEV after event shock`
