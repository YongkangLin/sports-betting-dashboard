# Proxy Trade Path

Event: **CA Lanús vs. LDU de Quito**
Market: `h2h_3way` / side `LDU Quito`
Decision time: `2026-04-28 18:00:00+00:00`
Recommended strategy: `market_residual` / score `market_residual_ev`
Strategy fair value: `0.229` from `market_residual_prob`
Fair source: `odds_consensus_live_plus_ml_residual`
ML residual applied to live odds fair: `+0.083`
Decision Polymarket price: `0.125`
Proxy path rows: `525`
Proxy trades/marks: `2`
Proxy PnL per share before costs: `0.000`
Trade display mode: `single round-trip`, entry edge `4.0%`, no-new-entry midpoint bounds `0.03` to `0.97`

![Proxy trade path](/Users/yongkanglin/Documents/Codex/2026-05-28/i-have-this-repo-git-github-3/Sports-Betting-ml/reports/proxy_trade_path_latest.png)

## Trade Reasoning

- `2026-04-28 18:11:15+00:00` `BUY` at `0.125`: Buy proxy: model fair 0.217 vs midpoint 0.125, edge 9.2%.
- `2026-04-28 18:13:04+00:00` `MARK_STALE_FAIR` at `0.125`: Stop/mark proxy: no fresh fair value within 90s; marked 0.000 per share before costs.

## Important Limitation

This is a visualization/debug simulation only. It is not a proof-quality trading backtest because the current data lacks executable bid/ask, depth, queue/fill mechanics, and a trained play-by-play in-game win-probability model.
