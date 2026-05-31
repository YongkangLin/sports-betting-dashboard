# Telonex Strategy Bucket Audit

- Generated: 2026-05-31T15:30:05.577144+00:00
- Labels: 5,768,529
- Markets/tokens: 725 / 1436
- Sports: {'soccer': 2625089, 'baseball_mlb': 1755107, 'basketball_nba': 908403, 'americanfootball_nfl': 384029, 'basketball_wnba': 56008, 'tennis': 26200, 'icehockey_nhl': 13693}
- Label SHA256: `8cdfb7cda52ff8ab59d31872381cd6a64e65df78ed427febd3caff5f3a59ee39`
- Odds API feature coverage: 69.31%
- Odds API split coverage: `{'test': {'rows': 1265120, 'matched_rows': 731772, 'row_coverage': 0.578421019349943, 'markets': 62, 'matched_markets': 34}, 'train': {'rows': 2195358, 'matched_rows': 1613531, 'row_coverage': 0.7349739769094608, 'markets': 287, 'matched_markets': 272}, 'unobserved': {'rows': 1510528, 'matched_rows': 1139906, 'row_coverage': 0.7546407613761545, 'markets': 314, 'matched_markets': 223}, 'val': {'rows': 797523, 'matched_rows': 513246, 'row_coverage': 0.6435500919722691, 'markets': 62, 'matched_markets': 47}}`
- Player/news feature coverage: 0.00% / status `missing_public_timestamped_feed`
- Play-by-play feature coverage: 26.17% / status `available`
- Sentiment feature coverage: 0.00% / status `missing_feature_file`
- Minimum bucket rows/markets: 1000 / 5
- Positive test buckets total/taker/maker: 0 / 0 / 0
- Executable taker gate: False
- Maker research lead gate: False

This is a fixed-bucket audit, not a model-selection sweep. The buckets are meant to falsify broad strategy hypotheses before any threshold tuning.

## Price Buckets

| Side | split | price_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 07 >=95c near_certain | 5,020 | 11 | -0.19% | -0.27% to 0.20% | 14.64% | 96.42% | 1.99% | -47.95% | -1.10% | 0.00% |
| maker | test | 06 85-95c favorite | 137,875 | 30 | -0.70% | -0.81% to -0.58% | 2.37% | 89.40% | 1.70% | -1.89% | -0.06% | 0.00% |
| maker | test | 05 70-85c high_mid | 214,741 | 47 | -1.45% | -1.63% to -1.32% | 1.45% | 77.94% | 3.49% | -3.22% | -0.03% | 0.00% |
| taker | test | 07 >=95c near_certain | 5,020 | 11 | -2.17% | -2.64% to -0.71% | 3.33% | 96.42% | 1.99% | -47.95% | -1.10% | 0.00% |
| taker | test | 06 85-95c favorite | 137,875 | 30 | -2.52% | -2.98% to -2.02% | 0.25% | 89.40% | 1.70% | -1.89% | -0.06% | 0.00% |
| maker | test | 04 30-70c mid | 548,148 | 45 | -2.93% | -3.05% to -2.81% | 2.12% | 50.04% | 8.28% | -1.01% | 0.00% | 0.00% |
| maker | test | 03 15-30c low_mid | 215,716 | 48 | -4.99% | -5.27% to -4.74% | 1.98% | 22.11% | 3.55% | 0.32% | 0.03% | 0.00% |
| maker | test | 02 5-15c longshot | 138,301 | 31 | -5.33% | -5.47% to -5.16% | 1.55% | 10.61% | 1.70% | 0.59% | 0.07% | 0.00% |
| taker | test | 05 70-85c high_mid | 214,741 | 47 | -5.69% | -7.63% to -4.46% | 0.16% | 77.94% | 3.49% | -3.22% | -0.03% | 0.00% |
| maker | test | 01 3-5c thin_tail | 4,573 | 12 | -6.80% | -16.97% to -5.76% | 8.24% | 3.91% | 2.17% | 41.44% | 1.42% | 0.00% |
| taker | test | 02 5-15c longshot | 138,301 | 31 | -19.72% | -22.64% to -17.37% | 0.22% | 10.61% | 1.70% | 0.59% | 0.07% | 0.00% |
| taker | test | 03 15-30c low_mid | 215,716 | 48 | -19.33% | -24.71% to -15.58% | 0.08% | 22.11% | 3.55% | 0.32% | 0.03% | 0.00% |
| taker | test | 04 30-70c mid | 548,148 | 45 | -17.76% | -25.60% to -12.05% | 0.21% | 50.04% | 8.28% | -1.01% | 0.00% | 0.00% |
| taker | test | 01 3-5c thin_tail | 4,573 | 12 | -48.53% | -54.13% to -36.55% | 0.33% | 3.91% | 2.17% | 41.44% | 1.42% | 0.00% |
| maker | train | 07 >=95c near_certain | 3,337 | 29 | -0.34% | -0.75% to -0.10% | 32.30% | 98.18% | 0.70% | -43.85% | -1.90% | 0.00% |
| maker | train | 06 85-95c favorite | 486,847 | 173 | -0.75% | -0.77% to -0.72% | 2.09% | 88.05% | 1.05% | -3.05% | -0.03% | 0.00% |
| maker | val | 07 >=95c near_certain | 2,032 | 15 | -0.25% | -0.80% to -0.02% | 37.45% | 97.48% | 0.81% | -43.32% | -0.96% | 0.00% |
| maker | unobserved | 06 85-95c favorite | 342,769 | 158 | -0.79% | -0.82% to -0.77% | 2.39% | 87.38% | 1.08% | -1.59% | -0.02% | 0.00% |
| maker | val | 06 85-95c favorite | 114,830 | 44 | -0.80% | -0.83% to -0.76% | 2.24% | 87.47% | 1.45% | -2.38% | -0.06% | 0.00% |
| maker | unobserved | 07 >=95c near_certain | 1,545 | 17 | -0.28% | -1.21% to 0.18% | 38.45% | 97.63% | 1.01% | -26.37% | -1.39% | 0.00% |

## Sport x Price Buckets

| Side | split | sport_family | price_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | soccer | 07 >=95c near_certain | 4,279 | 6 | -0.25% | -0.31% to 0.30% | 9.16% | 96.16% | 2.22% | -29.70% | -1.86% | 0.00% |
| maker | test | soccer | 06 85-95c favorite | 136,831 | 24 | -0.70% | -0.81% to -0.58% | 2.08% | 89.40% | 1.70% | -1.43% | -0.02% | 0.00% |
| maker | test | baseball_mlb | 06 85-95c favorite | 1,044 | 6 | -0.41% | -1.21% to 0.70% | 40.33% | 90.24% | 1.12% | -44.10% | -2.87% | 0.00% |
| maker | test | soccer | 05 70-85c high_mid | 212,289 | 36 | -1.45% | -1.62% to -1.33% | 1.27% | 77.99% | 3.47% | -2.93% | 0.01% | 0.00% |
| taker | test | baseball_mlb | 06 85-95c favorite | 1,044 | 6 | -1.61% | -2.38% to -0.43% | 26.92% | 90.24% | 1.12% | -44.10% | -2.87% | 0.00% |
| taker | test | soccer | 06 85-95c favorite | 136,831 | 24 | -2.53% | -2.96% to -2.04% | 0.04% | 89.40% | 1.70% | -1.43% | -0.02% | 0.00% |
| taker | test | soccer | 07 >=95c near_certain | 4,279 | 6 | -2.46% | -3.00% to -1.39% | 0.82% | 96.16% | 2.22% | -29.70% | -1.86% | 0.00% |
| maker | test | soccer | 04 30-70c mid | 255,901 | 31 | -2.78% | -3.02% to -2.66% | 1.24% | 50.08% | 6.33% | -1.22% | 0.00% | 0.00% |
| maker | test | baseball_mlb | 05 70-85c high_mid | 1,740 | 10 | -1.21% | -3.08% to 0.44% | 22.87% | 75.05% | 6.07% | -22.35% | -2.40% | 0.00% |
| maker | test | baseball_mlb | 04 30-70c mid | 263,219 | 13 | -3.08% | -3.14% to -3.02% | 2.87% | 49.99% | 6.83% | -0.75% | 0.00% | 0.00% |
| maker | test | soccer | 03 15-30c low_mid | 213,065 | 36 | -4.97% | -5.30% to -4.72% | 1.85% | 22.06% | 3.52% | 0.02% | -0.01% | 0.00% |
| maker | test | soccer | 02 5-15c longshot | 137,002 | 24 | -5.30% | -5.44% to -5.13% | 1.31% | 10.62% | 1.71% | 0.03% | 0.02% | 0.00% |
| taker | test | soccer | 05 70-85c high_mid | 212,289 | 36 | -5.67% | -7.38% to -4.58% | 0.01% | 77.99% | 3.47% | -2.93% | 0.01% | 0.00% |
| maker | test | baseball_mlb | 03 15-30c low_mid | 1,833 | 11 | -6.95% | -14.02% to -3.85% | 17.29% | 25.12% | 6.49% | 19.28% | 2.37% | 0.00% |
| maker | test | baseball_mlb | 02 5-15c longshot | 1,299 | 7 | -8.76% | -17.05% to -1.94% | 27.02% | 9.92% | 1.10% | 41.04% | 2.79% | 0.00% |
| taker | test | baseball_mlb | 05 70-85c high_mid | 1,740 | 10 | -8.78% | -17.15% to -4.25% | 17.53% | 75.05% | 6.07% | -22.35% | -2.40% | 0.00% |
| taker | test | baseball_mlb | 04 30-70c mid | 263,219 | 13 | -15.48% | -18.20% to -12.36% | 0.39% | 49.99% | 6.83% | -0.75% | 0.00% | 0.00% |
| maker | test | soccer | 01 3-5c thin_tail | 4,299 | 6 | -6.35% | -20.44% to -5.76% | 7.35% | 3.90% | 2.25% | 18.11% | 1.53% | 0.00% |
| taker | test | soccer | 02 5-15c longshot | 137,002 | 24 | -19.73% | -22.90% to -17.59% | 0.09% | 10.62% | 1.71% | 0.03% | 0.02% | 0.00% |
| taker | test | soccer | 03 15-30c low_mid | 213,065 | 36 | -19.27% | -24.81% to -15.43% | 0.03% | 22.06% | 3.52% | 0.02% | -0.01% | 0.00% |

## Horizon x Spread Buckets

| Side | split | horizon_sec | spread_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 30 | 01 1-3c | 161,085 | 59 | -2.15% | -2.36% to -1.94% | 0.53% | 49.40% | 1.38% | -0.70% | -0.00% | 0.00% |
| maker | test | 60 | 01 1-3c | 158,856 | 60 | -2.17% | -2.38% to -1.95% | 0.66% | 49.39% | 1.37% | -0.70% | -0.00% | 0.00% |
| maker | test | 300 | 01 1-3c | 160,281 | 60 | -2.17% | -2.39% to -1.97% | 1.14% | 49.34% | 1.37% | -0.70% | -0.00% | 0.00% |
| maker | test | 120 | 01 1-3c | 157,597 | 59 | -2.17% | -2.40% to -1.95% | 0.86% | 49.38% | 1.37% | -0.70% | -0.00% | 0.00% |
| maker | test | 900 | 01 1-3c | 157,781 | 60 | -2.20% | -2.41% to -1.96% | 1.87% | 49.34% | 1.37% | -0.69% | -0.00% | 0.00% |
| maker | test | 30 | 02 3-5c | 25,847 | 52 | -1.99% | -2.44% to -1.58% | 2.70% | 56.53% | 3.83% | -1.95% | -0.00% | 0.00% |
| maker | test | 300 | 02 3-5c | 25,979 | 52 | -2.03% | -2.46% to -1.61% | 2.86% | 56.68% | 3.82% | -1.96% | -0.00% | 0.00% |
| maker | test | 60 | 02 3-5c | 25,547 | 53 | -2.02% | -2.49% to -1.59% | 2.71% | 56.42% | 3.83% | -1.95% | -0.00% | 0.00% |
| maker | test | 900 | 02 3-5c | 25,307 | 52 | -2.02% | -2.52% to -1.60% | 4.73% | 56.70% | 3.82% | -1.96% | -0.00% | 0.00% |
| maker | test | 120 | 02 3-5c | 24,831 | 52 | -2.02% | -2.53% to -1.67% | 2.88% | 56.59% | 3.83% | -1.95% | -0.00% | 0.00% |
| maker | test | 30 | 03 5-10c | 23,145 | 47 | -2.58% | -2.91% to -2.37% | 1.79% | 51.29% | 7.12% | -3.41% | -0.02% | 0.00% |
| maker | test | 60 | 03 5-10c | 22,918 | 47 | -2.57% | -2.94% to -2.36% | 2.26% | 51.32% | 7.12% | -3.43% | -0.01% | 0.00% |
| maker | test | 120 | 03 5-10c | 22,413 | 47 | -2.59% | -2.95% to -2.34% | 2.83% | 51.31% | 7.13% | -3.44% | -0.01% | 0.00% |
| maker | test | 300 | 03 5-10c | 22,499 | 46 | -2.59% | -2.95% to -2.28% | 4.28% | 51.33% | 7.12% | -3.42% | -0.01% | 0.00% |
| maker | test | 900 | 03 5-10c | 22,123 | 47 | -2.64% | -3.10% to -2.27% | 6.81% | 51.34% | 7.12% | -3.43% | -0.01% | 0.00% |
| maker | test | 120 | 00 <=1c | 22,273 | 48 | -2.12% | -3.14% to -1.47% | 0.93% | 45.49% | 0.99% | -0.07% | 0.03% | 0.00% |
| maker | test | 900 | 04 >10c | 21,809 | 41 | -2.60% | -3.16% to -1.93% | 13.97% | 49.99% | 33.53% | -9.03% | 0.00% | 0.00% |
| maker | test | 30 | 00 <=1c | 22,628 | 48 | -2.11% | -3.18% to -1.42% | 0.39% | 45.26% | 0.99% | -0.04% | 0.03% | 0.00% |
| maker | test | 300 | 00 <=1c | 22,516 | 48 | -2.14% | -3.18% to -1.46% | 1.29% | 45.45% | 0.99% | -0.06% | 0.03% | 0.00% |
| maker | test | 60 | 00 <=1c | 22,521 | 49 | -2.11% | -3.21% to -1.43% | 0.65% | 45.47% | 0.99% | -0.06% | 0.03% | 0.00% |

## Odds Edge Buckets

| Side | split | odds_edge_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 00 <=-10c against | 3,654 | 11 | 0.38% | -0.78% to 1.34% | 41.38% | 79.37% | 1.07% | -36.45% | -2.88% | 0.00% |
| maker | test | 03 -2c-+2c neutral | 481,234 | 34 | -1.96% | -2.34% to -1.67% | 0.57% | 54.38% | 1.53% | -1.25% | -0.00% | 0.00% |
| maker | test | 02 -5c--2c against | 40,257 | 18 | -1.87% | -2.83% to -1.54% | 0.49% | 69.36% | 1.75% | -4.40% | -0.04% | 0.00% |
| maker | test | 01 -10c--5c against | 7,810 | 11 | -2.73% | -3.29% to -1.29% | 3.18% | 55.58% | 1.31% | -9.09% | -0.20% | 0.00% |
| maker | test | 04 +2c-+5c edge | 165,865 | 34 | -3.24% | -3.86% to -2.46% | 1.26% | 33.94% | 2.17% | 0.77% | 0.02% | 0.00% |
| maker | test | 05 +5c-+10c edge | 17,572 | 18 | -3.63% | -4.32% to -3.33% | 3.11% | 39.56% | 7.12% | 0.43% | 0.09% | 0.00% |
| taker | test | 03 -2c-+2c neutral | 481,239 | 34 | -5.52% | -6.16% to -5.04% | 0.08% | 45.61% | 1.53% | -0.28% | 0.00% | 0.00% |
| maker | test | 06 >+10c edge | 15,380 | 17 | -3.94% | -6.55% to -2.38% | 10.29% | 36.11% | 15.22% | 6.26% | 1.39% | 0.00% |
| taker | test | 02 -5c--2c against | 165,845 | 33 | -4.87% | -7.12% to -3.72% | 0.05% | 66.06% | 2.17% | -2.94% | -0.01% | 0.00% |
| taker | test | 04 +2c-+5c edge | 40,272 | 19 | -9.31% | -13.44% to -6.47% | 0.29% | 30.65% | 1.75% | 2.65% | 0.04% | 0.00% |
| taker | test | 05 +5c-+10c edge | 7,815 | 12 | -6.20% | -16.38% to -5.40% | 1.87% | 44.41% | 1.31% | 7.79% | 0.20% | 0.00% |
| taker | test | 06 >+10c edge | 4,144 | 12 | -14.53% | -21.60% to -10.20% | 10.93% | 19.06% | 1.06% | 35.50% | 2.79% | 0.00% |
| taker | test | 01 -10c--5c against | 17,567 | 17 | -13.21% | -22.22% to -6.64% | 1.01% | 60.44% | 7.12% | -7.55% | -0.09% | 0.00% |
| taker | test | 00 <=-10c against | 14,890 | 16 | -23.51% | -29.78% to -5.02% | 6.57% | 62.94% | 15.69% | -20.96% | -1.34% | 0.00% |
| maker | val | 00 <=-10c against | 8,646 | 16 | -0.57% | -1.21% to -0.01% | 30.40% | 85.10% | 1.24% | -29.42% | -2.36% | 0.00% |
| maker | train | 02 -5c--2c against | 78,029 | 134 | -1.44% | -1.79% to -1.09% | 1.19% | 72.41% | 1.04% | -3.82% | -0.11% | 0.00% |
| maker | unobserved | 03 -2c-+2c neutral | 967,860 | 215 | -1.73% | -1.84% to -1.61% | 1.47% | 52.12% | 1.09% | -0.72% | -0.01% | 0.00% |
| maker | train | 03 -2c-+2c neutral | 1,169,640 | 259 | -1.75% | -1.87% to -1.62% | 1.05% | 55.48% | 1.05% | -0.87% | -0.00% | 0.00% |
| maker | train | 00 <=-10c against | 24,305 | 39 | -1.21% | -1.96% to -0.54% | 22.44% | 77.37% | 1.03% | -39.14% | -1.50% | 0.00% |
| maker | train | 01 -10c--5c against | 12,359 | 48 | -1.50% | -2.01% to -0.52% | 3.63% | 71.61% | 1.01% | -7.50% | -0.36% | 0.00% |

## Sport x Odds Edge Buckets

| Side | split | sport_family | odds_edge_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | baseball_mlb | 00 <=-10c against | 3,196 | 8 | 0.06% | -1.42% to 0.67% | 41.11% | 83.69% | 1.08% | -37.59% | -2.61% | 0.00% |
| maker | test | soccer | 03 -2c-+2c neutral | 364,456 | 22 | -1.66% | -1.98% to -1.35% | 0.60% | 55.85% | 1.61% | -1.38% | -0.00% | 0.00% |
| maker | test | soccer | 02 -5c--2c against | 36,375 | 11 | -1.80% | -2.68% to -1.46% | 0.13% | 70.97% | 1.75% | -4.32% | -0.03% | 0.00% |
| maker | test | baseball_mlb | 03 -2c-+2c neutral | 103,775 | 11 | -3.03% | -3.07% to -2.99% | 0.55% | 49.92% | 1.22% | -0.82% | -0.01% | 0.00% |
| maker | test | baseball_mlb | 04 +2c-+5c edge | 13,727 | 11 | -2.90% | -3.20% to -2.71% | 2.79% | 50.59% | 2.43% | 0.63% | 0.07% | 0.00% |
| maker | test | baseball_mlb | 02 -5c--2c against | 3,882 | 7 | -2.73% | -3.28% to -1.83% | 3.86% | 54.27% | 1.72% | -5.15% | -0.12% | 0.00% |
| maker | test | soccer | 04 +2c-+5c edge | 148,011 | 22 | -3.33% | -4.14% to -2.28% | 1.10% | 31.82% | 2.10% | 0.83% | 0.01% | 0.00% |
| maker | test | baseball_mlb | 01 -10c--5c against | 7,531 | 8 | -2.84% | -4.29% to -1.78% | 2.48% | 54.30% | 1.26% | -9.03% | -0.16% | 0.00% |
| maker | test | baseball_mlb | 05 +5c-+10c edge | 9,536 | 10 | -3.43% | -4.54% to -2.93% | 3.96% | 45.34% | 2.40% | 5.89% | 0.08% | 0.00% |
| maker | test | soccer | 05 +5c-+10c edge | 8,036 | 8 | -4.04% | -5.18% to -3.67% | 2.10% | 32.69% | 12.73% | -6.05% | 0.14% | 0.00% |
| taker | test | baseball_mlb | 03 -2c-+2c neutral | 103,780 | 11 | -5.33% | -5.81% to -5.01% | 0.24% | 50.03% | 1.22% | -0.40% | 0.01% | 0.00% |
| maker | test | soccer | 06 >+10c edge | 10,655 | 7 | -3.55% | -6.15% to -1.91% | 5.21% | 42.70% | 20.36% | -3.81% | 0.50% | 0.00% |
| taker | test | soccer | 03 -2c-+2c neutral | 364,456 | 22 | -5.59% | -6.49% to -4.95% | 0.04% | 44.15% | 1.61% | -0.24% | 0.00% | 0.00% |
| taker | test | soccer | 02 -5c--2c against | 148,011 | 22 | -4.54% | -6.69% to -3.26% | 0.00% | 68.18% | 2.10% | -2.93% | -0.01% | 0.00% |
| taker | test | baseball_mlb | 02 -5c--2c against | 13,707 | 10 | -7.83% | -9.85% to -5.62% | 0.57% | 49.40% | 2.43% | -3.06% | -0.07% | 0.00% |
| taker | test | baseball_mlb | 00 <=-10c against | 4,235 | 9 | -4.88% | -10.92% to -1.29% | 19.95% | 77.13% | 3.94% | -32.05% | -2.35% | 0.00% |
| maker | test | baseball_mlb | 06 >+10c edge | 4,725 | 10 | -5.43% | -10.95% to -0.35% | 21.74% | 21.26% | 3.63% | 28.97% | 2.33% | 0.00% |
| taker | test | baseball_mlb | 04 +2c-+5c edge | 3,897 | 8 | -6.90% | -12.21% to -5.10% | 2.54% | 45.71% | 1.72% | 3.43% | 0.14% | 0.00% |
| taker | test | baseball_mlb | 05 +5c-+10c edge | 7,536 | 9 | -5.99% | -13.30% to -5.25% | 1.94% | 45.70% | 1.26% | 7.77% | 0.16% | 0.00% |
| taker | test | baseball_mlb | 01 -10c--5c against | 9,531 | 9 | -6.95% | -14.73% to -4.89% | 1.76% | 54.66% | 2.40% | -8.29% | -0.07% | 0.00% |

## Predeclared Strategy Support

| Split | Strategy | Rows | Markets | Reportable | ROI | Positive | Odds gap | Line-lag gap | Reason |
|---|---|---:|---:|---|---:|---:|---:|---:|---|
| train | favorite_longshot_fade_v2 | 831,555 | 269 | yes | -2.50% | 0.50% | -2.72% | -0.06% | reportable |
| train | sharp_consensus_clob_mispricing | 107,035 | 151 | yes | -7.47% | 2.72% | 11.12% | 0.48% | reportable |
| train | line_lag_clv_capture | 58 | 3 | no | -13.12% | 1.72% | 3.01% | 2.48% | rows 58 < 1,000; markets 3 < 5 |
| val | favorite_longshot_fade_v2 | 237,062 | 56 | yes | -3.02% | 0.77% | -1.77% | -0.12% | reportable |
| val | sharp_consensus_clob_mispricing | 37,582 | 31 | yes | -5.31% | 3.63% | 10.19% | 0.63% | reportable |
| val | line_lag_clv_capture | 0 | 0 | no | n/a | n/a | n/a | n/a | no candidate rows; rows 0 < 1,000; markets 0 < 5 |
| test | favorite_longshot_fade_v2 | 473,440 | 59 | yes | -3.46% | 0.18% | -2.02% | -0.04% | reportable |
| test | sharp_consensus_clob_mispricing | 36,800 | 18 | yes | -7.56% | 1.92% | 7.39% | 0.49% | reportable |
| test | line_lag_clv_capture | 0 | 0 | no | n/a | n/a | n/a | n/a | no candidate rows; rows 0 < 1,000; markets 0 < 5 |
| unobserved | favorite_longshot_fade_v2 | 547,966 | 248 | yes | -2.58% | 0.28% | -1.65% | -0.02% | reportable |
| unobserved | sharp_consensus_clob_mispricing | 35,903 | 85 | yes | -7.36% | 1.38% | 6.28% | 0.43% | reportable |
| unobserved | line_lag_clv_capture | 12 | 1 | no | -8.48% | 0.00% | 1.48% | 7.59% | rows 12 < 1,000; markets 1 < 5 |

## Predeclared Strategy Rows

| Side | split | strategy | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| taker | test | favorite_longshot_fade_v2 | 473,440 | 59 | -3.46% | -3.83% to -3.13% | 0.18% | 75.95% | 1.63% | -2.02% | -0.04% | 0.00% |
| taker | test | sharp_consensus_clob_mispricing | 36,800 | 18 | -7.56% | -9.58% to -6.08% | 1.92% | 30.86% | 1.06% | 7.39% | 0.49% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 831,555 | 269 | -2.50% | -2.68% to -2.35% | 0.50% | 79.99% | 1.13% | -2.72% | -0.06% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 547,966 | 248 | -2.58% | -2.76% to -2.42% | 0.28% | 79.67% | 1.18% | -1.65% | -0.02% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 237,062 | 56 | -3.02% | -3.40% to -2.65% | 0.77% | 75.45% | 1.29% | -1.77% | -0.12% | 0.00% |
| taker | val | sharp_consensus_clob_mispricing | 37,582 | 31 | -5.31% | -7.83% to -4.43% | 3.63% | 49.57% | 1.51% | 10.19% | 0.63% | 0.00% |
| taker | unobserved | sharp_consensus_clob_mispricing | 35,903 | 85 | -7.36% | -8.39% to -6.42% | 1.38% | 37.10% | 1.48% | 6.28% | 0.43% | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 107,035 | 151 | -7.47% | -8.97% to -6.59% | 2.72% | 26.84% | 1.03% | 11.12% | 0.48% | 0.00% |

## Predeclared Strategy Buckets

| Side | split | strategy | strategy_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| taker | test | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 00 <=1c | 14,260 | 5 | -1.45% | -1.46% to -0.97% | 0.01% | 93.51% | 1.00% | -2.11% | -0.08% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 101,709 | 23 | -2.19% | -2.38% to -2.00% | 0.05% | 88.70% | 1.32% | -1.33% | -0.02% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 94,307 | 16 | -2.93% | -3.16% to -2.65% | 0.03% | 79.82% | 1.39% | -1.85% | 0.01% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 01 1-3c | 88,898 | 12 | -3.60% | -3.88% to -3.25% | 0.00% | 69.84% | 1.27% | -2.14% | 0.01% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 02 3-5c | 23,394 | 15 | -4.07% | -4.26% to -3.66% | 0.00% | 88.71% | 3.16% | -1.17% | -0.00% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 00 <=1c | 11,934 | 9 | -4.40% | -4.53% to -4.28% | 0.12% | 56.50% | 1.00% | -0.86% | -0.02% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | soccer | h2h_or_binary | 01 1-3c | 19,778 | 8 | -4.58% | -4.76% to -4.14% | 0.04% | 61.49% | 1.41% | -3.32% | 0.08% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 01 1-3c | 29,891 | 9 | -4.57% | -4.92% to -4.29% | 0.36% | 57.74% | 1.16% | -1.02% | -0.12% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 02 3-5c | 13,166 | 16 | -5.67% | -6.30% to -5.06% | 0.00% | 80.02% | 3.70% | -3.65% | -0.02% | 0.00% |
| taker | test | sharp_consensus_clob_mispricing | 01 +2c-+4c | baseball_mlb | h2h_or_binary | books=9 | 2,619 | 7 | -4.94% | -6.86% to -4.66% | 2.79% | 50.14% | 1.03% | 3.12% | 0.11% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 02 3-5c | 16,006 | 11 | -7.04% | -8.29% to -5.93% | 0.01% | 71.23% | 3.94% | -2.72% | 0.01% | 0.00% |
| taker | test | sharp_consensus_clob_mispricing | 01 +2c-+4c | soccer | h2h_or_binary | books=9 | 15,890 | 6 | -8.62% | -10.05% to -3.06% | 0.06% | 24.60% | 1.08% | 2.68% | 0.01% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 02 3-5c | 9,823 | 8 | -9.16% | -10.07% to -8.50% | 0.04% | 57.26% | 3.94% | -1.07% | 0.03% | 0.00% |
| taker | test | sharp_consensus_clob_mispricing | 02 +4c-+7c | baseball_mlb | h2h_or_binary | books=9 | 1,183 | 8 | -8.46% | -14.15% to -5.71% | 6.85% | 46.98% | 1.69% | 5.18% | 0.48% | 0.00% |
| taker | test | sharp_consensus_clob_mispricing | 03 >+7c | baseball_mlb | h2h_or_binary | books=9 | 9,818 | 9 | -6.92% | -20.66% to -5.55% | 5.42% | 35.28% | 1.00% | 18.82% | 0.99% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | basketball_nba | h2h_or_binary | 01 1-3c | 246,690 | 84 | -1.81% | -1.85% to -1.77% | 0.03% | 88.88% | 1.03% | -2.48% | 0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | americanfootball_nfl | h2h_or_binary | 01 1-3c | 22,445 | 12 | -1.92% | -1.99% to -1.85% | 0.21% | 87.54% | 1.04% | -1.56% | -0.03% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 209,060 | 53 | -1.97% | -2.01% to -1.93% | 0.07% | 86.98% | 1.04% | -2.99% | -0.00% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 311,046 | 99 | -1.99% | -2.02% to -1.95% | 0.04% | 87.31% | 1.08% | -1.50% | -0.01% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 93,764 | 25 | -1.95% | -2.03% to -1.88% | 0.06% | 87.24% | 1.04% | -1.84% | -0.00% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 04 85-95c | basketball_nba | h2h_or_binary | 01 1-3c | 23,660 | 40 | -1.94% | -2.04% to -1.84% | 0.10% | 87.52% | 1.05% | -1.33% | -0.02% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 22,841 | 36 | -2.11% | -2.15% to -2.08% | 0.18% | 84.43% | 1.02% | -1.18% | 0.05% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 9,388 | 9 | -2.24% | -2.33% to -1.75% | 0.29% | 82.55% | 1.03% | -1.43% | 0.15% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | basketball_nba | h2h_or_binary | 00 <=1c | 2,600 | 8 | -2.34% | -2.37% to -2.29% | 0.12% | 81.50% | 1.00% | -4.14% | -0.00% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 04 85-95c | baseball_mlb | h2h_or_binary | 01 1-3c | 1,251 | 12 | -1.41% | -2.39% to -0.70% | 28.06% | 89.68% | 1.13% | -39.52% | -2.84% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 26,398 | 20 | -2.25% | -2.47% to -2.10% | 0.06% | 82.95% | 1.03% | -1.12% | 0.02% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 03 75-85c | basketball_nba | h2h_or_binary | 01 1-3c | 13,930 | 19 | -2.47% | -2.61% to -2.24% | 0.06% | 79.71% | 1.04% | -1.84% | 0.02% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | americanfootball_nfl | h2h_or_binary | 01 1-3c | 25,457 | 22 | -2.64% | -2.76% to -2.53% | 0.44% | 78.22% | 1.07% | -1.69% | -0.03% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | basketball_nba | h2h_or_binary | 01 1-3c | 32,794 | 29 | -2.55% | -2.92% to -2.28% | 0.20% | 81.65% | 1.22% | -2.27% | 0.02% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | baseball_mlb | h2h_or_binary | 01 1-3c | 3,636 | 22 | -2.42% | -3.28% to -1.63% | 23.57% | 89.76% | 1.12% | -36.74% | -3.19% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | americanfootball_nfl | h2h_or_binary | 01 1-3c | 51,812 | 27 | -3.19% | -3.29% to -3.10% | 0.16% | 71.02% | 1.05% | -1.13% | 0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | americanfootball_nfl | h2h_or_binary | 00 <=1c | 4,554 | 12 | -3.33% | -3.38% to -3.28% | 0.13% | 68.50% | 1.00% | -0.87% | 0.02% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | basketball_nba | h2h_or_binary | 00 <=1c | 3,007 | 6 | -3.32% | -3.45% to -3.20% | 0.00% | 68.50% | 1.00% | -1.97% | -0.04% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 02 65-75c | basketball_nba | h2h_or_binary | 00 <=1c | 1,599 | 7 | -3.44% | -3.50% to -3.18% | 0.00% | 68.50% | 1.00% | -7.06% | -0.08% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | basketball_nba | h2h_or_binary | 01 1-3c | 27,785 | 15 | -3.37% | -3.55% to -3.15% | 0.18% | 68.56% | 1.07% | -1.37% | -0.01% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 02 65-75c | basketball_nba | h2h_or_binary | 01 1-3c | 11,117 | 13 | -3.50% | -3.61% to -3.34% | 0.08% | 68.02% | 1.10% | -2.45% | 0.01% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 01 1-3c | 12,940 | 6 | -3.36% | -3.64% to -3.13% | 0.12% | 69.90% | 1.11% | -1.46% | 0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 01 1-3c | 3,660 | 5 | -3.19% | -3.95% to -2.77% | 0.00% | 70.44% | 1.00% | -1.86% | 0.15% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 01 55-65c | soccer | h2h_or_binary | 01 1-3c | 20,606 | 7 | -3.99% | -4.09% to -3.85% | 0.01% | 61.47% | 1.06% | -1.76% | 0.01% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 02 65-75c | baseball_mlb | h2h_or_binary | 01 1-3c | 5,075 | 10 | -3.45% | -4.15% to -1.87% | 6.48% | 66.69% | 1.03% | -5.15% | -1.00% | 0.00% |

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
