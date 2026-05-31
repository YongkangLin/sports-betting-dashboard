# Telonex Strategy Bucket Audit

- Generated: 2026-05-31T04:43:41.231087+00:00
- Labels: 2,888,585
- Markets/tokens: 216 / 429
- Sports: {'baseball_mlb': 1731351, 'soccer': 1108317, 'basketball_wnba': 43570, 'icehockey_nhl': 5347}
- Label SHA256: `32537f0d3b561eb1f7a39bcb5ed6ad4834d6f854a4443683da29c657d09f223b`
- Odds API feature coverage: 48.96%
- Odds API split coverage: `{'test': {'rows': 226224, 'matched_rows': 73604, 'row_coverage': 0.3253589362755499, 'markets': 18, 'matched_markets': 5}, 'train': {'rows': 1776863, 'matched_rows': 936300, 'row_coverage': 0.5269398935089536, 'markets': 75, 'matched_markets': 44}, 'unobserved': {'rows': 539748, 'matched_rows': 229330, 'row_coverage': 0.4248834641351149, 'markets': 107, 'matched_markets': 24}, 'val': {'rows': 345750, 'matched_rows': 174926, 'row_coverage': 0.5059320318148951, 'markets': 16, 'matched_markets': 6}}`
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
| maker | test | 06 85-95c favorite | 2,038 | 6 | -1.05% | -1.73% to -0.56% | 9.81% | 87.25% | 2.80% | -43.44% | -1.66% | 0.00% |
| maker | test | 05 70-85c high_mid | 33,613 | 14 | -1.44% | -1.74% to -1.21% | 2.79% | 78.74% | 5.02% | -11.95% | -1.70% | 0.00% |
| maker | test | 04 30-70c mid | 148,133 | 17 | -3.05% | -3.28% to -2.86% | 2.45% | 50.09% | 13.20% | -0.88% | 0.00% | 0.00% |
| taker | test | 06 85-95c favorite | 2,038 | 6 | -4.11% | -5.65% to -1.91% | 4.86% | 87.25% | 2.80% | -43.44% | -1.66% | 0.00% |
| maker | test | 03 15-30c low_mid | 34,252 | 14 | -5.57% | -6.77% to -4.83% | 3.29% | 21.44% | 5.22% | 8.39% | 1.53% | 0.00% |
| maker | test | 02 5-15c longshot | 2,032 | 6 | -3.54% | -8.06% to 2.68% | 22.98% | 13.03% | 2.90% | 42.42% | 1.66% | 0.00% |
| taker | test | 05 70-85c high_mid | 33,613 | 14 | -7.43% | -11.98% to -5.00% | 0.34% | 78.74% | 5.02% | -11.95% | -1.70% | 0.00% |
| taker | test | 02 5-15c longshot | 2,032 | 6 | -23.31% | -29.19% to -8.12% | 3.69% | 13.03% | 2.90% | 42.42% | 1.66% | 0.00% |
| taker | test | 03 15-30c low_mid | 34,252 | 14 | -26.42% | -33.53% to -19.60% | 0.18% | 21.44% | 5.22% | 8.39% | 1.53% | 0.00% |
| taker | test | 04 30-70c mid | 148,133 | 17 | -25.62% | -41.96% to -11.48% | 0.08% | 50.09% | 13.20% | -0.88% | 0.00% | 0.00% |
| maker | train | 07 >=95c near_certain | 3,682 | 25 | -0.25% | -0.57% to -0.04% | 34.00% | 97.92% | 0.75% | -44.33% | -1.23% | 0.00% |
| maker | val | 06 85-95c favorite | 55,201 | 10 | -0.54% | -0.70% to -0.45% | 3.27% | 91.84% | 1.89% | -2.25% | -0.11% | 0.00% |
| maker | train | 06 85-95c favorite | 62,661 | 35 | -0.85% | -1.05% to -0.76% | 4.94% | 87.94% | 2.40% | -4.56% | -0.30% | 0.00% |
| taker | train | 07 >=95c near_certain | 3,682 | 25 | -0.99% | -1.34% to -0.73% | 14.07% | 97.92% | 0.75% | -44.33% | -1.23% | 0.00% |
| maker | train | 05 70-85c high_mid | 212,110 | 61 | -1.52% | -1.73% to -1.38% | 1.83% | 77.49% | 5.01% | -3.65% | -0.19% | 0.00% |
| maker | val | 05 70-85c high_mid | 20,087 | 14 | -1.43% | -1.99% to -1.08% | 1.20% | 77.59% | 2.49% | -26.69% | -6.14% | 0.00% |
| maker | train | 04 30-70c mid | 1,218,891 | 70 | -3.04% | -3.11% to -2.98% | 3.88% | 49.99% | 9.85% | -0.84% | -0.00% | 0.00% |
| maker | val | 04 30-70c mid | 191,531 | 13 | -2.94% | -3.19% to -2.73% | 2.00% | 50.01% | 6.56% | -0.73% | 0.00% | 0.00% |
| maker | unobserved | 04 30-70c mid | 538,199 | 107 | -3.21% | -3.29% to -3.14% | 3.81% | 50.00% | 11.09% | -0.73% | 0.00% | 0.00% |
| taker | val | 06 85-95c favorite | 55,201 | 10 | -2.51% | -3.66% to -1.86% | 0.12% | 91.84% | 1.89% | -2.25% | -0.11% | 0.00% |

## Sport x Price Buckets

| Side | split | sport_family | price_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | soccer | 05 70-85c high_mid | 31,824 | 10 | -1.44% | -1.72% to -1.20% | 2.52% | 79.12% | 5.05% | nan% | nan% | 0.00% |
| maker | test | baseball_mlb | 04 30-70c mid | 80,164 | 5 | -3.03% | -3.15% to -2.90% | 2.54% | 50.01% | 4.16% | -0.84% | -0.00% | 0.00% |
| maker | test | soccer | 04 30-70c mid | 38,941 | 11 | -3.24% | -3.72% to -2.45% | 1.80% | 50.28% | 12.89% | nan% | nan% | 0.00% |
| maker | test | soccer | 03 15-30c low_mid | 32,323 | 10 | -5.61% | -7.03% to -4.83% | 3.08% | 21.04% | 5.28% | nan% | nan% | 0.00% |
| taker | test | soccer | 05 70-85c high_mid | 31,824 | 10 | -7.44% | -11.74% to -4.90% | 0.03% | 79.12% | 5.05% | nan% | nan% | 0.00% |
| taker | test | baseball_mlb | 04 30-70c mid | 80,164 | 5 | -10.78% | -17.68% to -6.66% | 0.12% | 50.01% | 4.16% | -0.84% | -0.00% | 0.00% |
| taker | test | soccer | 03 15-30c low_mid | 32,323 | 10 | -27.01% | -35.50% to -18.83% | 0.08% | 21.04% | 5.28% | nan% | nan% | 0.00% |
| taker | test | soccer | 04 30-70c mid | 38,941 | 11 | -25.23% | -53.03% to -17.19% | 0.03% | 50.28% | 12.89% | nan% | nan% | 0.00% |
| maker | train | baseball_mlb | 07 >=95c near_certain | 3,658 | 24 | -0.25% | -0.58% to -0.04% | 34.14% | 97.93% | 0.74% | -44.33% | -1.23% | 0.00% |
| maker | val | soccer | 06 85-95c favorite | 55,051 | 8 | -0.54% | -0.72% to -0.46% | 3.12% | 91.84% | 1.89% | -1.99% | 0.00% | 0.00% |
| maker | train | soccer | 06 85-95c favorite | 58,172 | 8 | -0.85% | -1.03% to -0.80% | 2.28% | 87.77% | 2.49% | -0.92% | -0.00% | 0.00% |
| maker | train | baseball_mlb | 06 85-95c favorite | 4,455 | 26 | -0.80% | -1.32% to -0.31% | 39.35% | 90.12% | 1.12% | -37.99% | -2.78% | 0.00% |
| taker | train | baseball_mlb | 07 >=95c near_certain | 3,658 | 24 | -0.98% | -1.38% to -0.73% | 14.16% | 97.93% | 0.74% | -44.33% | -1.23% | 0.00% |
| maker | train | soccer | 05 70-85c high_mid | 183,053 | 24 | -1.46% | -1.69% to -1.32% | 1.06% | 78.00% | 3.78% | -3.01% | -0.00% | 0.00% |
| maker | val | soccer | 05 70-85c high_mid | 19,776 | 9 | -1.39% | -1.76% to -1.06% | 0.79% | 77.62% | 2.31% | -5.98% | nan% | 0.00% |
| taker | train | baseball_mlb | 06 85-95c favorite | 4,455 | 26 | -1.99% | -2.52% to -1.53% | 24.96% | 90.12% | 1.12% | -37.99% | -2.78% | 0.00% |
| maker | train | baseball_mlb | 05 70-85c high_mid | 23,581 | 36 | -1.99% | -2.77% to -1.34% | 8.00% | 73.68% | 14.34% | -9.24% | -1.30% | 0.00% |
| maker | train | soccer | 04 30-70c mid | 285,136 | 27 | -2.90% | -3.06% to -2.76% | 1.26% | 50.05% | 5.50% | -1.12% | 0.00% | 0.00% |
| maker | train | baseball_mlb | 04 30-70c mid | 931,763 | 42 | -3.09% | -3.15% to -3.03% | 4.68% | 49.97% | 11.05% | -0.70% | -0.00% | 0.00% |
| maker | val | baseball_mlb | 04 30-70c mid | 116,873 | 5 | -3.12% | -3.20% to -3.08% | 2.77% | 50.01% | 7.58% | -0.77% | 0.00% | 0.00% |

## Horizon x Spread Buckets

| Side | split | horizon_sec | spread_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 300 | 02 3-5c | 5,186 | 18 | -2.43% | -2.76% to -1.94% | 3.34% | 52.80% | 3.95% | -2.22% | 0.00% | 0.00% |
| maker | test | 900 | 02 3-5c | 5,015 | 18 | -2.42% | -2.77% to -1.98% | 5.46% | 52.71% | 3.94% | -2.17% | 0.02% | 0.00% |
| maker | test | 30 | 02 3-5c | 5,163 | 18 | -2.42% | -2.78% to -1.85% | 3.49% | 52.23% | 3.97% | -2.20% | 0.01% | 0.00% |
| maker | test | 120 | 01 1-3c | 21,663 | 17 | -2.49% | -2.81% to -2.05% | 1.01% | 50.40% | 1.42% | -0.77% | -0.01% | 0.00% |
| maker | test | 30 | 01 1-3c | 22,344 | 17 | -2.48% | -2.82% to -2.05% | 0.59% | 50.36% | 1.43% | -0.78% | -0.01% | 0.00% |
| maker | test | 60 | 01 1-3c | 21,901 | 17 | -2.49% | -2.82% to -2.12% | 0.76% | 50.37% | 1.42% | -0.78% | -0.01% | 0.00% |
| maker | test | 60 | 02 3-5c | 5,171 | 18 | -2.49% | -2.83% to -1.96% | 3.19% | 52.14% | 3.97% | -2.21% | 0.01% | 0.00% |
| maker | test | 300 | 01 1-3c | 21,996 | 17 | -2.49% | -2.84% to -2.05% | 1.36% | 50.29% | 1.43% | -0.78% | -0.01% | 0.00% |
| maker | test | 900 | 01 1-3c | 21,673 | 17 | -2.52% | -2.87% to -2.09% | 2.05% | 50.28% | 1.43% | -0.78% | -0.02% | 0.00% |
| maker | test | 120 | 02 3-5c | 5,008 | 18 | -2.54% | -2.90% to -1.96% | 3.25% | 52.07% | 3.98% | -2.25% | 0.00% | 0.00% |
| maker | test | 30 | 03 5-10c | 4,640 | 16 | -2.44% | -2.97% to -2.18% | 1.72% | 50.74% | 6.70% | -3.39% | -0.04% | 0.00% |
| maker | test | 60 | 03 5-10c | 4,460 | 16 | -2.45% | -2.99% to -2.20% | 2.47% | 50.74% | 6.69% | -3.39% | -0.04% | 0.00% |
| maker | test | 300 | 03 5-10c | 4,433 | 16 | -2.40% | -3.10% to -2.10% | 6.43% | 50.70% | 6.69% | -3.38% | -0.03% | 0.00% |
| maker | test | 120 | 03 5-10c | 4,461 | 16 | -2.49% | -3.10% to -2.21% | 3.56% | 50.72% | 6.70% | -3.39% | -0.04% | 0.00% |
| maker | test | 900 | 03 5-10c | 4,418 | 16 | -2.54% | -3.43% to -2.12% | 10.25% | 50.80% | 6.73% | -3.37% | -0.03% | 0.00% |
| maker | test | 60 | 00 <=1c | 3,085 | 14 | -3.06% | -3.92% to -2.70% | 1.07% | 42.81% | 0.99% | 0.99% | 0.08% | 0.00% |
| maker | test | 120 | 00 <=1c | 3,069 | 14 | -3.13% | -3.96% to -2.79% | 1.40% | 42.79% | 0.99% | 1.00% | 0.08% | 0.00% |
| maker | test | 30 | 00 <=1c | 3,102 | 13 | -3.07% | -4.00% to -2.69% | 0.71% | 42.62% | 0.99% | 1.01% | 0.08% | 0.00% |
| maker | test | 300 | 00 <=1c | 3,103 | 13 | -3.22% | -4.01% to -2.88% | 1.84% | 42.34% | 0.99% | 1.03% | 0.08% | 0.00% |
| maker | test | 900 | 04 >10c | 10,101 | 15 | -2.99% | -4.03% to -1.79% | 12.02% | 49.98% | 34.45% | -12.48% | 0.00% | 0.00% |

## Odds Edge Buckets

| Side | split | odds_edge_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 03 -2c-+2c neutral | 57,887 | 5 | -2.95% | -3.03% to -2.81% | 0.23% | 49.86% | 1.38% | -1.00% | -0.01% | 0.00% |
| maker | test | 04 +2c-+5c edge | 9,636 | 5 | -2.71% | -3.33% to -2.35% | 1.81% | 50.72% | 3.03% | -0.04% | 0.02% | 0.00% |
| taker | test | 03 -2c-+2c neutral | 57,887 | 5 | -5.53% | -6.24% to -4.99% | 0.08% | 50.14% | 1.38% | -0.38% | 0.01% | 0.00% |
| taker | test | 02 -5c--2c against | 9,636 | 5 | -8.77% | -10.42% to -7.22% | 0.01% | 49.28% | 3.03% | -2.99% | -0.02% | 0.00% |
| maker | train | 00 <=-10c against | 14,956 | 28 | -0.90% | -1.61% to -0.31% | 38.71% | 82.06% | 1.06% | -32.72% | -2.64% | 0.00% |
| maker | train | 03 -2c-+2c neutral | 610,783 | 44 | -2.50% | -2.86% to -2.20% | 0.50% | 51.50% | 1.45% | -1.08% | -0.00% | 0.00% |
| maker | unobserved | 01 -10c--5c against | 2,946 | 9 | -2.40% | -2.91% to 1.33% | 2.21% | 58.12% | 2.52% | -8.12% | -0.46% | 0.00% |
| maker | train | 02 -5c--2c against | 60,876 | 34 | -2.22% | -2.95% to -1.83% | 0.86% | 62.39% | 1.57% | -4.42% | -0.12% | 0.00% |
| maker | unobserved | 03 -2c-+2c neutral | 166,416 | 23 | -2.97% | -3.03% to -2.90% | 0.19% | 50.16% | 1.21% | -0.95% | -0.00% | 0.00% |
| maker | val | 03 -2c-+2c neutral | 104,023 | 6 | -1.87% | -3.07% to -0.99% | 0.38% | 60.48% | 1.24% | -1.39% | -0.01% | 0.00% |
| maker | val | 02 -5c--2c against | 5,794 | 5 | -1.97% | -3.12% to -1.86% | 1.57% | 67.28% | 1.23% | -3.72% | -0.04% | 0.00% |
| maker | unobserved | 02 -5c--2c against | 13,810 | 20 | -2.96% | -3.16% to -2.75% | 0.51% | 52.12% | 2.02% | -4.96% | -0.07% | 0.00% |
| maker | unobserved | 04 +2c-+5c edge | 35,777 | 22 | -3.04% | -3.27% to -2.84% | 0.63% | 48.56% | 1.67% | 1.49% | 0.03% | 0.00% |
| maker | train | 04 +2c-+5c edge | 174,717 | 42 | -3.08% | -3.55% to -2.54% | 1.40% | 41.73% | 2.29% | 0.85% | 0.04% | 0.00% |
| maker | train | 01 -10c--5c against | 16,761 | 27 | -2.61% | -3.77% to -1.81% | 3.23% | 55.61% | 1.19% | -8.05% | -0.27% | 0.00% |
| maker | unobserved | 05 +5c-+10c edge | 8,870 | 17 | -3.23% | -3.79% to -2.74% | 2.15% | 47.12% | 3.45% | 3.22% | 0.14% | 0.00% |
| maker | train | 05 +5c-+10c edge | 32,282 | 37 | -3.26% | -3.84% to -2.84% | 3.20% | 42.64% | 4.95% | 2.30% | 0.18% | 0.00% |
| maker | val | 04 +2c-+5c edge | 48,065 | 6 | -4.01% | -4.63% to -2.91% | 0.58% | 25.31% | 1.55% | 1.16% | 0.02% | 0.00% |
| maker | val | 05 +5c-+10c edge | 7,053 | 5 | -3.28% | -5.15% to -2.54% | 3.46% | 47.78% | 1.87% | 7.10% | -0.03% | 0.00% |
| maker | train | 06 >+10c edge | 25,925 | 34 | -3.70% | -5.28% to -2.44% | 18.19% | 28.39% | 9.18% | 16.38% | 2.09% | 0.00% |

## Sport x Odds Edge Buckets

| Side | split | sport_family | odds_edge_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | train | baseball_mlb | 00 <=-10c against | 14,952 | 27 | -0.89% | -1.78% to -0.33% | 38.72% | 82.06% | 1.06% | -32.73% | -2.64% | 0.00% |
| maker | train | soccer | 03 -2c-+2c neutral | 319,016 | 14 | -2.14% | -2.65% to -1.78% | 0.42% | 52.63% | 1.68% | -1.34% | -0.00% | 0.00% |
| maker | unobserved | baseball_mlb | 01 -10c--5c against | 2,946 | 9 | -2.40% | -2.77% to 3.26% | 2.21% | 58.12% | 2.52% | -8.12% | -0.46% | 0.00% |
| maker | train | soccer | 02 -5c--2c against | 31,821 | 9 | -1.79% | -2.78% to -1.44% | 0.12% | 70.99% | 1.86% | -4.48% | -0.03% | 0.00% |
| maker | train | baseball_mlb | 03 -2c-+2c neutral | 283,876 | 29 | -2.91% | -2.97% to -2.84% | 0.59% | 50.37% | 1.19% | -0.80% | -0.01% | 0.00% |
| maker | unobserved | baseball_mlb | 03 -2c-+2c neutral | 166,416 | 23 | -2.97% | -3.02% to -2.89% | 0.19% | 50.16% | 1.21% | -0.95% | -0.00% | 0.00% |
| maker | train | baseball_mlb | 02 -5c--2c against | 29,055 | 25 | -2.86% | -3.08% to -2.61% | 1.67% | 52.98% | 1.25% | -4.36% | -0.17% | 0.00% |
| maker | unobserved | baseball_mlb | 02 -5c--2c against | 13,810 | 20 | -2.96% | -3.19% to -2.77% | 0.51% | 52.12% | 2.02% | -4.96% | -0.07% | 0.00% |
| maker | unobserved | baseball_mlb | 04 +2c-+5c edge | 35,777 | 22 | -3.04% | -3.27% to -2.82% | 0.63% | 48.56% | 1.67% | 1.49% | 0.03% | 0.00% |
| maker | train | baseball_mlb | 04 +2c-+5c edge | 57,551 | 27 | -3.17% | -3.36% to -3.02% | 1.66% | 47.02% | 2.05% | 1.27% | 0.10% | 0.00% |
| maker | train | baseball_mlb | 01 -10c--5c against | 16,691 | 26 | -2.59% | -3.56% to -1.38% | 3.24% | 55.52% | 1.17% | -8.03% | -0.27% | 0.00% |
| maker | train | soccer | 06 >+10c edge | 10,174 | 6 | -3.17% | -3.58% to -0.74% | 5.32% | 42.47% | 21.30% | -5.25% | 0.01% | 0.00% |
| taker | train | baseball_mlb | 00 <=-10c against | 15,751 | 28 | -2.56% | -3.66% to -1.84% | 24.89% | 80.70% | 1.35% | -31.70% | -2.65% | 0.00% |
| maker | unobserved | baseball_mlb | 05 +5c-+10c edge | 8,870 | 17 | -3.23% | -3.73% to -2.77% | 2.15% | 47.12% | 3.45% | 3.22% | 0.14% | 0.00% |
| maker | train | baseball_mlb | 05 +5c-+10c edge | 23,966 | 28 | -3.12% | -3.83% to -2.28% | 3.54% | 45.51% | 2.25% | 5.22% | 0.20% | 0.00% |
| maker | train | soccer | 04 +2c-+5c edge | 115,408 | 14 | -3.06% | -3.91% to -2.30% | 1.21% | 38.73% | 2.36% | 0.68% | 0.01% | 0.00% |
| maker | train | soccer | 05 +5c-+10c edge | 8,259 | 8 | -3.95% | -4.71% to -3.58% | 2.23% | 34.06% | 12.78% | -6.16% | 0.02% | 0.00% |
| taker | train | baseball_mlb | 03 -2c-+2c neutral | 283,814 | 29 | -5.25% | -5.50% to -5.08% | 0.32% | 49.63% | 1.19% | -0.39% | 0.01% | 0.00% |
| taker | unobserved | baseball_mlb | 03 -2c-+2c neutral | 166,416 | 23 | -5.31% | -5.71% to -5.03% | 0.08% | 49.84% | 1.21% | -0.26% | 0.00% | 0.00% |
| maker | unobserved | baseball_mlb | 06 >+10c edge | 1,090 | 10 | -2.06% | -6.11% to 8.07% | 18.35% | 33.87% | 5.09% | 14.02% | 2.92% | 0.00% |

## Predeclared Strategy Rows

| Side | split | strategy | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| taker | test | favorite_longshot_fade_v2 | 69,104 | 16 | -4.56% | -5.21% to -3.85% | 0.38% | 66.41% | 1.78% | -1.84% | -0.07% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 118,515 | 16 | -3.15% | -3.99% to -2.44% | 0.18% | 79.09% | 1.62% | -2.54% | -0.09% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 466,090 | 63 | -3.99% | -4.42% to -3.64% | 0.85% | 69.88% | 1.61% | -2.59% | -0.16% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 70,160 | 44 | -5.41% | -6.24% to -4.87% | 0.31% | 59.03% | 1.76% | -1.53% | -0.07% | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 77,254 | 33 | -6.52% | -7.62% to -5.66% | 4.07% | 35.61% | 1.13% | 9.34% | 0.76% | 0.00% |
| taker | unobserved | sharp_consensus_clob_mispricing | 16,670 | 18 | -7.20% | -8.59% to -5.36% | 0.99% | 46.11% | 1.93% | 4.02% | 0.35% | 0.00% |
| taker | val | sharp_consensus_clob_mispricing | 13,486 | 5 | -6.38% | -13.87% to -5.46% | 2.17% | 38.82% | 1.06% | 7.80% | 0.32% | 0.00% |

## Predeclared Strategy Buckets

| Side | split | strategy | strategy_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| taker | test | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 13,045 | 5 | -2.86% | -3.54% to -2.59% | 0.05% | 80.80% | 1.39% | nan% | nan% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 02 3-5c | 3,876 | 6 | -5.74% | -6.21% to -4.77% | 0.00% | 80.27% | 3.79% | nan% | nan% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | baseball_mlb | h2h_or_binary | 01 1-3c | 3,733 | 25 | -2.08% | -2.64% to -1.58% | 24.38% | 89.49% | 1.14% | -37.41% | -3.11% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 33,726 | 8 | -2.31% | -2.78% to -1.97% | 0.01% | 90.92% | 1.58% | -1.83% | 0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 79,355 | 8 | -2.94% | -3.20% to -2.60% | 0.00% | 79.77% | 1.39% | -1.88% | 0.01% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 01 1-3c | 55,457 | 6 | -3.51% | -3.77% to -3.31% | 0.00% | 69.95% | 1.22% | -1.78% | 0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | baseball_mlb | h2h_or_binary | 01 1-3c | 23,114 | 23 | -3.34% | -3.92% to -2.98% | 3.15% | 69.20% | 1.04% | -4.90% | -0.45% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 02 3-5c | 8,958 | 7 | -3.87% | -4.27% to -3.07% | 0.00% | 89.56% | 3.15% | nan% | nan% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | baseball_mlb | h2h_or_binary | 01 1-3c | 2,818 | 25 | -2.75% | -4.38% to -0.92% | 30.84% | 80.06% | 1.14% | -28.81% | -3.72% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 00 <=1c | 11,919 | 19 | -4.30% | -4.40% to -3.92% | 1.12% | 56.52% | 1.00% | -0.87% | -0.03% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 01 1-3c | 98,497 | 26 | -4.33% | -4.45% to -4.22% | 0.89% | 59.64% | 1.15% | -1.26% | -0.06% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 02 3-5c | 15,272 | 5 | -4.21% | -4.62% to -4.16% | 0.00% | 88.50% | 3.20% | -1.16% | 0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | soccer | h2h_or_binary | 01 1-3c | 40,563 | 6 | -4.40% | -4.85% to -4.16% | 0.00% | 60.00% | 1.21% | -1.90% | -0.01% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 01 1-3c | 30,537 | 22 | -4.88% | -5.46% to -4.38% | 0.29% | 58.19% | 1.42% | -1.05% | -0.00% | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 01 +2c-+4c | baseball_mlb | h2h_or_binary | books=9 | 23,957 | 22 | -5.38% | -6.31% to -4.98% | 1.10% | 47.77% | 1.15% | 3.01% | 0.13% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 02 3-5c | 9,641 | 12 | -5.67% | -6.49% to -4.89% | 0.00% | 79.82% | 3.68% | -3.67% | -0.02% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | baseball_mlb | h2h_or_binary | 02 3-5c | 3,049 | 12 | -6.71% | -6.91% to -4.83% | 0.39% | 64.71% | 3.15% | -6.72% | -0.25% | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 02 +4c-+7c | baseball_mlb | h2h_or_binary | books=9 | 14,198 | 22 | -6.41% | -7.25% to -5.45% | 1.70% | 42.08% | 1.30% | 6.04% | 0.17% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | nrfi_yrfi | 01 1-3c | 2,999 | 5 | -7.26% | -7.78% to -7.17% | 0.23% | 56.34% | 2.52% | nan% | nan% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 02 3-5c | 14,046 | 8 | -6.99% | -8.42% to -5.85% | 0.00% | 71.38% | 3.93% | -2.72% | 0.01% | 0.00% |
| taker | unobserved | sharp_consensus_clob_mispricing | 01 +2c-+4c | baseball_mlb | h2h_or_binary | books=9 | 10,451 | 11 | -7.18% | -8.67% to -5.40% | 0.34% | 48.68% | 2.11% | 2.70% | 0.02% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 02 3-5c | 26,340 | 22 | -9.19% | -9.71% to -8.54% | 0.13% | 57.17% | 3.95% | -1.86% | 0.01% | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 01 +2c-+4c | soccer | h2h_or_binary | books=9 | 16,139 | 5 | -8.57% | -10.07% to -5.93% | 0.00% | 24.81% | 1.08% | 2.70% | 0.01% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | soccer | h2h_or_binary | 02 3-5c | 3,461 | 6 | -8.20% | -10.46% to -7.85% | 0.00% | 59.44% | 3.59% | -2.60% | 0.02% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | nrfi_yrfi | 02 3-5c | 3,573 | 13 | -9.63% | -10.60% to -8.94% | 0.06% | 54.64% | 3.82% | nan% | nan% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 02 3-5c | 9,028 | 16 | -9.01% | -10.84% to -8.55% | 0.00% | 57.37% | 3.71% | -2.77% | 0.02% | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 03 >+7c | baseball_mlb | h2h_or_binary | books=9 | 19,392 | 25 | -7.50% | -11.37% to -5.80% | 12.81% | 26.50% | 1.04% | 25.53% | 2.09% | 0.00% |
| taker | unobserved | sharp_consensus_clob_mispricing | 02 +4c-+7c | baseball_mlb | h2h_or_binary | books=9 | 2,967 | 7 | -9.09% | -18.00% to -8.34% | 0.27% | 41.75% | 2.30% | 5.34% | 0.32% | 0.00% |

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
