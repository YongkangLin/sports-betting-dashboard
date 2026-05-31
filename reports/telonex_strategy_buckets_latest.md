# Telonex Strategy Bucket Audit

- Generated: 2026-05-31T14:45:43.636039+00:00
- Labels: 5,418,878
- Markets/tokens: 632 / 1261
- Sports: {'soccer': 2625089, 'baseball_mlb': 1731351, 'basketball_nba': 900769, 'americanfootball_nfl': 66302, 'basketball_wnba': 55474, 'tennis': 26200, 'icehockey_nhl': 13693}
- Label SHA256: `a0a6e936af3ca1f7dbe20717dd54aad3f0078761c7c11a0784d7fb95862677da`
- Odds API feature coverage: 67.36%
- Odds API split coverage: `{'test': {'rows': 852668, 'matched_rows': 394094, 'row_coverage': 0.4621892694460212, 'markets': 48, 'matched_markets': 22}, 'train': {'rows': 2060552, 'matched_rows': 1459594, 'row_coverage': 0.7083509661488766, 'markets': 220, 'matched_markets': 205}, 'unobserved': {'rows': 1546280, 'matched_rows': 1175658, 'row_coverage': 0.7603137853428874, 'markets': 317, 'matched_markets': 226}, 'val': {'rows': 959378, 'matched_rows': 621070, 'row_coverage': 0.6473673567665716, 'markets': 47, 'matched_markets': 31}}`
- Player/news feature coverage: 0.00% / status `missing_public_timestamped_feed`
- Play-by-play feature coverage: 27.86% / status `available`
- Sentiment feature coverage: 0.00% / status `missing_feature_file`
- Minimum bucket rows/markets: 1000 / 5
- Positive test buckets total/taker/maker: 0 / 0 / 0
- Executable taker gate: False
- Maker research lead gate: False

This is a fixed-bucket audit, not a model-selection sweep. The buckets are meant to falsify broad strategy hypotheses before any threshold tuning.

## Price Buckets

| Side | split | price_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 07 >=95c near_certain | 4,841 | 7 | -0.21% | -0.29% to 0.12% | 12.99% | 96.38% | 2.03% | -50.47% | -0.76% | 0.00% |
| maker | test | 06 85-95c favorite | 85,028 | 24 | -0.64% | -0.82% to -0.53% | 2.96% | 90.33% | 1.72% | -2.35% | -0.06% | 0.00% |
| maker | test | 05 70-85c high_mid | 125,044 | 35 | -1.43% | -1.61% to -1.31% | 1.45% | 78.18% | 4.00% | -4.78% | -0.28% | 0.00% |
| taker | test | 07 >=95c near_certain | 4,841 | 7 | -2.23% | -2.72% to -0.81% | 2.52% | 96.38% | 2.03% | -50.47% | -0.76% | 0.00% |
| maker | test | 04 30-70c mid | 421,868 | 35 | -2.94% | -3.09% to -2.82% | 2.02% | 50.05% | 7.99% | -0.80% | 0.00% | 0.00% |
| taker | test | 06 85-95c favorite | 85,028 | 24 | -2.48% | -3.16% to -1.99% | 0.21% | 90.33% | 1.72% | -2.35% | -0.06% | 0.00% |
| maker | test | 02 5-15c longshot | 85,209 | 24 | -5.40% | -5.57% to -5.21% | 1.81% | 9.69% | 1.73% | 1.28% | 0.06% | 0.00% |
| maker | test | 03 15-30c low_mid | 125,763 | 35 | -5.17% | -5.62% to -4.74% | 2.44% | 21.90% | 4.07% | 1.95% | 0.28% | 0.00% |
| taker | test | 05 70-85c high_mid | 125,044 | 35 | -6.27% | -8.32% to -5.00% | 0.14% | 78.18% | 4.00% | -4.78% | -0.28% | 0.00% |
| maker | test | 01 3-5c thin_tail | 4,418 | 7 | -6.52% | -19.08% to -5.87% | 7.74% | 3.91% | 2.21% | 48.82% | 0.83% | 0.00% |
| taker | test | 02 5-15c longshot | 85,209 | 24 | -21.33% | -25.51% to -17.46% | 0.14% | 9.69% | 1.73% | 1.28% | 0.06% | 0.00% |
| taker | test | 04 30-70c mid | 421,868 | 35 | -17.29% | -26.71% to -11.19% | 0.19% | 50.05% | 7.99% | -0.80% | 0.00% | 0.00% |
| taker | test | 03 15-30c low_mid | 125,763 | 35 | -21.57% | -28.10% to -16.56% | 0.06% | 21.90% | 4.07% | 1.95% | 0.28% | 0.00% |
| taker | test | 01 3-5c thin_tail | 4,418 | 7 | -49.01% | -58.35% to -37.72% | 0.14% | 3.91% | 2.21% | 48.82% | 0.83% | 0.00% |
| maker | val | 07 >=95c near_certain | 1,424 | 12 | -0.21% | -0.68% to 0.05% | 38.27% | 97.65% | 0.84% | -44.25% | -1.15% | 0.00% |
| maker | train | 06 85-95c favorite | 547,192 | 175 | -0.76% | -0.78% to -0.74% | 1.88% | 87.92% | 1.05% | -2.78% | -0.02% | 0.00% |
| maker | unobserved | 06 85-95c favorite | 359,692 | 163 | -0.79% | -0.81% to -0.77% | 2.25% | 87.40% | 1.08% | -1.52% | -0.01% | 0.00% |
| maker | train | 07 >=95c near_certain | 2,468 | 21 | -0.24% | -0.82% to 0.03% | 32.29% | 97.98% | 0.71% | -41.23% | -1.42% | 0.00% |
| maker | val | 06 85-95c favorite | 87,326 | 25 | -0.79% | -0.84% to -0.74% | 2.34% | 87.93% | 1.90% | -2.05% | -0.08% | 0.00% |
| maker | unobserved | 05 70-85c high_mid | 63,620 | 93 | -1.20% | -1.34% to -1.07% | 3.73% | 80.24% | 1.27% | -1.57% | -0.02% | 0.00% |

## Sport x Price Buckets

| Side | split | sport_family | price_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | soccer | 06 85-95c favorite | 84,454 | 20 | -0.65% | -0.83% to -0.54% | 2.67% | 90.33% | 1.73% | -1.80% | -0.00% | 0.00% |
| maker | test | soccer | 05 70-85c high_mid | 122,944 | 26 | -1.43% | -1.58% to -1.30% | 1.29% | 78.27% | 3.97% | -4.07% | -0.00% | 0.00% |
| maker | test | soccer | 04 30-70c mid | 195,803 | 24 | -2.81% | -3.09% to -2.66% | 1.21% | 50.08% | 5.27% | -0.78% | 0.00% | 0.00% |
| maker | test | baseball_mlb | 04 30-70c mid | 197,037 | 10 | -3.09% | -3.16% to -3.02% | 2.67% | 50.01% | 6.19% | -0.79% | -0.00% | 0.00% |
| taker | test | soccer | 06 85-95c favorite | 84,454 | 20 | -2.48% | -3.29% to -1.99% | 0.02% | 90.33% | 1.73% | -1.80% | -0.00% | 0.00% |
| maker | test | baseball_mlb | 05 70-85c high_mid | 1,388 | 8 | -1.81% | -4.77% to 0.21% | 15.56% | 73.37% | 7.21% | -17.45% | -2.91% | 0.00% |
| maker | test | soccer | 02 5-15c longshot | 84,635 | 20 | -5.37% | -5.51% to -5.19% | 1.68% | 9.69% | 1.74% | 0.73% | 0.00% | 0.00% |
| maker | test | soccer | 03 15-30c low_mid | 123,480 | 26 | -5.18% | -5.66% to -4.74% | 2.28% | 21.79% | 4.03% | 1.28% | 0.00% | 0.00% |
| taker | test | soccer | 05 70-85c high_mid | 122,944 | 26 | -6.22% | -7.82% to -4.93% | 0.01% | 78.27% | 3.97% | -4.07% | -0.00% | 0.00% |
| maker | test | baseball_mlb | 03 15-30c low_mid | 1,465 | 8 | -5.55% | -13.23% to -1.40% | 15.90% | 26.81% | 7.70% | 13.96% | 2.83% | 0.00% |
| taker | test | baseball_mlb | 04 30-70c mid | 197,037 | 10 | -14.38% | -17.81% to -10.88% | 0.39% | 50.01% | 6.19% | -0.79% | -0.00% | 0.00% |
| taker | test | baseball_mlb | 05 70-85c high_mid | 1,388 | 8 | -10.88% | -22.20% to -5.89% | 12.03% | 73.37% | 7.21% | -17.45% | -2.91% | 0.00% |
| taker | test | soccer | 04 30-70c mid | 195,803 | 24 | -12.53% | -24.05% to -8.39% | 0.01% | 50.08% | 5.27% | -0.78% | 0.00% | 0.00% |
| taker | test | soccer | 02 5-15c longshot | 84,635 | 20 | -21.33% | -25.35% to -18.07% | 0.06% | 9.69% | 1.74% | 0.73% | 0.00% | 0.00% |
| taker | test | soccer | 03 15-30c low_mid | 123,480 | 26 | -21.52% | -27.38% to -16.54% | 0.02% | 21.79% | 4.03% | 1.28% | 0.00% | 0.00% |
| taker | test | baseball_mlb | 03 15-30c low_mid | 1,465 | 8 | -29.60% | -51.51% to -18.19% | 3.62% | 26.81% | 7.70% | 13.96% | 2.83% | 0.00% |
| maker | train | basketball_nba | 06 85-95c favorite | 260,837 | 86 | -0.70% | -0.73% to -0.66% | 1.99% | 88.86% | 1.05% | -2.39% | -0.00% | 0.00% |
| maker | unobserved | americanfootball_nfl | 06 85-95c favorite | 21,657 | 12 | -0.73% | -0.76% to -0.70% | 1.82% | 88.07% | 1.03% | -1.62% | -0.06% | 0.00% |
| maker | train | baseball_mlb | 07 >=95c near_certain | 2,378 | 15 | -0.23% | -0.78% to 0.03% | 33.05% | 98.07% | 0.70% | -42.94% | -1.34% | 0.00% |
| maker | unobserved | soccer | 06 85-95c favorite | 305,726 | 98 | -0.79% | -0.81% to -0.77% | 2.04% | 87.35% | 1.07% | -1.49% | -0.01% | 0.00% |

## Horizon x Spread Buckets

| Side | split | horizon_sec | spread_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 30 | 01 1-3c | 104,223 | 47 | -2.19% | -2.43% to -1.94% | 0.61% | 50.09% | 1.35% | -0.71% | 0.00% | 0.00% |
| maker | test | 60 | 01 1-3c | 102,418 | 47 | -2.21% | -2.44% to -1.91% | 0.70% | 50.08% | 1.34% | -0.70% | 0.00% | 0.00% |
| maker | test | 300 | 01 1-3c | 103,532 | 47 | -2.21% | -2.45% to -1.93% | 1.10% | 50.01% | 1.35% | -0.70% | 0.00% | 0.00% |
| maker | test | 120 | 01 1-3c | 101,462 | 47 | -2.22% | -2.46% to -1.98% | 0.86% | 50.07% | 1.34% | -0.70% | -0.00% | 0.00% |
| maker | test | 900 | 01 1-3c | 101,884 | 47 | -2.24% | -2.48% to -1.97% | 1.77% | 50.02% | 1.34% | -0.70% | 0.00% | 0.00% |
| maker | test | 30 | 02 3-5c | 17,575 | 41 | -2.18% | -2.61% to -1.74% | 3.43% | 53.47% | 4.05% | -2.26% | 0.01% | 0.00% |
| maker | test | 60 | 02 3-5c | 17,406 | 41 | -2.24% | -2.67% to -1.78% | 3.32% | 53.30% | 4.05% | -2.27% | 0.01% | 0.00% |
| maker | test | 300 | 02 3-5c | 17,623 | 40 | -2.25% | -2.68% to -1.75% | 3.13% | 53.66% | 4.05% | -2.29% | 0.01% | 0.00% |
| maker | test | 120 | 02 3-5c | 16,778 | 41 | -2.25% | -2.69% to -1.73% | 3.47% | 53.40% | 4.07% | -2.28% | 0.01% | 0.00% |
| maker | test | 900 | 02 3-5c | 17,033 | 40 | -2.26% | -2.70% to -1.79% | 5.11% | 53.59% | 4.05% | -2.28% | 0.01% | 0.00% |
| maker | test | 30 | 03 5-10c | 18,183 | 38 | -2.49% | -2.84% to -2.25% | 2.11% | 51.51% | 7.06% | -3.39% | -0.03% | 0.00% |
| maker | test | 60 | 03 5-10c | 17,940 | 38 | -2.48% | -2.86% to -2.22% | 2.59% | 51.54% | 7.06% | -3.42% | -0.03% | 0.00% |
| maker | test | 300 | 03 5-10c | 17,580 | 37 | -2.45% | -2.88% to -2.19% | 4.89% | 51.55% | 7.06% | -3.39% | -0.03% | 0.00% |
| maker | test | 120 | 03 5-10c | 17,603 | 38 | -2.49% | -2.93% to -2.24% | 3.27% | 51.54% | 7.08% | -3.41% | -0.03% | 0.00% |
| maker | test | 900 | 03 5-10c | 17,400 | 38 | -2.47% | -3.03% to -2.15% | 7.87% | 51.56% | 7.06% | -3.40% | -0.03% | 0.00% |
| maker | test | 900 | 04 >10c | 15,705 | 34 | -2.73% | -3.47% to -1.99% | 13.89% | 49.98% | 35.04% | -11.99% | 0.00% | 0.00% |
| maker | test | 60 | 00 <=1c | 16,374 | 38 | -2.07% | -3.73% to -1.26% | 0.49% | 44.33% | 0.99% | -0.07% | -0.00% | 0.00% |
| maker | test | 120 | 00 <=1c | 16,146 | 37 | -2.09% | -3.74% to -1.28% | 0.69% | 44.33% | 0.99% | -0.08% | -0.00% | 0.00% |
| maker | test | 30 | 00 <=1c | 16,464 | 37 | -2.07% | -3.75% to -1.27% | 0.29% | 44.06% | 0.99% | -0.05% | -0.00% | 0.00% |
| maker | test | 300 | 00 <=1c | 16,434 | 37 | -2.11% | -3.89% to -1.23% | 0.94% | 44.35% | 0.99% | -0.06% | 0.00% | 0.00% |

## Odds Edge Buckets

| Side | split | odds_edge_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 00 <=-10c against | 2,252 | 6 | -0.13% | -2.02% to 0.71% | 40.23% | 83.25% | 1.03% | -35.75% | -2.67% | 0.00% |
| maker | test | 02 -5c--2c against | 23,926 | 11 | -1.71% | -2.40% to -1.38% | 0.59% | 71.23% | 1.27% | -3.93% | -0.03% | 0.00% |
| maker | test | 03 -2c-+2c neutral | 247,444 | 22 | -2.11% | -2.66% to -1.60% | 0.42% | 55.61% | 1.37% | -1.27% | -0.00% | 0.00% |
| maker | test | 04 +2c-+5c edge | 97,470 | 22 | -3.55% | -4.10% to -2.91% | 0.93% | 31.49% | 1.94% | 1.01% | 0.02% | 0.00% |
| maker | test | 01 -10c--5c against | 7,390 | 8 | -2.81% | -4.37% to -1.28% | 2.33% | 54.29% | 1.27% | -9.06% | -0.08% | 0.00% |
| maker | test | 05 +5c-+10c edge | 11,630 | 11 | -3.62% | -4.88% to -3.28% | 2.75% | 41.16% | 3.10% | 4.83% | -0.02% | 0.00% |
| taker | test | 03 -2c-+2c neutral | 247,444 | 22 | -5.58% | -6.27% to -4.99% | 0.08% | 44.39% | 1.37% | -0.10% | 0.00% | 0.00% |
| taker | test | 02 -5c--2c against | 97,470 | 22 | -4.41% | -6.98% to -3.04% | 0.04% | 68.51% | 1.94% | -2.94% | -0.02% | 0.00% |
| maker | test | 06 >+10c edge | 3,982 | 9 | -3.29% | -8.20% to 2.60% | 18.91% | 25.88% | 8.08% | 20.47% | 2.27% | 0.00% |
| taker | test | 04 +2c-+5c edge | 23,926 | 11 | -8.35% | -9.55% to -6.98% | 0.26% | 28.77% | 1.27% | 2.66% | 0.03% | 0.00% |
| taker | test | 05 +5c-+10c edge | 7,390 | 8 | -6.01% | -13.67% to -5.27% | 1.41% | 45.71% | 1.27% | 7.80% | 0.08% | 0.00% |
| taker | test | 01 -10c--5c against | 11,630 | 11 | -7.43% | -14.20% to -5.65% | 1.26% | 58.84% | 3.10% | -7.94% | 0.02% | 0.00% |
| taker | test | 00 <=-10c against | 3,982 | 9 | -10.63% | -21.48% to -2.66% | 13.79% | 74.12% | 8.08% | -28.55% | -2.27% | 0.00% |
| taker | test | 06 >+10c edge | 2,252 | 6 | -14.13% | -22.76% to -6.86% | 11.41% | 16.75% | 1.03% | 34.72% | 2.67% | 0.00% |
| maker | val | 00 <=-10c against | 5,969 | 14 | -0.32% | -1.27% to 0.54% | 38.28% | 79.44% | 1.10% | -33.00% | -2.64% | 0.00% |
| maker | train | 03 -2c-+2c neutral | 1,012,876 | 198 | -1.49% | -1.62% to -1.38% | 1.28% | 56.24% | 1.06% | -0.90% | -0.00% | 0.00% |
| maker | unobserved | 03 -2c-+2c neutral | 1,004,357 | 221 | -1.71% | -1.83% to -1.59% | 1.45% | 52.09% | 1.09% | -0.72% | -0.01% | 0.00% |
| maker | train | 02 -5c--2c against | 75,837 | 108 | -1.44% | -1.87% to -1.05% | 1.47% | 69.83% | 1.22% | -4.10% | -0.08% | 0.00% |
| maker | train | 00 <=-10c against | 22,074 | 26 | -1.26% | -2.15% to -0.53% | 17.65% | 77.30% | 1.10% | -38.10% | -1.34% | 0.00% |
| maker | unobserved | 01 -10c--5c against | 7,526 | 34 | -2.16% | -2.51% to -1.26% | 3.87% | 60.13% | 1.66% | -7.99% | -0.33% | 0.00% |

## Sport x Odds Edge Buckets

| Side | split | sport_family | odds_edge_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | baseball_mlb | 00 <=-10c against | 2,252 | 6 | -0.13% | -2.02% to 0.71% | 40.23% | 83.25% | 1.03% | -35.75% | -2.67% | 0.00% |
| maker | test | soccer | 03 -2c-+2c neutral | 150,213 | 13 | -1.63% | -2.24% to -1.00% | 0.42% | 59.42% | 1.42% | -1.51% | -0.00% | 0.00% |
| maker | test | soccer | 02 -5c--2c against | 21,588 | 6 | -1.65% | -2.35% to -1.32% | 0.19% | 72.69% | 1.17% | -3.74% | -0.02% | 0.00% |
| maker | test | baseball_mlb | 02 -5c--2c against | 2,338 | 5 | -2.40% | -2.81% to -1.90% | 4.23% | 57.79% | 2.19% | -5.71% | -0.08% | 0.00% |
| maker | test | baseball_mlb | 03 -2c-+2c neutral | 84,228 | 8 | -3.03% | -3.07% to -2.99% | 0.48% | 49.92% | 1.27% | -0.87% | -0.01% | 0.00% |
| maker | test | baseball_mlb | 04 +2c-+5c edge | 11,056 | 8 | -2.84% | -3.16% to -2.59% | 2.79% | 50.70% | 2.75% | 0.23% | 0.07% | 0.00% |
| maker | test | baseball_mlb | 01 -10c--5c against | 7,386 | 7 | -2.82% | -4.21% to -1.70% | 2.29% | 54.27% | 1.27% | -9.06% | -0.08% | 0.00% |
| maker | test | soccer | 04 +2c-+5c edge | 82,287 | 13 | -3.84% | -4.50% to -3.07% | 0.63% | 27.75% | 1.72% | 1.21% | 0.01% | 0.00% |
| maker | test | baseball_mlb | 05 +5c-+10c edge | 9,271 | 7 | -3.46% | -4.62% to -3.17% | 3.16% | 45.33% | 2.43% | 5.90% | -0.03% | 0.00% |
| taker | test | baseball_mlb | 03 -2c-+2c neutral | 84,228 | 8 | -5.40% | -5.93% to -5.02% | 0.20% | 50.08% | 1.27% | -0.40% | 0.01% | 0.00% |
| taker | test | soccer | 02 -5c--2c against | 82,287 | 13 | -3.80% | -6.37% to -2.17% | 0.00% | 72.25% | 1.72% | -2.93% | -0.01% | 0.00% |
| taker | test | soccer | 03 -2c-+2c neutral | 150,213 | 13 | -5.73% | -6.90% to -4.60% | 0.03% | 40.58% | 1.42% | 0.09% | 0.00% | 0.00% |
| taker | test | soccer | 04 +2c-+5c edge | 21,588 | 6 | -8.33% | -9.63% to -6.87% | 0.03% | 27.31% | 1.17% | 2.57% | 0.02% | 0.00% |
| maker | test | baseball_mlb | 06 >+10c edge | 3,291 | 7 | -3.59% | -9.71% to 3.43% | 20.12% | 25.05% | 4.72% | 24.48% | 2.31% | 0.00% |
| taker | test | baseball_mlb | 02 -5c--2c against | 11,056 | 8 | -8.46% | -10.90% to -5.97% | 0.33% | 49.30% | 2.75% | -2.98% | -0.07% | 0.00% |
| taker | test | baseball_mlb | 04 +2c-+5c edge | 2,338 | 5 | -8.50% | -13.06% to -5.54% | 2.35% | 42.21% | 2.19% | 3.52% | 0.08% | 0.00% |
| taker | test | baseball_mlb | 05 +5c-+10c edge | 7,386 | 7 | -6.00% | -13.62% to -5.26% | 1.41% | 45.73% | 1.27% | 7.80% | 0.08% | 0.00% |
| taker | test | baseball_mlb | 00 <=-10c against | 3,291 | 7 | -6.15% | -14.56% to -1.66% | 16.68% | 74.95% | 4.72% | -29.20% | -2.31% | 0.00% |
| taker | test | baseball_mlb | 01 -10c--5c against | 9,271 | 7 | -6.97% | -15.68% to -5.19% | 1.59% | 54.67% | 2.43% | -8.33% | 0.03% | 0.00% |
| taker | test | baseball_mlb | 06 >+10c edge | 2,252 | 6 | -14.13% | -22.76% to -6.86% | 11.41% | 16.75% | 1.03% | 34.72% | 2.67% | 0.00% |

## Predeclared Strategy Support

| Split | Strategy | Rows | Markets | Reportable | ROI | Positive | Odds gap | Line-lag gap | Reason |
|---|---|---:|---:|---|---:|---:|---:|---:|---|
| train | favorite_longshot_fade_v2 | 785,127 | 212 | yes | -2.38% | 0.39% | -2.59% | -0.05% | reportable |
| train | sharp_consensus_clob_mispricing | 112,498 | 119 | yes | -6.68% | 1.85% | 10.19% | 0.36% | reportable |
| train | line_lag_clv_capture | 58 | 3 | no | -13.12% | 1.72% | 3.01% | 2.48% | rows 58 < 1,000; markets 3 < 5 |
| val | favorite_longshot_fade_v2 | 302,793 | 43 | yes | -3.45% | 0.50% | -1.94% | -0.07% | reportable |
| val | sharp_consensus_clob_mispricing | 24,169 | 19 | yes | -6.24% | 4.82% | 10.31% | 0.80% | reportable |
| val | line_lag_clv_capture | 0 | 0 | no | n/a | n/a | n/a | n/a | no candidate rows; rows 0 < 1,000; markets 0 < 5 |
| test | favorite_longshot_fade_v2 | 302,292 | 46 | yes | -3.56% | 0.16% | -2.22% | -0.06% | reportable |
| test | sharp_consensus_clob_mispricing | 25,898 | 11 | yes | -7.48% | 1.61% | 6.82% | 0.39% | reportable |
| test | line_lag_clv_capture | 0 | 0 | no | n/a | n/a | n/a | n/a | no candidate rows; rows 0 < 1,000; markets 0 < 5 |
| unobserved | favorite_longshot_fade_v2 | 566,442 | 253 | yes | -2.56% | 0.22% | -1.59% | -0.01% | reportable |
| unobserved | sharp_consensus_clob_mispricing | 33,767 | 81 | yes | -7.19% | 0.79% | 4.45% | 0.29% | reportable |
| unobserved | line_lag_clv_capture | 12 | 1 | no | -8.48% | 0.00% | 1.48% | 7.59% | rows 12 < 1,000; markets 1 < 5 |

## Predeclared Strategy Rows

| Side | split | strategy | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| taker | test | favorite_longshot_fade_v2 | 302,292 | 46 | -3.56% | -4.12% to -3.05% | 0.16% | 74.77% | 1.63% | -2.22% | -0.06% | 0.00% |
| taker | test | sharp_consensus_clob_mispricing | 25,898 | 11 | -7.48% | -10.77% to -5.83% | 1.61% | 30.78% | 1.08% | 6.82% | 0.39% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 785,127 | 212 | -2.38% | -2.58% to -2.22% | 0.39% | 82.23% | 1.16% | -2.59% | -0.05% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 566,442 | 253 | -2.56% | -2.71% to -2.41% | 0.22% | 79.85% | 1.17% | -1.59% | -0.01% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 302,793 | 43 | -3.45% | -3.87% to -3.12% | 0.50% | 73.98% | 1.50% | -1.94% | -0.07% | 0.00% |
| taker | val | sharp_consensus_clob_mispricing | 24,169 | 19 | -6.24% | -8.06% to -5.20% | 4.82% | 36.53% | 1.03% | 10.31% | 0.80% | 0.00% |
| taker | unobserved | sharp_consensus_clob_mispricing | 33,767 | 81 | -7.19% | -8.31% to -6.25% | 0.79% | 38.65% | 1.52% | 4.45% | 0.29% | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 112,498 | 119 | -6.68% | -8.41% to -5.81% | 1.85% | 32.27% | 1.19% | 10.19% | 0.36% | 0.00% |

## Predeclared Strategy Buckets

| Side | split | strategy | strategy_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| taker | test | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 60,833 | 19 | -2.22% | -2.54% to -2.01% | 0.03% | 89.41% | 1.39% | -1.66% | -0.00% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 52,860 | 11 | -2.67% | -2.85% to -2.57% | 0.01% | 79.44% | 1.16% | -3.30% | 0.01% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 01 1-3c | 53,398 | 8 | -3.78% | -4.01% to -3.25% | 0.00% | 69.13% | 1.36% | -1.93% | -0.00% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 02 3-5c | 11,753 | 12 | -3.99% | -4.32% to -3.54% | 0.00% | 88.76% | 3.16% | -6.52% | -4.50% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 00 <=1c | 8,237 | 7 | -4.45% | -4.66% to -4.34% | 0.07% | 56.50% | 1.00% | -0.35% | -0.04% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | soccer | h2h_or_binary | 01 1-3c | 19,738 | 7 | -4.57% | -4.71% to -4.14% | 0.02% | 61.49% | 1.41% | -3.48% | 0.03% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 01 1-3c | 22,717 | 7 | -4.72% | -5.03% to -4.55% | 0.31% | 57.16% | 1.21% | -1.07% | -0.11% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 02 3-5c | 7,700 | 10 | -6.18% | -6.62% to -5.40% | 0.00% | 79.91% | 4.09% | -5.32% | 0.00% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 02 3-5c | 7,974 | 7 | -8.20% | -8.89% to -7.25% | 0.01% | 69.57% | 4.65% | -2.55% | -0.01% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 02 3-5c | 6,047 | 6 | -9.79% | -10.44% to -9.28% | 0.07% | 57.28% | 4.29% | -1.00% | 0.05% | 0.00% |
| taker | test | sharp_consensus_clob_mispricing | 03 >+7c | baseball_mlb | h2h_or_binary | books=9 | 8,353 | 6 | -6.17% | -19.68% to -5.23% | 3.89% | 39.12% | 0.99% | 15.38% | 0.73% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | basketball_nba | h2h_or_binary | 01 1-3c | 258,015 | 86 | -1.83% | -1.88% to -1.78% | 0.03% | 88.80% | 1.04% | -2.38% | -0.00% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 04 85-95c | americanfootball_nfl | h2h_or_binary | 01 1-3c | 21,592 | 12 | -1.86% | -1.90% to -1.83% | 0.32% | 88.05% | 1.02% | -1.59% | -0.06% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 278,211 | 72 | -1.97% | -2.01% to -1.93% | 0.07% | 87.03% | 1.05% | -2.72% | -0.00% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 311,046 | 99 | -1.99% | -2.02% to -1.96% | 0.04% | 87.31% | 1.08% | -1.50% | -0.01% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 04 85-95c | basketball_nba | h2h_or_binary | 01 1-3c | 23,660 | 40 | -1.94% | -2.04% to -1.85% | 0.10% | 87.52% | 1.05% | -1.33% | -0.02% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 22,841 | 36 | -2.11% | -2.14% to -2.08% | 0.18% | 84.43% | 1.02% | -1.18% | 0.05% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 65,489 | 10 | -2.06% | -2.18% to -1.85% | 0.06% | 87.54% | 1.15% | -1.31% | -0.02% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | basketball_nba | h2h_or_binary | 00 <=1c | 3,247 | 9 | -2.36% | -2.41% to -2.31% | 0.09% | 81.50% | 1.00% | -2.06% | -0.01% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 29,554 | 26 | -2.22% | -2.43% to -2.09% | 0.15% | 83.11% | 1.03% | -1.16% | 0.03% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 03 75-85c | basketball_nba | h2h_or_binary | 01 1-3c | 13,930 | 19 | -2.47% | -2.60% to -2.23% | 0.06% | 79.71% | 1.04% | -1.84% | 0.02% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 04 85-95c | baseball_mlb | h2h_or_binary | 01 1-3c | 1,212 | 10 | -1.76% | -2.67% to -0.80% | 25.58% | 89.33% | 1.14% | -39.61% | -3.13% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | baseball_mlb | h2h_or_binary | 01 1-3c | 2,521 | 15 | -2.24% | -2.89% to -1.63% | 23.80% | 89.57% | 1.14% | -35.85% | -3.10% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | basketball_nba | h2h_or_binary | 01 1-3c | 36,610 | 26 | -2.63% | -3.00% to -2.28% | 0.28% | 81.88% | 1.29% | -1.02% | 0.02% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 47,679 | 8 | -3.13% | -3.38% to -2.52% | 0.04% | 80.47% | 1.60% | -1.33% | 0.01% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | basketball_nba | h2h_or_binary | 00 <=1c | 3,007 | 6 | -3.32% | -3.42% to -3.15% | 0.00% | 68.50% | 1.00% | -1.97% | -0.04% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 02 65-75c | basketball_nba | h2h_or_binary | 00 <=1c | 1,589 | 6 | -3.45% | -3.50% to -3.22% | 0.00% | 68.50% | 1.00% | -7.10% | -0.09% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | basketball_nba | h2h_or_binary | 01 1-3c | 27,060 | 11 | -3.38% | -3.56% to -3.14% | 0.18% | 68.46% | 1.07% | -1.43% | -0.01% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 01 1-3c | 35,785 | 5 | -3.33% | -3.60% to -3.20% | 0.00% | 70.90% | 1.13% | -2.48% | 0.03% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 02 65-75c | basketball_nba | h2h_or_binary | 01 1-3c | 10,053 | 12 | -3.52% | -3.63% to -3.34% | 0.09% | 67.76% | 1.11% | -2.52% | 0.01% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 01 1-3c | 12,940 | 6 | -3.36% | -3.65% to -3.14% | 0.12% | 69.90% | 1.11% | -1.46% | 0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 01 1-3c | 3,660 | 5 | -3.19% | -3.98% to -2.76% | 0.00% | 70.44% | 1.00% | -1.86% | 0.15% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 01 55-65c | soccer | h2h_or_binary | 01 1-3c | 20,606 | 7 | -3.99% | -4.10% to -3.84% | 0.01% | 61.47% | 1.06% | -1.76% | 0.01% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 01 55-65c | basketball_nba | h2h_or_binary | 01 1-3c | 24,717 | 12 | -4.04% | -4.22% to -3.90% | 0.06% | 61.38% | 1.09% | -2.66% | 0.03% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | basketball_nba | h2h_or_binary | 01 1-3c | 11,601 | 13 | -4.06% | -4.29% to -3.86% | 0.17% | 59.87% | 1.02% | -1.12% | 0.01% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 01 1-3c | 39,043 | 10 | -4.24% | -4.36% to -4.12% | 0.87% | 59.58% | 1.10% | -1.28% | -0.05% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 00 <=1c | 5,841 | 9 | -4.30% | -4.42% to -1.07% | 1.01% | 56.50% | 1.00% | -1.57% | -0.04% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 00 <=1c | 6,078 | 10 | -4.31% | -4.46% to -3.76% | 1.22% | 56.54% | 1.00% | -0.41% | -0.03% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 01 55-65c | baseball_mlb | h2h_or_binary | 01 1-3c | 59,454 | 16 | -4.39% | -4.57% to -4.24% | 0.91% | 59.67% | 1.19% | -1.20% | -0.07% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 02 3-5c | 1,745 | 7 | -4.19% | -4.73% to -4.03% | 0.06% | 88.18% | 3.20% | -5.55% | -0.41% | 0.00% |

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
