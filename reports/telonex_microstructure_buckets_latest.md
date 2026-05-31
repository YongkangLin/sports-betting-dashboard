# Telonex Microstructure Bucket Audit

- Generated: 2026-05-31T15:13:47.591677+00:00
- Labels: 5,768,529 rows, 725 markets, 1,436 tokens
- Label SHA256: `8cdfb7cda52ff8ab59d31872381cd6a64e65df78ed427febd3caff5f3a59ee39`
- Overall gate: False
- Gate reasons: YES+NO strict fee-adjusted arbitrage gate failed, no price-shock rule had enough validation rows/markets for CI

## YES+NO Underpricing

- Unique paired snapshots: 574,623
- Near buy-both rows (`ask_yes + ask_no <= 1.02`): 443,919 across 639 markets
- Strict gross buy-both rows: 0
- Strict fee-adjusted buy-both rows: 0
- Minimum ask sum / max net edge: 1.0 / -2.9970000000000026e-05
- Gate: False (no fee-adjusted YES+NO arbitrage in labels)

## Price-Shock Fade/Follow

- Gate: False
- Selected by validation: none

## Top Validation Rules

| Rule | Strategy | Val rows | Val markets | Val ROI | Val CI low | Test rows | Test markets | Test ROI | Test CI low |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|
| follow_lb900_move5c_h30 | follow | 895 | 21 | -3.08% | -3.35% | 592 | 21 | -3.72% | -4.84% |
| follow_lb900_move10c_h30 | follow | 520 | 18 | -2.96% | -3.40% | 305 | 15 | -3.44% | -4.92% |
| follow_lb300_move5c_h30 | follow | 532 | 22 | -3.36% | -3.72% | 312 | 19 | -5.08% | -6.89% |
| follow_lb900_move10c_h60 | follow | 511 | 18 | -3.25% | -3.79% | 301 | 14 | -3.10% | -4.52% |
| follow_lb900_move5c_h60 | follow | 882 | 19 | -3.35% | -3.88% | 592 | 21 | -3.54% | -4.96% |
| follow_lb300_move10c_h30 | follow | 237 | 19 | -3.45% | -4.18% | 89 | 14 | -5.59% | -8.84% |
| follow_lb300_move5c_h60 | follow | 524 | 20 | -3.87% | -4.31% | 311 | 19 | -4.83% | -6.89% |
| follow_lb900_move5c_h120 | follow | 867 | 19 | -3.54% | -4.32% | 586 | 19 | -3.16% | -4.70% |
| follow_lb900_move10c_h120 | follow | 502 | 16 | -3.55% | -4.56% | 301 | 14 | -2.23% | -3.53% |
| follow_lb300_move10c_h60 | follow | 233 | 18 | -4.06% | -4.91% | 87 | 12 | -4.95% | -7.96% |

## Interpretation

- YES+NO buy-both is only capital-relevant when the fee-adjusted edge is positive. Near-arb rows are useful for hedging research, not guaranteed profit.
- Price-shock rules are executable taker proxies using visible ask for entry and future bid for exit, minus sports fee friction.
- This is still not a live bot proof: the audit has no authenticated fill logs, no queue position, and no game-event ground truth.
