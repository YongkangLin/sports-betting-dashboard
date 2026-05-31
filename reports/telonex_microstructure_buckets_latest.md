# Telonex Microstructure Bucket Audit

- Generated: 2026-05-31T17:25:58.231500+00:00
- Labels: 9,457,109 rows, 1,665 markets, 3,316 tokens
- Label SHA256: `1233ef779055fd65b8ccb205cac07cdc089d439cda2d7b232126663560183ec6`
- Overall gate: False
- Gate reasons: YES+NO strict fee-adjusted arbitrage gate failed, selected price-shock validation CI lower bound is not positive, selected price-shock test CI lower bound is not positive

## YES+NO Underpricing

- Unique paired snapshots: 934,174
- Near buy-both rows (`ask_yes + ask_no <= 1.02`): 798,359 across 1,579 markets
- Strict gross buy-both rows: 0
- Strict fee-adjusted buy-both rows: 0
- Minimum ask sum / max net edge: 1.0 / -8.973000000000008e-05
- Gate: False (no fee-adjusted YES+NO arbitrage in labels)

## Price-Shock Fade/Follow

- Gate: False
- Selected by validation: follow_lb900_move5c_h60

| Split | Rows | Markets | ROI | 95% CI | Positive | Avg entry | Avg exit | Avg move |
|---|---:|---:|---:|---|---:|---:|---:|---:|
| train | 1,711 | 98 | -3.34% | -3.77% to -2.97% | 12.27% | 68.52% | 67.22% | 15.40% |
| val | 1,205 | 44 | -3.74% | -4.60% to -3.12% | 11.87% | 68.92% | 67.36% | 14.15% |
| test | 875 | 47 | -3.98% | -5.05% to -3.20% | 8.69% | 66.74% | 65.13% | 13.17% |

## Top Validation Rules

| Rule | Strategy | Val rows | Val markets | Val ROI | Val CI low | Test rows | Test markets | Test ROI | Test CI low |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|
| follow_lb300_move10c_h30 | follow | 284 | 26 | -3.76% | -4.41% | 168 | 28 | -5.09% | -7.71% |
| follow_lb900_move5c_h60 | follow | 1,205 | 44 | -3.74% | -4.60% | 875 | 47 | -3.98% | -5.05% |
| follow_lb900_move5c_h30 | follow | 1,225 | 45 | -3.67% | -4.61% | 896 | 50 | -3.90% | -4.97% |
| follow_lb300_move5c_h60 | follow | 681 | 44 | -4.13% | -5.02% | 517 | 48 | -5.17% | -6.85% |
| follow_lb300_move10c_h60 | follow | 279 | 26 | -4.06% | -5.04% | 163 | 24 | -5.26% | -8.15% |
| follow_lb300_move5c_h30 | follow | 696 | 46 | -4.00% | -5.05% | 541 | 52 | -4.66% | -5.83% |
| follow_lb900_move10c_h60 | follow | 640 | 27 | -3.94% | -5.18% | 424 | 24 | -3.46% | -4.53% |
| follow_lb900_move10c_h30 | follow | 652 | 27 | -3.93% | -5.32% | 433 | 25 | -3.59% | -4.97% |
| follow_lb900_move5c_h120 | follow | 1,184 | 41 | -4.12% | -5.68% | 849 | 39 | -3.90% | -5.34% |
| follow_lb300_move10c_h120 | follow | 275 | 25 | -4.12% | -5.80% | 162 | 24 | -5.14% | -7.97% |

## Interpretation

- YES+NO buy-both is only capital-relevant when the fee-adjusted edge is positive. Near-arb rows are useful for hedging research, not guaranteed profit.
- Price-shock rules are executable taker proxies using visible ask for entry and future bid for exit, minus sports fee friction.
- This is still not a live bot proof: the audit has no authenticated fill logs, no queue position, and no game-event ground truth.
