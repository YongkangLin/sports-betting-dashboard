# Telonex Microstructure Bucket Audit

- Generated: 2026-05-31T14:44:44.058565+00:00
- Labels: 5,418,878 rows, 632 markets, 1,261 tokens
- Label SHA256: `a0a6e936af3ca1f7dbe20717dd54aad3f0078761c7c11a0784d7fb95862677da`
- Overall gate: False
- Gate reasons: YES+NO strict fee-adjusted arbitrage gate failed, no price-shock rule had enough validation rows/markets for CI

## YES+NO Underpricing

- Unique paired snapshots: 540,638
- Near buy-both rows (`ask_yes + ask_no <= 1.02`): 410,099 across 558 markets
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
| follow_lb900_move10c_h30 | follow | 500 | 16 | -2.98% | -3.46% | 183 | 11 | -3.67% | -5.92% |
| follow_lb900_move5c_h30 | follow | 847 | 19 | -3.24% | -3.50% | 365 | 15 | -4.12% | -6.09% |
| follow_lb900_move10c_h60 | follow | 492 | 16 | -3.21% | -3.78% | 180 | 10 | -3.42% | -6.63% |
| follow_lb900_move5c_h60 | follow | 840 | 18 | -3.49% | -3.98% | 364 | 15 | -3.86% | -6.10% |
| follow_lb900_move10c_h120 | follow | 484 | 14 | -3.06% | -4.12% | 180 | 10 | -2.80% | -5.57% |
| follow_lb300_move5c_h30 | follow | 500 | 18 | -3.67% | -4.17% | 191 | 14 | -5.39% | -9.08% |
| follow_lb900_move5c_h120 | follow | 826 | 17 | -3.45% | -4.32% | 361 | 14 | -3.66% | -6.37% |
| follow_lb300_move10c_h30 | follow | 208 | 16 | -3.61% | -4.47% | 50 | 10 | -6.45% | -14.44% |
| follow_lb300_move5c_h60 | follow | 494 | 17 | -4.15% | -4.51% | 190 | 14 | -5.33% | -9.03% |
| follow_lb300_move5c_h120 | follow | 485 | 15 | -4.48% | -5.07% | 192 | 13 | -5.40% | -9.33% |

## Interpretation

- YES+NO buy-both is only capital-relevant when the fee-adjusted edge is positive. Near-arb rows are useful for hedging research, not guaranteed profit.
- Price-shock rules are executable taker proxies using visible ask for entry and future bid for exit, minus sports fee friction.
- This is still not a live bot proof: the audit has no authenticated fill logs, no queue position, and no game-event ground truth.
