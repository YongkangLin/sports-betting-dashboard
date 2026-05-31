# Telonex Microstructure Bucket Audit

- Generated: 2026-05-31T00:24:48.626667+00:00
- Labels: 2,888,585 rows, 216 markets, 429 tokens
- Label SHA256: `32537f0d3b561eb1f7a39bcb5ed6ad4834d6f854a4443683da29c657d09f223b`
- Overall gate: False
- Gate reasons: YES+NO strict fee-adjusted arbitrage gate failed, no price-shock rule had enough validation rows/markets for CI

## YES+NO Underpricing

- Unique paired snapshots: 288,756
- Near buy-both rows (`ask_yes + ask_no <= 1.02`): 160,845 across 142 markets
- Strict gross buy-both rows: 0
- Strict fee-adjusted buy-both rows: 0
- Minimum ask sum / max net edge: 1.0 / -0.0002970000000000002
- Gate: False (no fee-adjusted YES+NO arbitrage in labels)

## Price-Shock Fade/Follow

- Gate: False
- Selected by validation: none

## Top Validation Rules

| Rule | Strategy | Val rows | Val markets | Val ROI | Val CI low | Test rows | Test markets | Test ROI | Test CI low |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|
| follow_lb900_move10c_h120 | follow | 89 | 4 | -2.44% | -5.94% | 91 | 6 | -3.18% | -13.27% |
| follow_lb900_move10c_h900 | follow | 77 | 4 | 4.11% | -6.01% | 79 | 6 | 2.25% | -10.91% |
| follow_lb300_move10c_h900 | follow | 18 | 3 | 1.01% | -6.37% | 28 | 6 | 1.82% | -14.08% |
| follow_lb900_move10c_h300 | follow | 87 | 4 | -1.31% | -7.19% | 93 | 6 | -1.06% | -10.03% |
| follow_lb900_move5c_h30 | follow | 211 | 6 | -4.33% | -8.05% | 151 | 8 | -3.91% | -8.30% |
| fade_lb300_move5c_h30 | fade | 126 | 6 | -6.67% | -8.65% | 63 | 7 | -7.22% | -18.11% |
| follow_lb900_move5c_h60 | follow | 213 | 6 | -4.29% | -8.66% | 149 | 8 | -3.29% | -6.36% |
| follow_lb900_move5c_h120 | follow | 211 | 5 | -3.92% | -8.72% | 149 | 8 | -3.30% | -8.72% |
| fade_lb300_move5c_h60 | fade | 126 | 6 | -6.65% | -8.78% | 62 | 6 | -8.16% | -23.11% |
| follow_lb900_move10c_h30 | follow | 92 | 5 | -3.60% | -9.02% | 91 | 6 | -3.75% | -10.31% |

## Interpretation

- YES+NO buy-both is only capital-relevant when the fee-adjusted edge is positive. Near-arb rows are useful for hedging research, not guaranteed profit.
- Price-shock rules are executable taker proxies using visible ask for entry and future bid for exit, minus sports fee friction.
- This is still not a live bot proof: the audit has no authenticated fill logs, no queue position, and no game-event ground truth.
