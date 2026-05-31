# Telonex Strategy Bucket Audit

- Generated: 2026-05-31T13:43:37.149055+00:00
- Labels: 2,888,585
- Markets/tokens: 216 / 429
- Sports: {'baseball_mlb': 1731351, 'soccer': 1108317, 'basketball_wnba': 43570, 'icehockey_nhl': 5347}
- Label SHA256: `32537f0d3b561eb1f7a39bcb5ed6ad4834d6f854a4443683da29c657d09f223b`
- Odds API feature coverage: 48.13%
- Odds API split coverage: `{'test': {'rows': 226224, 'matched_rows': 73398, 'row_coverage': 0.3244483343942287, 'markets': 18, 'matched_markets': 5}, 'train': {'rows': 1776863, 'matched_rows': 913326, 'row_coverage': 0.5140103654586763, 'markets': 75, 'matched_markets': 44}, 'unobserved': {'rows': 539748, 'matched_rows': 229330, 'row_coverage': 0.4248834641351149, 'markets': 107, 'matched_markets': 24}, 'val': {'rows': 345750, 'matched_rows': 174092, 'row_coverage': 0.5035198843094721, 'markets': 16, 'matched_markets': 6}}`
- Player/news feature coverage: 0.00% / status `missing_public_timestamped_feed`
- Play-by-play feature coverage: 52.27% / status `available`
- Sentiment feature coverage: 0.00% / status `missing_feature_file`
- Minimum bucket rows/markets: 1000 / 5
- Positive test buckets total/taker/maker: 0 / 0 / 0
- Executable taker gate: False
- Maker research lead gate: False

This is a fixed-bucket audit, not a model-selection sweep. The buckets are meant to falsify broad strategy hypotheses before any threshold tuning.

## Price Buckets

| Side | split | price_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 06 85-95c favorite | 2,038 | 6 | -1.05% | -1.69% to -0.42% | 9.81% | 87.25% | 2.80% | -43.44% | -1.66% | 0.00% |
| maker | test | 05 70-85c high_mid | 33,613 | 14 | -1.44% | -1.74% to -1.21% | 2.79% | 78.74% | 5.02% | -11.95% | -1.70% | 0.00% |
| maker | test | 04 30-70c mid | 148,133 | 17 | -3.05% | -3.28% to -2.86% | 2.45% | 50.09% | 13.20% | -0.88% | 0.00% | 0.00% |
| taker | test | 06 85-95c favorite | 2,038 | 6 | -4.11% | -5.75% to -1.67% | 4.86% | 87.25% | 2.80% | -43.44% | -1.66% | 0.00% |
| maker | test | 03 15-30c low_mid | 34,252 | 14 | -5.57% | -6.69% to -4.88% | 3.29% | 21.44% | 5.22% | 8.39% | 1.53% | 0.00% |
| maker | test | 02 5-15c longshot | 2,032 | 6 | -3.54% | -7.67% to 2.65% | 22.98% | 13.03% | 2.90% | 42.42% | 1.66% | 0.00% |
| taker | test | 05 70-85c high_mid | 33,613 | 14 | -7.43% | -11.65% to -5.00% | 0.34% | 78.74% | 5.02% | -11.95% | -1.70% | 0.00% |
| taker | test | 02 5-15c longshot | 2,032 | 6 | -23.31% | -29.19% to -8.13% | 3.69% | 13.03% | 2.90% | 42.42% | 1.66% | 0.00% |
| taker | test | 03 15-30c low_mid | 34,252 | 14 | -26.42% | -33.65% to -19.69% | 0.18% | 21.44% | 5.22% | 8.39% | 1.53% | 0.00% |
| taker | test | 04 30-70c mid | 148,133 | 17 | -25.62% | -41.72% to -11.91% | 0.08% | 50.09% | 13.20% | -0.88% | 0.00% | 0.00% |
| maker | train | 07 >=95c near_certain | 3,682 | 25 | -0.25% | -0.57% to -0.04% | 34.00% | 97.92% | 0.75% | -44.03% | -1.23% | 0.00% |
| maker | val | 06 85-95c favorite | 55,201 | 10 | -0.54% | -0.69% to -0.45% | 3.27% | 91.84% | 1.89% | -2.24% | -0.11% | 0.00% |
| maker | train | 06 85-95c favorite | 62,661 | 35 | -0.85% | -1.04% to -0.75% | 4.94% | 87.94% | 2.40% | -4.54% | -0.30% | 0.00% |
| taker | train | 07 >=95c near_certain | 3,682 | 25 | -0.99% | -1.34% to -0.73% | 14.07% | 97.92% | 0.75% | -44.03% | -1.23% | 0.00% |
| maker | train | 05 70-85c high_mid | 212,110 | 61 | -1.52% | -1.73% to -1.38% | 1.83% | 77.49% | 5.01% | -3.63% | -0.19% | 0.00% |
| maker | val | 05 70-85c high_mid | 20,087 | 14 | -1.43% | -2.26% to -1.09% | 1.20% | 77.59% | 2.49% | -26.47% | -6.14% | 0.00% |
| maker | train | 04 30-70c mid | 1,218,891 | 70 | -3.04% | -3.11% to -2.98% | 3.88% | 49.99% | 9.85% | -0.84% | -0.00% | 0.00% |
| maker | val | 04 30-70c mid | 191,531 | 13 | -2.94% | -3.19% to -2.75% | 2.00% | 50.01% | 6.56% | -0.73% | 0.00% | 0.00% |
| maker | unobserved | 04 30-70c mid | 538,199 | 107 | -3.21% | -3.29% to -3.14% | 3.81% | 50.00% | 11.09% | -0.73% | 0.00% | 0.00% |
| taker | val | 06 85-95c favorite | 55,201 | 10 | -2.51% | -3.74% to -1.91% | 0.12% | 91.84% | 1.89% | -2.24% | -0.11% | 0.00% |

## Sport x Price Buckets

| Side | split | sport_family | price_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | soccer | 05 70-85c high_mid | 31,824 | 10 | -1.44% | -1.74% to -1.20% | 2.52% | 79.12% | 5.05% | n/a | n/a | 0.00% |
| maker | test | baseball_mlb | 04 30-70c mid | 80,164 | 5 | -3.03% | -3.15% to -2.90% | 2.54% | 50.01% | 4.16% | -0.83% | -0.00% | 0.00% |
| maker | test | soccer | 04 30-70c mid | 38,941 | 11 | -3.24% | -3.70% to -2.50% | 1.80% | 50.28% | 12.89% | n/a | n/a | 0.00% |
| maker | test | soccer | 03 15-30c low_mid | 32,323 | 10 | -5.61% | -6.81% to -4.82% | 3.08% | 21.04% | 5.28% | n/a | n/a | 0.00% |
| taker | test | soccer | 05 70-85c high_mid | 31,824 | 10 | -7.44% | -11.96% to -4.96% | 0.03% | 79.12% | 5.05% | n/a | n/a | 0.00% |
| taker | test | baseball_mlb | 04 30-70c mid | 80,164 | 5 | -10.78% | -17.73% to -6.38% | 0.12% | 50.01% | 4.16% | -0.83% | -0.00% | 0.00% |
| taker | test | soccer | 03 15-30c low_mid | 32,323 | 10 | -27.01% | -35.02% to -19.19% | 0.08% | 21.04% | 5.28% | n/a | n/a | 0.00% |
| taker | test | soccer | 04 30-70c mid | 38,941 | 11 | -25.23% | -46.80% to -17.42% | 0.03% | 50.28% | 12.89% | n/a | n/a | 0.00% |
| maker | train | baseball_mlb | 07 >=95c near_certain | 3,658 | 24 | -0.25% | -0.58% to -0.03% | 34.14% | 97.93% | 0.74% | -44.03% | -1.23% | 0.00% |
| maker | val | soccer | 06 85-95c favorite | 55,051 | 8 | -0.54% | -0.71% to -0.46% | 3.12% | 91.84% | 1.89% | -1.98% | -0.00% | 0.00% |
| maker | train | soccer | 06 85-95c favorite | 58,172 | 8 | -0.85% | -1.04% to -0.80% | 2.28% | 87.77% | 2.49% | -0.92% | -0.00% | 0.00% |
| maker | train | baseball_mlb | 06 85-95c favorite | 4,455 | 26 | -0.80% | -1.33% to -0.33% | 39.35% | 90.12% | 1.12% | -37.66% | -2.78% | 0.00% |
| taker | train | baseball_mlb | 07 >=95c near_certain | 3,658 | 24 | -0.98% | -1.36% to -0.72% | 14.16% | 97.93% | 0.74% | -44.03% | -1.23% | 0.00% |
| maker | train | soccer | 05 70-85c high_mid | 183,053 | 24 | -1.46% | -1.70% to -1.32% | 1.06% | 78.00% | 3.78% | -3.01% | -0.00% | 0.00% |
| maker | val | soccer | 05 70-85c high_mid | 19,776 | 9 | -1.39% | -1.76% to -1.06% | 0.79% | 77.62% | 2.31% | -5.83% | n/a | 0.00% |
| taker | train | baseball_mlb | 06 85-95c favorite | 4,455 | 26 | -1.99% | -2.53% to -1.53% | 24.96% | 90.12% | 1.12% | -37.66% | -2.78% | 0.00% |
| maker | train | baseball_mlb | 05 70-85c high_mid | 23,581 | 36 | -1.99% | -2.75% to -1.41% | 8.00% | 73.68% | 14.34% | -9.28% | -1.30% | 0.00% |
| maker | train | soccer | 04 30-70c mid | 285,136 | 27 | -2.90% | -3.05% to -2.76% | 1.26% | 50.05% | 5.50% | -1.12% | 0.00% | 0.00% |
| maker | train | baseball_mlb | 04 30-70c mid | 931,763 | 42 | -3.09% | -3.15% to -3.03% | 4.68% | 49.97% | 11.05% | -0.69% | -0.00% | 0.00% |
| maker | val | baseball_mlb | 04 30-70c mid | 116,873 | 5 | -3.12% | -3.20% to -3.08% | 2.77% | 50.01% | 7.58% | -0.77% | 0.00% | 0.00% |

## Horizon x Spread Buckets

| Side | split | horizon_sec | spread_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 900 | 02 3-5c | 5,015 | 18 | -2.42% | -2.77% to -1.99% | 5.46% | 52.71% | 3.94% | -2.22% | 0.01% | 0.00% |
| maker | test | 300 | 02 3-5c | 5,186 | 18 | -2.43% | -2.78% to -1.94% | 3.34% | 52.80% | 3.95% | -2.25% | -0.00% | 0.00% |
| maker | test | 30 | 02 3-5c | 5,163 | 18 | -2.42% | -2.78% to -1.86% | 3.49% | 52.23% | 3.97% | -2.22% | 0.01% | 0.00% |
| maker | test | 60 | 01 1-3c | 21,901 | 17 | -2.49% | -2.81% to -2.10% | 0.76% | 50.37% | 1.42% | -0.77% | -0.01% | 0.00% |
| maker | test | 30 | 01 1-3c | 22,344 | 17 | -2.48% | -2.82% to -2.04% | 0.59% | 50.36% | 1.43% | -0.78% | -0.01% | 0.00% |
| maker | test | 120 | 01 1-3c | 21,663 | 17 | -2.49% | -2.83% to -2.05% | 1.01% | 50.40% | 1.42% | -0.77% | -0.01% | 0.00% |
| maker | test | 60 | 02 3-5c | 5,171 | 18 | -2.49% | -2.83% to -1.96% | 3.19% | 52.14% | 3.97% | -2.25% | 0.00% | 0.00% |
| maker | test | 300 | 01 1-3c | 21,996 | 17 | -2.49% | -2.84% to -2.09% | 1.36% | 50.29% | 1.43% | -0.78% | -0.01% | 0.00% |
| maker | test | 120 | 02 3-5c | 5,008 | 18 | -2.54% | -2.85% to -1.99% | 3.25% | 52.07% | 3.98% | -2.27% | -0.00% | 0.00% |
| maker | test | 900 | 01 1-3c | 21,673 | 17 | -2.52% | -2.87% to -2.07% | 2.05% | 50.28% | 1.43% | -0.78% | -0.02% | 0.00% |
| maker | test | 60 | 03 5-10c | 4,460 | 16 | -2.45% | -3.00% to -2.20% | 2.47% | 50.74% | 6.69% | -3.38% | -0.03% | 0.00% |
| maker | test | 30 | 03 5-10c | 4,640 | 16 | -2.44% | -3.00% to -2.19% | 1.72% | 50.74% | 6.70% | -3.38% | -0.04% | 0.00% |
| maker | test | 300 | 03 5-10c | 4,433 | 16 | -2.40% | -3.07% to -2.10% | 6.43% | 50.70% | 6.69% | -3.37% | -0.03% | 0.00% |
| maker | test | 120 | 03 5-10c | 4,461 | 16 | -2.49% | -3.09% to -2.21% | 3.56% | 50.72% | 6.70% | -3.37% | -0.04% | 0.00% |
| maker | test | 900 | 03 5-10c | 4,418 | 16 | -2.54% | -3.48% to -2.12% | 10.25% | 50.80% | 6.73% | -3.36% | -0.03% | 0.00% |
| maker | test | 60 | 00 <=1c | 3,085 | 14 | -3.06% | -3.76% to -2.69% | 1.07% | 42.81% | 0.99% | 0.98% | 0.08% | 0.00% |
| maker | test | 120 | 00 <=1c | 3,069 | 14 | -3.13% | -3.94% to -2.79% | 1.40% | 42.79% | 0.99% | 0.98% | 0.08% | 0.00% |
| maker | test | 30 | 00 <=1c | 3,102 | 13 | -3.07% | -3.96% to -2.70% | 0.71% | 42.62% | 0.99% | 0.99% | 0.08% | 0.00% |
| maker | test | 300 | 00 <=1c | 3,103 | 13 | -3.22% | -4.04% to -2.87% | 1.84% | 42.34% | 0.99% | 1.02% | 0.08% | 0.00% |
| maker | test | 900 | 04 >10c | 10,101 | 15 | -2.99% | -4.07% to -1.67% | 12.02% | 49.98% | 34.45% | -12.48% | 0.00% | 0.00% |

## Odds Edge Buckets

| Side | split | odds_edge_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 03 -2c-+2c neutral | 57,914 | 5 | -2.97% | -3.05% to -2.84% | 0.20% | 49.49% | 1.37% | -0.98% | -0.01% | 0.00% |
| maker | test | 04 +2c-+5c edge | 9,483 | 5 | -2.59% | -3.30% to -2.28% | 2.07% | 52.98% | 3.08% | -0.09% | 0.03% | 0.00% |
| taker | test | 03 -2c-+2c neutral | 57,914 | 5 | -5.47% | -6.22% to -4.97% | 0.08% | 50.51% | 1.37% | -0.39% | 0.01% | 0.00% |
| taker | test | 02 -5c--2c against | 9,483 | 5 | -9.27% | -11.26% to -7.23% | 0.01% | 47.02% | 3.08% | -2.98% | -0.03% | 0.00% |
| maker | train | 00 <=-10c against | 14,973 | 28 | -0.92% | -1.65% to -0.26% | 38.54% | 82.05% | 1.06% | -32.54% | -2.62% | 0.00% |
| maker | val | 02 -5c--2c against | 6,589 | 5 | -2.04% | -2.81% to -1.88% | 1.47% | 65.28% | 1.17% | -3.76% | -0.02% | 0.00% |
| maker | train | 03 -2c-+2c neutral | 570,904 | 44 | -2.47% | -2.84% to -2.17% | 0.52% | 51.58% | 1.47% | -1.12% | -0.01% | 0.00% |
| maker | unobserved | 01 -10c--5c against | 2,946 | 9 | -2.40% | -2.87% to 1.33% | 2.21% | 58.12% | 2.52% | -8.12% | -0.46% | 0.00% |
| maker | train | 02 -5c--2c against | 69,105 | 35 | -2.31% | -2.93% to -1.89% | 0.72% | 60.72% | 1.50% | -4.39% | -0.09% | 0.00% |
| maker | unobserved | 03 -2c-+2c neutral | 166,416 | 23 | -2.97% | -3.02% to -2.90% | 0.19% | 50.16% | 1.21% | -0.95% | -0.00% | 0.00% |
| maker | val | 03 -2c-+2c neutral | 102,173 | 6 | -1.85% | -3.06% to -1.04% | 0.41% | 60.54% | 1.23% | -1.39% | -0.00% | 0.00% |
| maker | unobserved | 02 -5c--2c against | 13,810 | 20 | -2.96% | -3.17% to -2.76% | 0.51% | 52.12% | 2.02% | -4.96% | -0.07% | 0.00% |
| maker | unobserved | 04 +2c-+5c edge | 35,777 | 22 | -3.04% | -3.27% to -2.83% | 0.63% | 48.56% | 1.67% | 1.49% | 0.03% | 0.00% |
| maker | train | 01 -10c--5c against | 16,709 | 27 | -2.54% | -3.39% to -1.67% | 3.43% | 56.14% | 1.17% | -7.85% | -0.28% | 0.00% |
| maker | train | 04 +2c-+5c edge | 182,496 | 43 | -3.06% | -3.56% to -2.58% | 1.37% | 42.22% | 2.21% | 0.93% | 0.05% | 0.00% |
| maker | unobserved | 05 +5c-+10c edge | 8,870 | 17 | -3.23% | -3.73% to -2.74% | 2.15% | 47.12% | 3.45% | 3.22% | 0.14% | 0.00% |
| maker | train | 05 +5c-+10c edge | 33,513 | 36 | -3.24% | -3.85% to -2.80% | 2.87% | 42.69% | 4.75% | 2.38% | 0.19% | 0.00% |
| maker | val | 05 +5c-+10c edge | 7,191 | 5 | -3.26% | -4.58% to -2.15% | 3.56% | 47.76% | 1.94% | 6.73% | -0.04% | 0.00% |
| maker | val | 04 +2c-+5c edge | 48,308 | 6 | -3.99% | -4.65% to -2.84% | 0.51% | 25.72% | 1.54% | 1.18% | 0.02% | 0.00% |
| taker | unobserved | 03 -2c-+2c neutral | 166,416 | 23 | -5.31% | -5.71% to -5.04% | 0.08% | 49.84% | 1.21% | -0.26% | 0.00% | 0.00% |

## Sport x Odds Edge Buckets

| Side | split | sport_family | odds_edge_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | train | baseball_mlb | 00 <=-10c against | 14,969 | 27 | -0.92% | -1.87% to -0.32% | 38.55% | 82.05% | 1.06% | -32.54% | -2.62% | 0.00% |
| maker | train | soccer | 03 -2c-+2c neutral | 318,996 | 14 | -2.14% | -2.68% to -1.78% | 0.42% | 52.63% | 1.68% | -1.34% | -0.00% | 0.00% |
| maker | unobserved | baseball_mlb | 01 -10c--5c against | 2,946 | 9 | -2.40% | -2.78% to 3.03% | 2.21% | 58.12% | 2.52% | -8.12% | -0.46% | 0.00% |
| maker | train | soccer | 02 -5c--2c against | 31,821 | 9 | -1.79% | -2.83% to -1.43% | 0.12% | 70.99% | 1.86% | -4.47% | -0.03% | 0.00% |
| maker | train | baseball_mlb | 03 -2c-+2c neutral | 243,823 | 29 | -2.91% | -2.98% to -2.83% | 0.65% | 50.40% | 1.19% | -0.83% | -0.01% | 0.00% |
| maker | unobserved | baseball_mlb | 03 -2c-+2c neutral | 166,416 | 23 | -2.97% | -3.02% to -2.90% | 0.19% | 50.16% | 1.21% | -0.95% | -0.00% | 0.00% |
| maker | train | baseball_mlb | 02 -5c--2c against | 37,284 | 26 | -2.92% | -3.15% to -2.68% | 1.23% | 51.95% | 1.19% | -4.32% | -0.12% | 0.00% |
| maker | unobserved | baseball_mlb | 02 -5c--2c against | 13,810 | 20 | -2.96% | -3.20% to -2.76% | 0.51% | 52.12% | 2.02% | -4.96% | -0.07% | 0.00% |
| maker | train | baseball_mlb | 04 +2c-+5c edge | 65,613 | 28 | -3.11% | -3.24% to -2.98% | 1.55% | 47.73% | 1.89% | 1.42% | 0.10% | 0.00% |
| maker | unobserved | baseball_mlb | 04 +2c-+5c edge | 35,777 | 22 | -3.04% | -3.26% to -2.82% | 0.63% | 48.56% | 1.67% | 1.49% | 0.03% | 0.00% |
| maker | train | baseball_mlb | 01 -10c--5c against | 16,639 | 26 | -2.53% | -3.37% to -1.43% | 3.44% | 56.05% | 1.14% | -7.83% | -0.28% | 0.00% |
| maker | train | soccer | 06 >+10c edge | 10,174 | 6 | -3.17% | -3.59% to -0.90% | 5.32% | 42.47% | 21.30% | -5.25% | 0.01% | 0.00% |
| taker | train | baseball_mlb | 00 <=-10c against | 15,452 | 28 | -2.45% | -3.61% to -1.63% | 25.35% | 81.34% | 1.29% | -31.93% | -2.65% | 0.00% |
| maker | train | baseball_mlb | 05 +5c-+10c edge | 25,088 | 27 | -3.11% | -3.76% to -2.56% | 3.11% | 45.31% | 2.09% | 5.22% | 0.21% | 0.00% |
| maker | unobserved | baseball_mlb | 05 +5c-+10c edge | 8,870 | 17 | -3.23% | -3.80% to -2.81% | 2.15% | 47.12% | 3.45% | 3.22% | 0.14% | 0.00% |
| maker | train | soccer | 04 +2c-+5c edge | 115,428 | 14 | -3.06% | -3.87% to -2.25% | 1.21% | 38.72% | 2.36% | 0.68% | 0.01% | 0.00% |
| maker | train | soccer | 05 +5c-+10c edge | 8,259 | 8 | -3.95% | -4.70% to -3.61% | 2.23% | 34.06% | 12.78% | -6.18% | 0.02% | 0.00% |
| taker | train | baseball_mlb | 03 -2c-+2c neutral | 243,755 | 29 | -5.25% | -5.51% to -5.07% | 0.38% | 49.60% | 1.19% | -0.36% | 0.01% | 0.00% |
| taker | unobserved | baseball_mlb | 03 -2c-+2c neutral | 166,416 | 23 | -5.31% | -5.71% to -5.03% | 0.08% | 49.84% | 1.21% | -0.26% | 0.00% | 0.00% |
| taker | train | baseball_mlb | 04 +2c-+5c edge | 37,284 | 26 | -5.44% | -6.05% to -4.97% | 1.10% | 48.05% | 1.19% | 3.12% | 0.12% | 0.00% |

## Predeclared Strategy Support

| Split | Strategy | Rows | Markets | Reportable | ROI | Positive | Odds gap | Line-lag gap | Reason |
|---|---|---:|---:|---|---:|---:|---:|---:|---|
| train | favorite_longshot_fade_v2 | 466,090 | 63 | yes | -3.99% | 0.85% | -2.62% | -0.17% | reportable |
| train | sharp_consensus_clob_mispricing | 86,217 | 33 | yes | -6.28% | 3.66% | 8.63% | 0.67% | reportable |
| train | line_lag_clv_capture | 0 | 0 | no | n/a | n/a | n/a | n/a | no candidate rows; rows 0 < 1,000; markets 0 < 5 |
| val | favorite_longshot_fade_v2 | 118,515 | 16 | yes | -3.15% | 0.18% | -2.48% | -0.09% | reportable |
| val | sharp_consensus_clob_mispricing | 14,329 | 5 | yes | -6.24% | 2.10% | 7.35% | 0.30% | reportable |
| val | line_lag_clv_capture | 0 | 0 | no | n/a | n/a | n/a | n/a | no candidate rows; rows 0 < 1,000; markets 0 < 5 |
| test | favorite_longshot_fade_v2 | 69,104 | 16 | yes | -4.56% | 0.38% | -1.72% | -0.07% | reportable |
| test | sharp_consensus_clob_mispricing | 1,133 | 2 | no | -17.90% | 10.06% | 38.24% | 1.82% | markets 2 < 5 |
| test | line_lag_clv_capture | 0 | 0 | no | n/a | n/a | n/a | n/a | no candidate rows; rows 0 < 1,000; markets 0 < 5 |
| unobserved | favorite_longshot_fade_v2 | 70,160 | 44 | yes | -5.41% | 0.31% | -1.53% | -0.07% | reportable |
| unobserved | sharp_consensus_clob_mispricing | 16,670 | 18 | yes | -7.20% | 0.99% | 4.02% | 0.35% | reportable |
| unobserved | line_lag_clv_capture | 0 | 0 | no | n/a | n/a | n/a | n/a | no candidate rows; rows 0 < 1,000; markets 0 < 5 |

## Predeclared Strategy Rows

| Side | split | strategy | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| taker | test | favorite_longshot_fade_v2 | 69,104 | 16 | -4.56% | -5.27% to -3.83% | 0.38% | 66.41% | 1.78% | -1.72% | -0.07% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 118,515 | 16 | -3.15% | -3.96% to -2.44% | 0.18% | 79.09% | 1.62% | -2.48% | -0.09% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 466,090 | 63 | -3.99% | -4.45% to -3.64% | 0.85% | 69.88% | 1.61% | -2.62% | -0.17% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 70,160 | 44 | -5.41% | -6.18% to -4.87% | 0.31% | 59.03% | 1.76% | -1.53% | -0.07% | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 86,217 | 33 | -6.28% | -7.27% to -5.58% | 3.66% | 37.17% | 1.11% | 8.63% | 0.67% | 0.00% |
| taker | val | sharp_consensus_clob_mispricing | 14,329 | 5 | -6.24% | -8.38% to -5.44% | 2.10% | 39.48% | 1.05% | 7.35% | 0.30% | 0.00% |
| taker | unobserved | sharp_consensus_clob_mispricing | 16,670 | 18 | -7.20% | -8.47% to -5.46% | 0.99% | 46.11% | 1.93% | 4.02% | 0.35% | 0.00% |

## Predeclared Strategy Buckets

| Side | split | strategy | strategy_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| taker | test | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 13,045 | 5 | -2.86% | -3.54% to -2.59% | 0.05% | 80.80% | 1.39% | n/a | n/a | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 02 3-5c | 3,876 | 6 | -5.74% | -6.21% to -4.77% | 0.00% | 80.27% | 3.79% | n/a | n/a | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | baseball_mlb | h2h_or_binary | 01 1-3c | 3,733 | 25 | -2.08% | -2.61% to -1.58% | 24.38% | 89.49% | 1.14% | -37.07% | -3.11% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 33,726 | 8 | -2.31% | -2.78% to -1.96% | 0.01% | 90.92% | 1.58% | -1.83% | 0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 79,355 | 8 | -2.94% | -3.21% to -2.61% | 0.00% | 79.77% | 1.39% | -1.87% | 0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 01 1-3c | 55,457 | 6 | -3.51% | -3.78% to -3.29% | 0.00% | 69.95% | 1.22% | -1.78% | 0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | baseball_mlb | h2h_or_binary | 01 1-3c | 23,114 | 23 | -3.34% | -3.89% to -2.95% | 3.15% | 69.20% | 1.04% | -4.97% | -0.46% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 02 3-5c | 8,958 | 7 | -3.87% | -4.31% to -3.08% | 0.00% | 89.56% | 3.15% | n/a | n/a | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | baseball_mlb | h2h_or_binary | 01 1-3c | 2,818 | 25 | -2.75% | -4.33% to -1.00% | 30.84% | 80.06% | 1.14% | -28.83% | -3.72% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 00 <=1c | 11,919 | 19 | -4.30% | -4.40% to -3.97% | 1.12% | 56.52% | 1.00% | -1.00% | -0.04% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 01 1-3c | 98,497 | 26 | -4.33% | -4.45% to -4.23% | 0.89% | 59.64% | 1.15% | -1.23% | -0.06% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 02 3-5c | 15,272 | 5 | -4.21% | -4.62% to -4.16% | 0.00% | 88.50% | 3.20% | -1.17% | 0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | soccer | h2h_or_binary | 01 1-3c | 40,563 | 6 | -4.40% | -4.88% to -4.16% | 0.00% | 60.00% | 1.21% | -1.90% | -0.01% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 01 1-3c | 30,537 | 22 | -4.88% | -5.49% to -4.38% | 0.29% | 58.19% | 1.42% | -1.05% | -0.00% | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 01 +2c-+4c | baseball_mlb | h2h_or_binary | books=9 | 32,101 | 23 | -5.28% | -5.74% to -4.94% | 0.86% | 48.33% | 1.11% | 2.93% | 0.09% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 02 3-5c | 9,641 | 12 | -5.67% | -6.49% to -4.89% | 0.00% | 79.82% | 3.68% | -3.65% | -0.02% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | baseball_mlb | h2h_or_binary | 02 3-5c | 3,049 | 12 | -6.71% | -6.94% to -5.07% | 0.39% | 64.71% | 3.15% | -6.91% | -0.25% | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 02 +4c-+7c | baseball_mlb | h2h_or_binary | books=9 | 17,201 | 23 | -6.08% | -6.98% to -5.35% | 1.48% | 43.25% | 1.25% | 5.93% | 0.17% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | nrfi_yrfi | 01 1-3c | 2,999 | 5 | -7.26% | -7.83% to -7.17% | 0.23% | 56.34% | 2.52% | n/a | n/a | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 02 3-5c | 14,046 | 8 | -6.99% | -8.43% to -5.89% | 0.00% | 71.38% | 3.93% | -2.71% | 0.01% | 0.00% |
| taker | unobserved | sharp_consensus_clob_mispricing | 01 +2c-+4c | baseball_mlb | h2h_or_binary | books=9 | 10,451 | 11 | -7.18% | -8.69% to -5.34% | 0.34% | 48.68% | 2.11% | 2.70% | 0.02% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 02 3-5c | 26,340 | 22 | -9.19% | -9.78% to -8.46% | 0.13% | 57.17% | 3.95% | -1.88% | 0.00% | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 01 +2c-+4c | soccer | h2h_or_binary | books=9 | 16,139 | 5 | -8.57% | -10.07% to -5.93% | 0.00% | 24.81% | 1.08% | 2.70% | 0.01% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | soccer | h2h_or_binary | 02 3-5c | 3,461 | 6 | -8.20% | -10.41% to -7.84% | 0.00% | 59.44% | 3.59% | -2.60% | 0.02% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 02 3-5c | 9,028 | 16 | -9.01% | -10.49% to -8.54% | 0.00% | 57.37% | 3.71% | -2.77% | 0.02% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | nrfi_yrfi | 02 3-5c | 3,573 | 13 | -9.63% | -10.57% to -8.94% | 0.06% | 54.64% | 3.82% | n/a | n/a | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 03 >+7c | baseball_mlb | h2h_or_binary | books=9 | 17,846 | 25 | -8.08% | -11.45% to -6.05% | 13.89% | 24.04% | 1.04% | 26.93% | 2.27% | 0.00% |
| taker | unobserved | sharp_consensus_clob_mispricing | 02 +4c-+7c | baseball_mlb | h2h_or_binary | books=9 | 2,967 | 7 | -9.09% | -18.00% to -8.37% | 0.27% | 41.75% | 2.30% | 5.34% | 0.32% | 0.00% |

## Player / Injury News Adjustment

- Status: missing_public_timestamped_feed
- Contract: public timestamped reports only; no raw player names in model features; use impact aggregates such as starter count out, usage/minutes lost, position impact, report age, and market reaction.
- Current use: filter favorite-longshot entries, trigger line-lag reviews, and adjust sharp-consensus fair value once a validated feed is present.

## Play-By-Play Event State

- Status: available
- Contract: causal event logs only; features include score differential, clock, possession, recent scoring/penalty/injury events, and win-probability/event-shock deltas.
- Current use: required before the post-event shock strategy can graduate beyond generic price-shock research.

## Sentiment / Public Hype

- Status: missing_feature_file
- Contract: public timestamped sentiment aggregates only; raw text/headlines stay outside model features. Use mention volume, source quality, sentiment surprise, and public hype score.
- Current use: overlay for favorite-longshot fade and news/line-lag filters, not a standalone prediction strategy.

## Verdict

No predeclared test bucket cleared a positive cluster-bootstrap CI lower bound. Current Telonex data does not support live capital for maker/taker price-bucket strategies.
