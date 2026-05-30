# Favorite-Longshot Bias Audit

- Generated: 2026-05-30T22:36:24.993368+00:00
- Bucket 1 raw edge gate: True
- Bucket 1 robust CI gate: False
- Stop sequence at Bucket 1: True
- Primary candidate: favorite_85_95_buy_yes
- Capital gate: False
- Verdict: PIVOT: favorite-longshot bias has raw positive pockets; build executable validation next
- Reasons: capital remains blocked until the bucket survives executable bid/ask, spread, latency, and market-disjoint validation; no favorite-longshot bucket has a positive 95% event-cluster bootstrap lower bound yet; Telonex clear-settlement sample is too small in tail buckets for executable validation

## Source Coverage

- Legacy observations: 25,409 contracts / 5,068 events from 41 files
- Legacy conflicting rows dropped: 2,102
- Telonex clear-settlement CLOB: 40 contracts / 20 markets
- Telonex note: Settlement is inferred only when the final CLOB midpoint clearly has one token near 1 and the rest near 0.

## Legacy Observation Price Buckets

| Bucket | Contracts | Events | Avg obs | Actual | Avg price | Edge | Buy YES ROI | Buy NO ROI | Fee-adj YES | Fee-adj NO |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 01 5-10c | 74 | 74 | 4.91 | 10.81% | 8.97% | 1.84% | 20.55% | -2.02% | 20.25% | -2.26% |
| 02 10-15c | 336 | 334 | 5.64 | 11.90% | 12.80% | -0.90% | -7.02% | 1.03% | -7.34% | 0.69% |
| 03 15-25c | 1,392 | 1,171 | 5.70 | 21.26% | 20.84% | 0.43% | 2.05% | -0.54% | 1.54% | -1.03% |
| 04 25-40c | 3,737 | 2,835 | 5.57 | 33.42% | 32.94% | 0.48% | 1.47% | -0.72% | 0.80% | -1.38% |
| 05 40-60c | 16,778 | 3,992 | 4.38 | 50.10% | 49.98% | 0.11% | 0.22% | -0.22% | -0.53% | -0.97% |
| 06 60-75c | 2,438 | 2,264 | 5.37 | 63.86% | 65.54% | -1.67% | -2.55% | 4.85% | -3.21% | 4.14% |
| 07 75-85c | 504 | 501 | 5.19 | 78.17% | 79.22% | -1.04% | -1.32% | 5.02% | -1.81% | 4.51% |
| 08 85-90c | 143 | 143 | 5.44 | 90.21% | 87.56% | 2.65% | 3.03% | -21.32% | 2.69% | -21.58% |
| 09 90-95c | 7 | 7 | 4.00 | 100.00% | 90.39% | 9.61% | 10.63% | -100.00% | 10.34% | -100.00% |

## Predeclared Buckets

| Bucket | Direction | Source | Contracts | Events | Actual | Avg price | Raw edge | Raw ROI | Fee-adj ROI | 95% CI | Raw gate | Robust gate |
|---|---|---|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|
| longshot_05_15_buy_no | buy_no | legacy_observations | 410 | 384 | 11.71% | 12.11% | 0.40% | 0.46% | 0.14% | -3.38% to 3.64% | True | False |
| longshot_10_15_buy_no | buy_no | legacy_observations | 336 | 334 | 11.90% | 12.80% | 0.90% | 1.03% | 0.69% | -3.44% to 4.58% | True | False |
| favorite_75_92_buy_yes | buy_yes | legacy_observations | 654 | 649 | 81.04% | 81.16% | -0.12% | -0.15% | -0.61% | -4.20% to 2.93% | False | False |
| favorite_85_95_buy_yes | buy_yes | legacy_observations | 150 | 150 | 90.67% | 87.69% | 2.98% | 3.40% | 3.06% | -2.95% to 8.25% | True | False |
| longshot_05_15_buy_no | buy_no | telonex_clear_settlement | 0 | 0 | n/a | n/a | n/a | n/a | n/a | n/a to n/a | False | False |
| longshot_10_15_buy_no | buy_no | telonex_clear_settlement | 0 | 0 | n/a | n/a | n/a | n/a | n/a | n/a to n/a | False | False |
| favorite_75_92_buy_yes | buy_yes | telonex_clear_settlement | 0 | 0 | n/a | n/a | n/a | n/a | n/a | n/a to n/a | False | False |
| favorite_85_95_buy_yes | buy_yes | telonex_clear_settlement | 0 | 0 | n/a | n/a | n/a | n/a | n/a | n/a to n/a | False | False |

## Telonex Clear-Settlement Buckets

| Bucket | Contracts | Markets | Avg minutes | Actual | Avg price | Edge | Buy YES ROI | Buy NO ROI |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| 04 25-40c | 5 | 5 | 2924.80 | 0.00% | 36.60% | -36.60% | -100.00% | 57.72% |
| 05 40-60c | 30 | 15 | 3435.47 | 50.00% | 50.00% | 0.00% | 0.00% | 0.00% |
| 06 60-75c | 5 | 5 | 2924.80 | 100.00% | 63.40% | 36.60% | 57.72% | -100.00% |

## Interpretation

- Bucket 1 is the first raw-positive pivot: the passive maker target stays dead, and the next model target should be favorite/longshot regime selection plus executable taker/limit-entry validation.
- The broad 75-92c favorite bucket does not pass in the legacy observations; the positive favorite pocket is narrower at 85-95c.
- The 10-15c longshot fade is positive but thin after fee assumptions, so spread and fill checks may erase it.
- This is not yet a profitable-bot claim because the legacy source lacks executable bid/ask depth and the Telonex clear-settlement sample is too small in the target tails.
