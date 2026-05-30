# Telonex Strategy Bucket Audit

- Generated: 2026-05-30T19:46:35.020403+00:00
- Labels: 2,888,585
- Markets/tokens: 216 / 429
- Sports: {'baseball_mlb': 1731351, 'soccer': 1108317, 'basketball_wnba': 43570, 'icehockey_nhl': 5347}
- Label SHA256: `5b9a5be597a5a43da9f3717a5acb974a469886d8de4a2c2914c4b68612a64c28`
- Odds API feature coverage: 48.96%
- Odds API split coverage: `{'test': {'rows': 29156, 'matched_rows': 0, 'row_coverage': 0.0, 'markets': 33, 'matched_markets': 0}, 'train': {'rows': 2656035, 'matched_rows': 1337398, 'row_coverage': 0.5035317682184158, 'markets': 151, 'matched_markets': 70}, 'val': {'rows': 203394, 'matched_rows': 76762, 'row_coverage': 0.37740542985535463, 'markets': 32, 'matched_markets': 9}}`
- Minimum bucket rows/markets: 1000 / 5
- Positive test buckets total/taker/maker: 0 / 0 / 0
- Executable taker gate: False
- Maker research lead gate: False

This is a fixed-bucket audit, not a model-selection sweep. The buckets are meant to falsify broad strategy hypotheses before any threshold tuning.

## Price Buckets

| Side | split | price_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread |
|---|---|---|---:|---:|---:|---|---:|---:|---:|
| maker | test | 04 30-70c mid | 28,828 | 33 | -4.26% | -7.71% to -3.55% | 9.73% | 50.00% | 30.65% |
| taker | test | 04 30-70c mid | 28,828 | 33 | -49.18% | -75.92% to -37.46% | 0.00% | 50.00% | 30.65% |
| maker | train | 07 >=95c near_certain | 8,522 | 31 | -0.23% | -0.39% to -0.08% | 22.06% | 97.05% | 1.48% |
| maker | train | 06 85-95c favorite | 120,051 | 53 | -0.70% | -0.84% to -0.54% | 4.30% | 89.72% | 2.17% |
| maker | train | 05 70-85c high_mid | 266,064 | 94 | -1.50% | -1.68% to -1.37% | 1.91% | 77.65% | 4.82% |
| taker | train | 07 >=95c near_certain | 8,522 | 31 | -1.69% | -2.23% to -0.91% | 7.51% | 97.05% | 1.48% |
| maker | train | 04 30-70c mid | 1,864,943 | 142 | -3.05% | -3.10% to -2.99% | 3.51% | 50.00% | 9.37% |
| maker | val | 04 30-70c mid | 202,983 | 32 | -3.19% | -3.33% to -3.09% | 3.48% | 50.00% | 13.90% |
| taker | train | 06 85-95c favorite | 120,051 | 53 | -3.02% | -4.24% to -2.37% | 1.10% | 89.72% | 2.17% |
| maker | train | 03 15-30c low_mid | 267,622 | 94 | -4.90% | -5.46% to -4.43% | 4.04% | 22.41% | 4.93% |
| maker | train | 02 5-15c longshot | 120,207 | 53 | -5.30% | -5.55% to -4.96% | 2.99% | 10.29% | 2.18% |
| taker | train | 05 70-85c high_mid | 266,064 | 94 | -7.34% | -10.35% to -5.36% | 0.61% | 77.65% | 4.82% |
| maker | train | 01 3-5c thin_tail | 5,560 | 30 | -5.33% | -10.92% to 2.87% | 10.59% | 3.93% | 1.97% |
| maker | train | 00 <=3c dust | 3,066 | 24 | 1.48% | -11.14% to 19.17% | 16.73% | 1.26% | 0.60% |
| taker | train | 04 30-70c mid | 1,864,943 | 142 | -19.67% | -23.75% to -15.81% | 0.28% | 50.00% | 9.37% |
| taker | train | 03 15-30c low_mid | 267,622 | 94 | -24.04% | -30.90% to -19.04% | 0.36% | 22.41% | 4.93% |
| taker | train | 02 5-15c longshot | 120,207 | 53 | -23.86% | -31.44% to -20.41% | 0.71% | 10.29% | 2.18% |
| taker | val | 04 30-70c mid | 202,983 | 32 | -26.82% | -37.95% to -18.84% | 0.06% | 50.00% | 13.90% |
| taker | train | 01 3-5c thin_tail | 5,560 | 30 | -44.45% | -50.09% to -23.23% | 2.00% | 3.93% | 1.97% |
| taker | train | 00 <=3c dust | 3,066 | 24 | -38.95% | -54.24% to -22.23% | 6.98% | 1.26% | 0.60% |

## Sport x Price Buckets

| Side | split | sport_family | price_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|
| maker | test | baseball_mlb | 04 30-70c mid | 28,828 | 33 | -4.26% | -7.71% to -3.55% | 9.73% | 50.00% | 30.65% |
| taker | test | baseball_mlb | 04 30-70c mid | 28,828 | 33 | -49.18% | -75.92% to -37.46% | 0.00% | 50.00% | 30.65% |
| maker | train | baseball_mlb | 07 >=95c near_certain | 4,340 | 27 | -0.18% | -0.46% to 0.01% | 36.06% | 97.93% | 0.72% |
| maker | train | soccer | 06 85-95c favorite | 114,837 | 20 | -0.70% | -0.84% to -0.56% | 2.68% | 89.70% | 2.21% |
| taker | train | baseball_mlb | 07 >=95c near_certain | 4,340 | 27 | -0.89% | -1.19% to -0.67% | 14.75% | 97.93% | 0.72% |
| maker | train | baseball_mlb | 06 85-95c favorite | 5,180 | 32 | -0.70% | -1.22% to -0.25% | 40.17% | 90.22% | 1.12% |
| maker | train | soccer | 05 70-85c high_mid | 234,653 | 43 | -1.45% | -1.64% to -1.33% | 1.24% | 78.12% | 3.83% |
| taker | train | baseball_mlb | 06 85-95c favorite | 5,180 | 32 | -1.89% | -2.42% to -1.44% | 25.41% | 90.22% | 1.12% |
| maker | train | baseball_mlb | 05 70-85c high_mid | 25,223 | 49 | -2.03% | -2.78% to -1.53% | 8.42% | 73.67% | 13.87% |
| maker | train | soccer | 04 30-70c mid | 398,902 | 47 | -2.89% | -3.06% to -2.75% | 1.23% | 50.06% | 6.13% |
| maker | train | baseball_mlb | 04 30-70c mid | 1,429,674 | 85 | -3.10% | -3.15% to -3.06% | 4.15% | 49.98% | 9.53% |
| maker | val | baseball_mlb | 04 30-70c mid | 202,147 | 31 | -3.19% | -3.33% to -3.08% | 3.48% | 50.00% | 13.72% |
| taker | train | soccer | 06 85-95c favorite | 114,837 | 20 | -3.06% | -4.23% to -2.50% | 0.01% | 89.70% | 2.21% |
| maker | train | baseball_mlb | 03 15-30c low_mid | 25,700 | 49 | -2.35% | -4.31% to 2.91% | 22.41% | 26.40% | 14.21% |
| maker | train | icehockey_nhl | 04 30-70c mid | 5,347 | 8 | -3.31% | -5.39% to -3.25% | 2.13% | 50.01% | 27.25% |
| maker | train | soccer | 02 5-15c longshot | 115,026 | 20 | -5.33% | -5.50% to -5.21% | 1.80% | 10.32% | 2.22% |
| maker | train | soccer | 03 15-30c low_mid | 235,628 | 43 | -5.18% | -5.81% to -4.79% | 2.02% | 21.93% | 3.90% |
| taker | train | soccer | 05 70-85c high_mid | 234,653 | 43 | -6.09% | -8.31% to -4.84% | 0.01% | 78.12% | 3.83% |
| maker | train | baseball_mlb | 02 5-15c longshot | 5,147 | 32 | -4.61% | -8.97% to -0.13% | 29.75% | 9.81% | 1.11% |
| maker | train | baseball_mlb | 00 <=3c dust | 3,066 | 24 | 1.48% | -11.14% to 19.17% | 16.73% | 1.26% | 0.60% |

## Horizon x Spread Buckets

| Side | split | horizon_sec | spread_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|
| maker | test | 60 | 04 >10c | 4,612 | 33 | -3.41% | -4.97% to -0.97% | 8.82% | 50.00% | 40.12% |
| maker | test | 30 | 04 >10c | 4,629 | 33 | -3.30% | -5.41% to -0.50% | 6.80% | 50.00% | 40.72% |
| maker | test | 120 | 04 >10c | 4,656 | 33 | -3.52% | -6.13% to -1.60% | 11.17% | 50.00% | 39.98% |
| maker | test | 300 | 04 >10c | 4,326 | 33 | -3.69% | -7.73% to -2.73% | 14.68% | 50.00% | 37.26% |
| maker | test | 30 | 02 3-5c | 1,010 | 6 | -3.80% | -9.60% to -3.20% | 0.00% | 49.63% | 4.02% |
| maker | test | 300 | 02 3-5c | 1,101 | 6 | -4.40% | -9.62% to -3.27% | 0.09% | 49.36% | 4.05% |
| maker | test | 900 | 04 >10c | 3,960 | 33 | -3.76% | -11.77% to -2.34% | 23.01% | 50.00% | 35.02% |
| taker | test | 300 | 02 3-5c | 1,101 | 6 | -11.94% | -17.37% to -10.72% | 0.00% | 49.36% | 4.05% |
| taker | test | 30 | 02 3-5c | 1,010 | 6 | -11.29% | -17.45% to -10.63% | 0.00% | 49.63% | 4.02% |
| taker | test | 900 | 04 >10c | 3,960 | 33 | -53.69% | -80.27% to -40.43% | 0.00% | 50.00% | 35.02% |
| taker | test | 120 | 04 >10c | 4,656 | 33 | -58.64% | -81.24% to -44.57% | 0.00% | 50.00% | 39.98% |
| taker | test | 300 | 04 >10c | 4,326 | 33 | -55.98% | -81.55% to -43.10% | 0.00% | 50.00% | 37.26% |
| taker | test | 60 | 04 >10c | 4,612 | 33 | -58.73% | -82.72% to -44.03% | 0.00% | 50.00% | 40.12% |
| taker | test | 30 | 04 >10c | 4,629 | 33 | -59.27% | -84.31% to -45.54% | 0.00% | 50.00% | 40.72% |
| maker | train | 30 | 01 1-3c | 283,526 | 125 | -2.53% | -2.67% to -2.38% | 0.63% | 49.62% | 1.31% |
| maker | train | 60 | 01 1-3c | 279,810 | 127 | -2.54% | -2.68% to -2.40% | 0.86% | 49.62% | 1.31% |
| maker | train | 300 | 01 1-3c | 282,575 | 126 | -2.55% | -2.68% to -2.40% | 1.52% | 49.59% | 1.31% |
| maker | train | 120 | 01 1-3c | 277,111 | 126 | -2.55% | -2.69% to -2.41% | 1.17% | 49.61% | 1.31% |
| maker | train | 900 | 01 1-3c | 277,677 | 125 | -2.57% | -2.70% to -2.41% | 2.10% | 49.58% | 1.31% |
| maker | train | 30 | 02 3-5c | 52,123 | 124 | -2.47% | -2.77% to -2.15% | 1.69% | 53.50% | 3.85% |

## Odds Edge Buckets

| Side | split | odds_edge_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread |
|---|---|---|---:|---:|---:|---|---:|---:|---:|
| maker | train | 00 <=-10c against | 17,498 | 38 | -0.83% | -1.56% to -0.25% | 38.76% | 82.22% | 1.07% |
| maker | train | 03 -2c-+2c neutral | 876,038 | 69 | -2.50% | -2.81% to -2.22% | 0.44% | 52.25% | 1.39% |
| maker | train | 02 -5c--2c against | 80,986 | 53 | -2.31% | -2.88% to -1.89% | 0.84% | 61.07% | 1.64% |
| maker | val | 03 -2c-+2c neutral | 63,071 | 9 | -2.90% | -3.02% to -2.75% | 0.13% | 50.85% | 1.32% |
| maker | train | 01 -10c--5c against | 27,136 | 42 | -2.63% | -3.18% to -2.02% | 2.87% | 55.57% | 1.37% |
| maker | train | 04 +2c-+5c edge | 255,518 | 66 | -3.16% | -3.53% to -2.75% | 1.18% | 39.75% | 2.10% |
| maker | val | 04 +2c-+5c edge | 12,677 | 9 | -3.23% | -3.59% to -2.91% | 0.83% | 45.48% | 2.10% |
| maker | train | 05 +5c-+10c edge | 50,059 | 57 | -3.30% | -3.66% to -2.99% | 2.91% | 43.87% | 4.20% |
| maker | train | 06 >+10c edge | 30,163 | 49 | -3.62% | -5.08% to -2.37% | 18.29% | 28.26% | 8.57% |
| taker | train | 03 -2c-+2c neutral | 875,976 | 69 | -5.50% | -5.81% to -5.25% | 0.14% | 47.75% | 1.39% |
| taker | val | 03 -2c-+2c neutral | 63,071 | 9 | -5.56% | -6.38% to -4.95% | 0.07% | 49.15% | 1.32% |
| taker | train | 02 -5c--2c against | 255,371 | 67 | -5.45% | -7.03% to -4.48% | 0.20% | 60.25% | 2.09% |
| taker | val | 02 -5c--2c against | 12,677 | 9 | -6.38% | -7.89% to -4.63% | 0.08% | 54.52% | 2.10% |
| taker | train | 05 +5c-+10c edge | 27,136 | 42 | -6.25% | -8.60% to -5.46% | 1.88% | 44.43% | 1.37% |
| taker | train | 04 +2c-+5c edge | 80,986 | 53 | -7.44% | -9.20% to -6.01% | 0.62% | 38.93% | 1.64% |
| taker | train | 06 >+10c edge | 17,498 | 38 | -10.48% | -13.51% to -7.44% | 15.29% | 17.78% | 1.07% |
| taker | train | 01 -10c--5c against | 50,268 | 57 | -9.64% | -14.76% to -6.83% | 1.23% | 56.11% | 4.22% |
| taker | train | 00 <=-10c against | 30,163 | 49 | -12.52% | -21.17% to -3.78% | 14.99% | 71.74% | 8.57% |

## Sport x Odds Edge Buckets

| Side | split | sport_family | odds_edge_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|
| maker | train | baseball_mlb | 00 <=-10c against | 17,494 | 37 | -0.82% | -1.58% to -0.27% | 38.77% | 82.22% | 1.07% |
| maker | train | soccer | 03 -2c-+2c neutral | 381,768 | 16 | -1.97% | -2.47% to -1.60% | 0.38% | 55.02% | 1.61% |
| maker | train | soccer | 02 -5c--2c against | 36,824 | 10 | -1.81% | -2.54% to -1.46% | 0.11% | 70.77% | 1.75% |
| maker | train | baseball_mlb | 03 -2c-+2c neutral | 473,248 | 51 | -2.95% | -3.00% to -2.90% | 0.49% | 50.18% | 1.20% |
| maker | train | baseball_mlb | 02 -5c--2c against | 44,162 | 43 | -2.87% | -3.02% to -2.70% | 1.45% | 52.97% | 1.55% |
| maker | val | baseball_mlb | 03 -2c-+2c neutral | 63,071 | 9 | -2.90% | -3.03% to -2.77% | 0.13% | 50.85% | 1.32% |
| maker | train | baseball_mlb | 01 -10c--5c against | 27,066 | 41 | -2.62% | -3.17% to -2.06% | 2.87% | 55.51% | 1.35% |
| maker | train | baseball_mlb | 04 +2c-+5c edge | 91,643 | 48 | -3.07% | -3.20% to -2.92% | 1.52% | 48.10% | 1.99% |
| maker | train | soccer | 06 >+10c edge | 10,184 | 7 | -3.16% | -3.59% to -0.74% | 5.34% | 42.49% | 21.30% |
| maker | val | baseball_mlb | 04 +2c-+5c edge | 12,677 | 9 | -3.23% | -3.62% to -2.92% | 0.83% | 45.48% | 2.10% |
| maker | train | baseball_mlb | 05 +5c-+10c edge | 41,666 | 46 | -3.22% | -3.65% to -2.90% | 3.02% | 45.75% | 2.49% |
| maker | train | soccer | 04 +2c-+5c edge | 158,127 | 16 | -3.28% | -3.95% to -2.45% | 0.92% | 34.33% | 2.08% |
| maker | train | soccer | 05 +5c-+10c edge | 8,327 | 9 | -3.92% | -4.60% to -3.50% | 2.28% | 34.26% | 12.74% |
| taker | train | baseball_mlb | 00 <=-10c against | 19,979 | 42 | -3.42% | -4.96% to -2.25% | 22.63% | 79.00% | 2.07% |
| taker | train | baseball_mlb | 03 -2c-+2c neutral | 473,186 | 51 | -5.26% | -5.47% to -5.11% | 0.25% | 49.82% | 1.20% |
| maker | train | baseball_mlb | 06 >+10c edge | 19,979 | 42 | -3.98% | -6.13% to -1.89% | 24.89% | 21.00% | 2.07% |
| taker | val | baseball_mlb | 03 -2c-+2c neutral | 63,071 | 9 | -5.56% | -6.30% to -5.02% | 0.07% | 49.15% | 1.32% |
| taker | train | soccer | 02 -5c--2c against | 158,127 | 16 | -4.78% | -6.90% to -3.58% | 0.00% | 65.67% | 2.08% |
| taker | train | soccer | 03 -2c-+2c neutral | 381,768 | 16 | -5.84% | -6.96% to -5.26% | 0.00% | 44.98% | 1.61% |
| taker | train | baseball_mlb | 04 +2c-+5c edge | 44,162 | 43 | -6.27% | -7.30% to -5.57% | 1.12% | 47.03% | 1.55% |

## Verdict

No predeclared test bucket cleared a positive cluster-bootstrap CI lower bound. Current Telonex data does not support live capital for maker/taker price-bucket strategies.
