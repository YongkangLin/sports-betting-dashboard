# Latest Status

## Overall Plan

Run a lean Telonex/Odds API execution workflow: collect/refresh CLOB and sportsbook data, build causal execution labels and odds features, train separate eligible market-group models, validate them on strict temporal splits, monitor live paper execution quality, and only then consider capital.

## Current Verdict

- Generated: 2026-06-01T00:48:39.773126+00:00
- Verdict: HOLD; live capital enabled: False; live capital gate: False
- Collector: healthy at loop 479
- Latest model: `20260531T234614Z-03d084dd3bd6`
- Model group/target/selection: `all` / `maker_positive` / `convergence_prob_lower`
- Test ROI/trades/markets: 0.0922 / 2134 / 50

## Achieved

- Built protected Telonex/Odds API model dataset: 6,395,081 label rows, 1,550 markets, 3,098 tokens.
- Materialized Odds API feature layer: 5,358,403 rows with 83.79% coverage.
- Trained latest Telonex convergence model run `20260531T234614Z` for `all` using `all_odds` features.
- Audited separate market-type model readiness: gate False.
- Materialized dashboard replay bundle: 1,660 events (277 decision replays, 1,383 plot-only series).
- Kept live CLOB capture, queue/fill modeling, Telonex scoring, validation, model monitoring, and dashboard publishing as the active workflow.
- Consolidated repository reporting to this single latest-status file; per-script summaries are treated as local byproducts outside the repo.

## What Is Left

- Validate a profitable executable strategy on strict temporal holdouts with train_max_date < test_min_date for every fold.
- Collect enough authenticated Polymarket order/fill lifecycle rows to prove queue/fill behavior on real fills.
- Improve historical Telonex quote/depth manifest coverage or repair local manifests so live gates see the full protected store.
- Prove Odds API fusion on the latest Telonex target with target-compatible validation outputs.
- Train/deploy separate model weights for market groups only after their minimum market-count gates pass.
- Keep live paper-fill LEV and drift monitors green before enabling capital.

## Blockers

- queue/fill model not validated on authenticated fills
- Polymarket user-channel credentials not configured
- no predeclared executable taker strategy bucket cleared validation
- market-type separate-weight readiness gate failed
- Telonex model monitor hold
- live paper-fill LEV/price-hold quality gate failed
- Telonex temporal validation gate failed

## Warnings

- predeclared non-ML Telonex strategy buckets failed
- live game-state feed too thin for event-regime/scoreline/garbage-time features
- trade-flow feature family has no confirmed economic permutation impact yet
- Odds feature family has no confirmed economic permutation impact in latest audit
- Odds API fusion reports are not target-compatible with latest Telonex model
- live strategy LEV evidence incomplete
- Telonex market-disjoint validation not run

## Current Metrics

- Telonex labels: 6,395,081 rows, 1,550 markets, 3,098 tokens.
- Odds features: 5,358,403 rows, 1,312 markets, 2,622 tokens, 83.79% coverage.
- Telonex downloaded quote/depth/trade rows: 2,258,881 / 11,451,632 / 38,783.
- Queue/fill training rows: 1,125; queue model proxy/auth gates: True / False.
- Strategy buckets positive test buckets: 0; executable taker gate: False.
- Replay bundle: 1,660 events, 849,053 CLOB points, 1,422 events with Odds API overlays.
- Live Telonex selected signals/candidate tokens: 0 / 212.
- Live execution quality gate: False; alpha/probe 3s rows: 0 / 19.
- Model monitor verdict: HOLD: latest external validation gate failed; ECE drift alerts fired; external validation gate: False.
- Market-disjoint gate/ROI/trades: None / n/a / None.
- Temporal gate/ROI/trades: False / n/a / 0.
- Market-type separate-weight gate: False; blockers: 4.
- Polymarket user channel configured: False; missing fields: api_key, api_secret, passphrase.
- Secret findings: 0; critical: 0.

## Next Actions

- Repair or refresh Telonex historical manifest paths so quote/depth gates reflect the protected data that is actually present.
- Collect authenticated Polymarket user-channel fills and rerun queue/fill training.
- Rerun strict temporal validation after separate market-group models are trained.
- Keep capital disabled until the live quality, model monitor, and validation gates all pass together.
