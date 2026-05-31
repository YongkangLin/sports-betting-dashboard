# Telonex Strategy Bucket Audit

- Generated: 2026-05-31T18:43:48.927968+00:00
- Labels: 5,392,062
- Markets/tokens: 1257 / 2513
- Sports: {'soccer': 3263258, 'icehockey_nhl': 1222278, 'americanfootball_nfl': 415814, 'basketball_nba': 250430, 'basketball_wnba': 191728, 'baseball_mlb': 48554}
- Label SHA256: `50310af44be32d0d81f82db65ef9aad936082580d7cb37b9e1e6ba17e41afd69`
- Odds API feature coverage: 94.54%
- Odds API split coverage: `{'test': {'rows': 810914, 'matched_rows': 782836, 'row_coverage': 0.9653748732911258, 'markets': 178, 'matched_markets': 172}, 'train': {'rows': 3123944, 'matched_rows': 2872556, 'row_coverage': 0.9195286471204349, 'markets': 828, 'matched_markets': 815}, 'unobserved': {'rows': 531302, 'matched_rows': 531302, 'row_coverage': 1.0, 'markets': 74, 'matched_markets': 74}, 'val': {'rows': 925902, 'matched_rows': 910706, 'row_coverage': 0.9835878959112303, 'markets': 177, 'matched_markets': 164}}`
- Player/news feature coverage: 0.00% / status `missing_public_timestamped_feed`
- Play-by-play feature coverage: 0.41% / status `available`
- Sentiment feature coverage: 0.00% / status `missing_feature_file`
- Minimum bucket rows/markets: 1000 / 5
- Positive test buckets total/taker/maker: 0 / 0 / 0
- Executable taker gate: False
- Maker research lead gate: False

This is a fixed-bucket audit, not a model-selection sweep. The buckets are meant to falsify broad strategy hypotheses before any threshold tuning.

## Price Buckets

| Side | split | price_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 06 85-95c favorite | 142,092 | 53 | -0.76% | -0.79% to -0.74% | 1.62% | 87.74% | 1.02% | -3.61% | -0.01% | 0.00% |
| maker | test | 05 70-85c high_mid | 39,627 | 51 | -1.39% | -1.59% to -1.19% | 2.48% | 78.62% | 1.49% | -1.48% | -0.04% | 0.00% |
| taker | test | 06 85-95c favorite | 142,092 | 53 | -1.88% | -1.93% to -1.85% | 0.24% | 87.74% | 1.02% | -3.61% | -0.01% | 0.00% |
| maker | test | 04 30-70c mid | 445,109 | 116 | -2.92% | -2.95% to -2.88% | 0.74% | 50.03% | 1.89% | -4.22% | -0.00% | 0.00% |
| taker | test | 05 70-85c high_mid | 39,627 | 51 | -3.21% | -3.73% to -2.71% | 0.83% | 78.62% | 1.49% | -1.48% | -0.04% | 0.00% |
| maker | test | 03 15-30c low_mid | 40,206 | 51 | -4.79% | -5.03% to -4.58% | 2.20% | 21.50% | 1.52% | -0.37% | 0.05% | 0.00% |
| maker | test | 02 5-15c longshot | 142,079 | 53 | -5.29% | -5.38% to -5.19% | 1.39% | 12.26% | 1.02% | 2.59% | 0.01% | 0.00% |
| taker | test | 04 30-70c mid | 445,109 | 116 | -6.52% | -8.95% to -5.03% | 0.20% | 50.03% | 1.89% | -4.22% | -0.00% | 0.00% |
| taker | test | 03 15-30c low_mid | 40,206 | 51 | -11.41% | -12.95% to -9.99% | 0.55% | 21.50% | 1.52% | -0.37% | 0.05% | 0.00% |
| taker | test | 02 5-15c longshot | 142,079 | 53 | -13.03% | -13.47% to -12.70% | 0.19% | 12.26% | 1.02% | 2.59% | 0.01% | 0.00% |
| maker | train | 07 >=95c near_certain | 4,067 | 16 | -0.27% | -0.35% to -0.04% | 7.65% | 96.41% | 0.80% | -6.45% | -0.32% | 0.00% |
| maker | train | 06 85-95c favorite | 164,307 | 119 | -0.73% | -0.78% to -0.69% | 2.41% | 88.44% | 1.11% | -1.64% | -0.03% | 0.00% |
| maker | unobserved | 06 85-95c favorite | 212,511 | 64 | -0.79% | -0.82% to -0.77% | 2.05% | 87.32% | 1.06% | -1.49% | -0.01% | 0.00% |
| maker | val | 06 85-95c favorite | 77,733 | 43 | -0.80% | -0.86% to -0.74% | 2.56% | 87.18% | 1.10% | -1.82% | -0.00% | 0.00% |
| maker | val | 07 >=95c near_certain | 1,487 | 15 | -0.40% | -0.96% to -0.06% | 37.39% | 97.74% | 0.67% | -10.16% | -6.32% | 0.00% |
| taker | train | 07 >=95c near_certain | 4,067 | 16 | -1.07% | -1.31% to -0.57% | 1.11% | 96.41% | 0.80% | -6.45% | -0.32% | 0.00% |
| maker | unobserved | 05 70-85c high_mid | 29,048 | 27 | -1.10% | -1.33% to -0.91% | 3.12% | 81.12% | 1.14% | -1.30% | 0.03% | 0.00% |
| maker | train | 05 70-85c high_mid | 634,194 | 393 | -1.49% | -1.52% to -1.46% | 0.90% | 75.80% | 1.23% | -1.26% | -0.02% | 0.00% |
| maker | val | 05 70-85c high_mid | 41,384 | 47 | -1.43% | -1.60% to -1.19% | 2.67% | 75.60% | 1.08% | -4.09% | -0.01% | 0.00% |
| taker | val | 07 >=95c near_certain | 1,487 | 15 | -1.06% | -1.69% to -0.65% | 13.85% | 97.74% | 0.67% | -10.16% | -6.32% | 0.00% |

## Sport x Price Buckets

| Side | split | sport_family | price_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | soccer | 06 85-95c favorite | 131,786 | 34 | -0.77% | -0.80% to -0.74% | 1.25% | 87.67% | 1.01% | -3.75% | -0.01% | 0.00% |
| maker | test | soccer | 05 70-85c high_mid | 9,993 | 10 | -0.96% | -1.04% to -0.87% | 1.89% | 84.14% | 1.01% | -0.77% | 0.10% | 0.00% |
| maker | test | basketball_wnba | 06 85-95c favorite | 8,928 | 8 | -0.75% | -1.13% to -0.63% | 2.68% | 88.31% | 1.21% | -1.61% | -0.06% | 0.00% |
| maker | test | basketball_nba | 05 70-85c high_mid | 3,202 | 9 | -1.21% | -1.39% to -1.13% | 0.72% | 80.76% | 1.00% | -1.04% | 0.03% | 0.00% |
| taker | test | soccer | 06 85-95c favorite | 131,786 | 34 | -1.88% | -1.92% to -1.84% | 0.08% | 87.67% | 1.01% | -3.75% | -0.01% | 0.00% |
| maker | test | basketball_wnba | 05 70-85c high_mid | 23,953 | 23 | -1.63% | -2.04% to -1.38% | 1.77% | 76.47% | 1.80% | -1.56% | -0.16% | 0.00% |
| taker | test | soccer | 05 70-85c high_mid | 9,993 | 10 | -2.11% | -2.21% to -2.02% | 0.25% | 84.14% | 1.01% | -0.77% | 0.10% | 0.00% |
| taker | test | basketball_nba | 05 70-85c high_mid | 3,202 | 9 | -2.41% | -2.61% to -2.31% | 0.09% | 80.76% | 1.00% | -1.04% | 0.03% | 0.00% |
| maker | test | basketball_wnba | 04 30-70c mid | 98,353 | 42 | -2.76% | -2.86% to -2.60% | 2.02% | 50.12% | 4.41% | -2.20% | -0.01% | 0.00% |
| taker | test | basketball_wnba | 06 85-95c favorite | 8,928 | 8 | -2.06% | -2.96% to -1.97% | 0.19% | 88.31% | 1.21% | -1.61% | -0.06% | 0.00% |
| maker | test | basketball_nba | 04 30-70c mid | 9,528 | 17 | -2.93% | -2.99% to -2.83% | 0.84% | 50.00% | 1.00% | -0.50% | 0.00% | 0.00% |
| maker | test | icehockey_nhl | 04 30-70c mid | 291,142 | 48 | -2.97% | -3.00% to -2.94% | 0.18% | 50.00% | 1.02% | -5.31% | 0.00% | 0.00% |
| maker | test | baseball_mlb | 04 30-70c mid | 23,248 | 5 | -3.04% | -3.04% to -2.90% | 2.49% | 50.00% | 3.44% | n/a | n/a | 0.00% |
| taker | test | basketball_wnba | 05 70-85c high_mid | 23,953 | 23 | -3.89% | -4.74% to -3.23% | 0.19% | 76.47% | 1.80% | -1.56% | -0.16% | 0.00% |
| maker | test | basketball_wnba | 03 15-30c low_mid | 24,532 | 23 | -4.63% | -4.87% to -4.41% | 2.18% | 23.68% | 1.84% | -0.28% | 0.18% | 0.00% |
| taker | test | basketball_nba | 04 30-70c mid | 9,528 | 17 | -4.85% | -4.91% to -4.75% | 0.37% | 50.00% | 1.00% | -0.50% | 0.00% | 0.00% |
| maker | test | basketball_nba | 03 15-30c low_mid | 3,202 | 9 | -4.72% | -4.94% to -4.38% | 1.37% | 19.24% | 1.00% | 0.04% | -0.03% | 0.00% |
| taker | test | icehockey_nhl | 04 30-70c mid | 291,142 | 48 | -4.93% | -4.97% to -4.89% | 0.06% | 50.00% | 1.02% | -5.31% | 0.00% | 0.00% |
| maker | test | soccer | 02 5-15c longshot | 131,773 | 34 | -5.26% | -5.33% to -5.18% | 1.15% | 12.33% | 1.01% | 2.74% | 0.01% | 0.00% |
| maker | test | basketball_wnba | 02 5-15c longshot | 8,928 | 8 | -5.24% | -5.60% to -3.40% | 2.63% | 11.69% | 1.21% | 0.40% | 0.06% | 0.00% |

## Horizon x Spread Buckets

| Side | split | horizon_sec | spread_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 60 | 04 >10c | 1,413 | 8 | -1.51% | -2.31% to 0.76% | 15.15% | 49.98% | 49.60% | -27.39% | -0.01% | 0.00% |
| maker | test | 60 | 01 1-3c | 134,931 | 177 | -2.14% | -2.32% to -1.93% | 0.50% | 54.25% | 1.08% | -2.94% | 0.00% | 0.00% |
| maker | test | 300 | 01 1-3c | 133,479 | 176 | -2.14% | -2.33% to -1.92% | 1.19% | 54.27% | 1.08% | -2.95% | 0.00% | 0.00% |
| maker | test | 900 | 01 1-3c | 130,906 | 145 | -2.14% | -2.33% to -1.95% | 2.36% | 54.30% | 1.08% | -2.96% | 0.00% | 0.00% |
| maker | test | 30 | 01 1-3c | 135,257 | 176 | -2.14% | -2.33% to -1.94% | 0.31% | 54.25% | 1.08% | -2.94% | 0.00% | 0.00% |
| maker | test | 120 | 01 1-3c | 134,560 | 177 | -2.14% | -2.34% to -1.96% | 0.77% | 54.25% | 1.08% | -2.94% | 0.00% | 0.00% |
| maker | test | 300 | 04 >10c | 1,472 | 7 | -0.34% | -2.37% to 2.70% | 15.69% | 49.95% | 48.31% | -26.40% | -0.01% | 0.00% |
| maker | test | 120 | 04 >10c | 1,409 | 7 | -1.34% | -2.51% to 0.49% | 14.69% | 49.95% | 48.94% | -26.79% | -0.01% | 0.00% |
| maker | test | 30 | 02 3-5c | 1,937 | 46 | -2.62% | -2.94% to -2.11% | 3.30% | 51.34% | 3.54% | -1.84% | -0.21% | 0.00% |
| maker | test | 60 | 02 3-5c | 1,895 | 42 | -2.77% | -3.26% to -2.15% | 4.17% | 51.34% | 3.54% | -1.82% | -0.16% | 0.00% |
| maker | test | 30 | 04 >10c | 1,766 | 7 | -2.61% | -3.37% to -1.91% | 10.48% | 49.97% | 45.54% | -24.49% | -0.01% | 0.00% |
| maker | test | 120 | 02 3-5c | 1,885 | 43 | -2.83% | -3.45% to -2.02% | 4.56% | 51.35% | 3.54% | -1.80% | -0.15% | 0.00% |
| maker | test | 300 | 02 3-5c | 1,764 | 38 | -2.90% | -3.68% to -1.94% | 5.73% | 51.28% | 3.53% | -1.80% | -0.19% | 0.00% |
| maker | test | 30 | 00 <=1c | 24,836 | 130 | -3.54% | -3.86% to -3.26% | 0.43% | 26.75% | 0.98% | 0.72% | -0.00% | 0.00% |
| maker | test | 60 | 00 <=1c | 24,754 | 130 | -3.56% | -3.89% to -3.30% | 0.62% | 26.70% | 0.98% | 0.74% | -0.00% | 0.00% |
| maker | test | 120 | 00 <=1c | 24,659 | 128 | -3.59% | -3.92% to -3.32% | 0.85% | 26.69% | 0.98% | 0.74% | -0.00% | 0.00% |
| maker | test | 300 | 00 <=1c | 24,536 | 122 | -3.62% | -3.96% to -3.33% | 1.30% | 26.66% | 0.98% | 0.74% | -0.00% | 0.00% |
| maker | test | 900 | 00 <=1c | 24,035 | 108 | -3.70% | -4.10% to -3.38% | 1.97% | 26.47% | 0.98% | 0.75% | -0.01% | 0.00% |
| maker | test | 900 | 02 3-5c | 1,646 | 29 | -3.09% | -4.21% to -1.71% | 9.54% | 51.23% | 3.53% | -1.82% | -0.24% | 0.00% |
| taker | test | 60 | 01 1-3c | 134,931 | 177 | -4.07% | -4.30% to -3.80% | 0.12% | 54.25% | 1.08% | -2.94% | 0.00% | 0.00% |

## Odds Edge Buckets

| Side | split | odds_edge_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | 03 -2c-+2c neutral | 439,087 | 138 | -1.81% | -1.99% to -1.65% | 0.90% | 51.59% | 1.42% | -1.15% | -0.00% | 0.00% |
| maker | test | 00 <=-10c against | 6,876 | 16 | -0.77% | -2.51% to 1.06% | 4.61% | 79.09% | 1.01% | -48.32% | -0.42% | 0.00% |
| maker | test | 01 -10c--5c against | 86,394 | 67 | -2.67% | -2.81% to -2.54% | 0.43% | 55.00% | 1.01% | -7.27% | -0.05% | 0.00% |
| maker | test | 02 -5c--2c against | 186,082 | 116 | -2.99% | -3.04% to -2.90% | 0.26% | 49.50% | 1.04% | -4.86% | -0.00% | 0.00% |
| maker | test | 05 +5c-+10c edge | 4,220 | 51 | -2.49% | -3.20% to -1.95% | 8.48% | 46.24% | 2.45% | 4.00% | 0.99% | 0.00% |
| maker | test | 04 +2c-+5c edge | 51,806 | 107 | -3.47% | -3.95% to -3.00% | 2.59% | 30.55% | 1.42% | 1.23% | 0.04% | 0.00% |
| taker | test | 01 -10c--5c against | 176,257 | 100 | -4.70% | -4.86% to -4.54% | 0.10% | 53.05% | 1.06% | -6.29% | -0.03% | 0.00% |
| taker | test | 02 -5c--2c against | 157,719 | 153 | -4.59% | -5.00% to -4.16% | 0.09% | 53.29% | 1.15% | -3.51% | 0.01% | 0.00% |
| taker | test | 03 -2c-+2c neutral | 418,218 | 127 | -4.80% | -6.18% to -4.03% | 0.11% | 47.67% | 1.44% | -0.40% | 0.01% | 0.00% |
| maker | test | 06 >+10c edge | 8,371 | 18 | -1.11% | -6.31% to 7.13% | 12.03% | 24.69% | 20.73% | 35.00% | 0.57% | 0.00% |
| taker | test | 04 +2c-+5c edge | 11,051 | 68 | -6.69% | -7.73% to -5.86% | 0.71% | 37.90% | 1.29% | 2.96% | 0.34% | 0.00% |
| taker | test | 05 +5c-+10c edge | 1,580 | 32 | -4.60% | -8.24% to -3.36% | 0.19% | 51.87% | 1.13% | 6.48% | 1.15% | 0.00% |
| taker | test | 06 >+10c edge | 5,251 | 11 | -13.01% | -21.03% to -9.08% | 0.30% | 14.03% | 1.01% | 58.62% | 0.49% | 0.00% |
| taker | test | 00 <=-10c against | 12,760 | 24 | -19.45% | -47.17% to -2.56% | 1.11% | 68.71% | 13.94% | -40.40% | -0.41% | 0.00% |
| maker | unobserved | 03 -2c-+2c neutral | 490,319 | 74 | -1.46% | -1.57% to -1.37% | 1.66% | 52.45% | 1.06% | -0.66% | -0.01% | 0.00% |
| maker | train | 00 <=-10c against | 1,926 | 50 | -0.76% | -1.73% to -0.19% | 27.31% | 78.53% | 1.61% | -26.66% | -5.41% | 0.00% |
| maker | unobserved | 02 -5c--2c against | 1,334 | 22 | -1.22% | -1.88% to -0.74% | 0.90% | 80.17% | 1.06% | -3.43% | -0.28% | 0.00% |
| maker | val | 03 -2c-+2c neutral | 200,396 | 105 | -1.71% | -1.93% to -1.57% | 1.15% | 53.47% | 1.10% | -1.06% | 0.01% | 0.00% |
| maker | train | 03 -2c-+2c neutral | 2,294,899 | 734 | -2.35% | -2.42% to -2.29% | 0.60% | 51.29% | 1.19% | -0.77% | -0.01% | 0.00% |
| maker | val | 01 -10c--5c against | 224,204 | 91 | -2.66% | -2.76% to -2.54% | 0.17% | 55.12% | 1.00% | -7.04% | -0.03% | 0.00% |

## Sport x Odds Edge Buckets

| Side | split | sport_family | odds_edge_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| maker | test | soccer | 03 -2c-+2c neutral | 273,872 | 36 | -1.38% | -1.52% to -1.27% | 0.93% | 52.68% | 1.00% | -0.64% | -0.00% | 0.00% |
| taker | test | soccer | 02 -5c--2c against | 21,675 | 34 | -2.15% | -2.55% to -1.88% | 0.04% | 83.98% | 1.03% | -2.22% | -0.06% | 0.00% |
| maker | test | basketball_nba | 03 -2c-+2c neutral | 10,790 | 26 | -2.18% | -2.56% to -1.82% | 1.32% | 53.33% | 1.00% | -0.79% | -0.01% | 0.00% |
| maker | test | basketball_nba | 02 -5c--2c against | 1,782 | 14 | -1.91% | -2.63% to -1.10% | 2.86% | 60.33% | 1.00% | -3.73% | -0.16% | 0.00% |
| maker | test | basketball_wnba | 06 >+10c edge | 3,102 | 14 | 6.44% | -2.65% to 16.25% | 29.88% | 43.13% | 54.24% | -4.79% | 0.89% | 0.00% |
| maker | test | basketball_wnba | 03 -2c-+2c neutral | 123,830 | 52 | -2.45% | -2.71% to -2.17% | 1.02% | 51.11% | 2.48% | -2.04% | -0.02% | 0.00% |
| maker | test | basketball_wnba | 02 -5c--2c against | 8,395 | 37 | -2.23% | -2.72% to -1.83% | 1.64% | 62.52% | 1.38% | -4.44% | -0.43% | 0.00% |
| maker | test | icehockey_nhl | 00 <=-10c against | 1,625 | 5 | -2.54% | -2.77% to -2.21% | 0.37% | 56.88% | 1.00% | -11.77% | -0.22% | 0.00% |
| maker | test | icehockey_nhl | 01 -10c--5c against | 84,814 | 35 | -2.68% | -2.80% to -2.57% | 0.28% | 55.13% | 1.01% | -7.26% | -0.04% | 0.00% |
| maker | test | icehockey_nhl | 02 -5c--2c against | 175,720 | 51 | -3.05% | -3.10% to -3.01% | 0.16% | 48.74% | 1.02% | -4.89% | 0.01% | 0.00% |
| maker | test | basketball_wnba | 05 +5c-+10c edge | 3,409 | 36 | -2.35% | -3.20% to -1.69% | 10.27% | 47.27% | 2.78% | 3.41% | 1.01% | 0.00% |
| maker | test | icehockey_nhl | 03 -2c-+2c neutral | 30,595 | 24 | -3.42% | -3.54% to -3.31% | 0.04% | 43.16% | 1.03% | -2.25% | 0.06% | 0.00% |
| taker | test | soccer | 03 -2c-+2c neutral | 273,872 | 36 | -3.59% | -3.75% to -3.48% | 0.08% | 47.32% | 1.00% | -0.37% | 0.00% | 0.00% |
| maker | test | icehockey_nhl | 04 +2c-+5c edge | 1,665 | 5 | -3.59% | -3.88% to -3.51% | 0.00% | 41.04% | 1.00% | 1.89% | 0.15% | 0.00% |
| maker | test | basketball_wnba | 04 +2c-+5c edge | 25,046 | 51 | -3.12% | -3.89% to -2.60% | 2.77% | 41.96% | 1.85% | 1.12% | -0.01% | 0.00% |
| taker | test | basketball_nba | 02 -5c--2c against | 3,420 | 17 | -3.15% | -4.02% to -2.42% | 0.20% | 65.98% | 1.00% | -2.90% | -0.08% | 0.00% |
| maker | test | basketball_nba | 04 +2c-+5c edge | 3,420 | 17 | -3.68% | -4.34% to -3.25% | 0.61% | 34.02% | 1.00% | 1.90% | 0.08% | 0.00% |
| taker | test | icehockey_nhl | 00 <=-10c against | 4,389 | 6 | -4.33% | -4.46% to -3.99% | 0.00% | 56.13% | 1.00% | -11.15% | -0.15% | 0.00% |
| taker | test | icehockey_nhl | 01 -10c--5c against | 172,038 | 50 | -4.65% | -4.78% to -4.49% | 0.08% | 53.03% | 1.02% | -6.28% | -0.02% | 0.00% |
| maker | test | soccer | 04 +2c-+5c edge | 21,675 | 34 | -4.45% | -4.90% to -4.06% | 2.88% | 16.02% | 1.03% | 1.19% | 0.06% | 0.00% |

## Predeclared Strategy Support

| Split | Strategy | Rows | Markets | Reportable | ROI | Positive | Odds gap | Line-lag gap | Reason |
|---|---|---:|---:|---|---:|---:|---:|---:|---|
| train | favorite_longshot_fade_v2 | 1,377,019 | 761 | yes | -3.29% | 0.12% | -1.49% | -0.01% | reportable |
| train | sharp_consensus_clob_mispricing | 73,710 | 305 | yes | -6.59% | 0.55% | 3.46% | 0.39% | reportable |
| train | line_lag_clv_capture | 25 | 1 | no | -5.62% | 0.00% | 1.61% | 2.20% | rows 25 < 1,000; markets 1 < 5 |
| val | favorite_longshot_fade_v2 | 316,884 | 155 | yes | -3.21% | 0.49% | -4.73% | 0.00% | reportable |
| val | sharp_consensus_clob_mispricing | 7,590 | 30 | yes | -9.77% | 0.53% | 2.59% | 0.17% | reportable |
| val | line_lag_clv_capture | 0 | 0 | no | n/a | n/a | n/a | n/a | no candidate rows; rows 0 < 1,000; markets 0 < 5 |
| test | favorite_longshot_fade_v2 | 301,450 | 158 | yes | -2.76% | 0.34% | -3.55% | -0.01% | reportable |
| test | sharp_consensus_clob_mispricing | 14,992 | 74 | yes | -7.04% | 0.56% | 22.81% | 0.47% | reportable |
| test | line_lag_clv_capture | 12 | 1 | no | -8.48% | 0.00% | 1.48% | 7.59% | rows 12 < 1,000; markets 1 < 5 |
| unobserved | favorite_longshot_fade_v2 | 265,584 | 74 | yes | -2.14% | 0.06% | -1.48% | 0.00% | reportable |
| unobserved | sharp_consensus_clob_mispricing | 1,416 | 29 | yes | -9.19% | 0.35% | 2.71% | 0.88% | reportable |
| unobserved | line_lag_clv_capture | 0 | 0 | no | n/a | n/a | n/a | n/a | no candidate rows; rows 0 < 1,000; markets 0 < 5 |

## Predeclared Strategy Rows

| Side | split | strategy | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| taker | test | favorite_longshot_fade_v2 | 301,450 | 158 | -2.76% | -3.02% to -2.52% | 0.34% | 75.94% | 1.11% | -3.55% | -0.01% | 0.00% |
| taker | test | sharp_consensus_clob_mispricing | 14,992 | 74 | -7.04% | -8.74% to -5.57% | 0.56% | 31.04% | 1.07% | 22.81% | 0.47% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 265,584 | 74 | -2.14% | -2.27% to -2.03% | 0.06% | 84.41% | 1.07% | -1.48% | 0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 1,377,019 | 761 | -3.29% | -3.36% to -3.20% | 0.12% | 71.54% | 1.20% | -1.49% | -0.01% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 316,884 | 155 | -3.21% | -3.44% to -2.99% | 0.49% | 69.39% | 1.06% | -4.73% | 0.00% | 0.00% |
| taker | train | sharp_consensus_clob_mispricing | 73,710 | 305 | -6.59% | -7.10% to -6.14% | 0.55% | 37.48% | 1.24% | 3.46% | 0.39% | 0.00% |
| taker | val | sharp_consensus_clob_mispricing | 7,590 | 30 | -9.77% | -12.44% to -8.19% | 0.53% | 18.23% | 1.04% | 2.59% | 0.17% | 0.00% |
| taker | unobserved | sharp_consensus_clob_mispricing | 1,416 | 29 | -9.19% | -14.09% to -6.94% | 0.35% | 19.97% | 1.08% | 2.71% | 0.88% | 0.00% |

## Predeclared Strategy Buckets

| Side | split | strategy | strategy_bucket | Rows | Markets | ROI | 95% CI | Positive | Avg mid | Avg spread | Odds gap | Line-lag gap | News cov. |
|---|---|---|---|---:|---:|---:|---|---:|---:|---:|---:|---:|---:|
| taker | test | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 131,792 | 34 | -1.88% | -1.92% to -1.84% | 0.08% | 87.67% | 1.01% | -3.74% | -0.01% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 9,752 | 9 | -2.09% | -2.13% to -1.98% | 0.22% | 84.39% | 1.00% | -1.13% | 0.03% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 04 85-95c | basketball_wnba | h2h_or_binary | 01 1-3c | 8,931 | 7 | -2.03% | -2.39% to -1.89% | 0.16% | 88.20% | 1.18% | -1.61% | -0.02% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 03 75-85c | basketball_nba | h2h_or_binary | 01 1-3c | 1,492 | 7 | -2.39% | -2.70% to -2.28% | 0.20% | 80.87% | 1.00% | -0.58% | 0.04% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 02 65-75c | basketball_wnba | h2h_or_binary | 00 <=1c | 1,924 | 9 | -3.08% | -3.50% to -2.56% | 0.57% | 67.89% | 0.73% | -1.50% | 0.06% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 02 65-75c | icehockey_nhl | h2h_or_binary | 01 1-3c | 2,293 | 7 | -3.19% | -3.53% to -2.98% | 0.00% | 70.71% | 1.01% | -5.75% | -0.09% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 03 75-85c | basketball_wnba | h2h_or_binary | 01 1-3c | 11,074 | 12 | -3.23% | -3.61% to -2.81% | 0.23% | 79.73% | 1.63% | -1.07% | -0.04% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 02 65-75c | basketball_wnba | h2h_or_binary | 01 1-3c | 28,373 | 26 | -3.84% | -4.09% to -3.59% | 0.26% | 69.01% | 1.38% | -1.07% | -0.06% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | icehockey_nhl | h2h_or_binary | 01 1-3c | 54,754 | 32 | -4.05% | -4.22% to -3.94% | 0.06% | 59.73% | 1.01% | -6.78% | 0.00% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | icehockey_nhl | h2h_or_binary | 00 <=1c | 9,099 | 12 | -4.33% | -4.37% to -4.27% | 0.04% | 56.50% | 1.00% | -6.31% | -0.03% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | basketball_nba | h2h_or_binary | 01 1-3c | 1,933 | 11 | -4.27% | -4.50% to -3.99% | 0.26% | 58.16% | 1.00% | -0.38% | -0.04% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | basketball_wnba | h2h_or_binary | 00 <=1c | 1,956 | 9 | -3.80% | -4.69% to -2.90% | 0.15% | 58.50% | 0.73% | -0.30% | -0.04% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 01 55-65c | basketball_wnba | h2h_or_binary | 01 1-3c | 16,027 | 24 | -4.34% | -4.71% to -4.04% | 0.27% | 59.48% | 1.16% | -1.30% | -0.02% | 0.00% |
| taker | test | sharp_consensus_clob_mispricing | 02 +4c-+7c | basketball_wnba | h2h_or_binary | books=9 | 1,547 | 21 | -4.85% | -6.90% to -3.08% | 0.97% | 52.41% | 1.28% | 4.94% | 0.73% | 0.00% |
| taker | test | sharp_consensus_clob_mispricing | 01 +2c-+4c | basketball_wnba | h2h_or_binary | books=9 | 4,795 | 28 | -6.41% | -7.34% to -5.42% | 0.83% | 37.13% | 1.10% | 2.95% | 0.33% | 0.00% |
| taker | test | sharp_consensus_clob_mispricing | 01 +2c-+4c | basketball_nba | h2h_or_binary | books=9 | 1,636 | 14 | -5.90% | -7.56% to -5.18% | 0.00% | 38.53% | 1.00% | 2.59% | 0.12% | 0.00% |
| taker | test | favorite_longshot_fade_v2 | 02 65-75c | basketball_wnba | h2h_or_binary | 02 3-5c | 1,808 | 19 | -8.20% | -10.32% to -5.88% | 0.28% | 69.54% | 3.53% | -1.86% | -1.26% | 0.00% |
| taker | test | sharp_consensus_clob_mispricing | 03 >+7c | soccer | h2h_or_binary | books=9 | 5,436 | 7 | -13.33% | -32.03% to -9.78% | 0.22% | 13.57% | 1.00% | 56.90% | 0.47% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 00 <=1c | 4,314 | 6 | -1.46% | -1.50% to -1.42% | 0.05% | 93.50% | 1.00% | -1.43% | 0.06% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 04 85-95c | basketball_nba | h2h_or_binary | 01 1-3c | 5,788 | 14 | -1.68% | -1.85% to -1.53% | 0.00% | 90.33% | 1.01% | -2.66% | -0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | americanfootball_nfl | h2h_or_binary | 01 1-3c | 19,573 | 13 | -1.85% | -1.91% to -1.81% | 0.36% | 88.10% | 1.03% | -1.72% | -0.07% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | basketball_nba | h2h_or_binary | 01 1-3c | 25,134 | 26 | -1.90% | -1.93% to -1.85% | 0.00% | 88.26% | 1.06% | -2.12% | -0.00% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 214,849 | 63 | -1.97% | -2.00% to -1.95% | 0.05% | 87.29% | 1.07% | -1.49% | -0.01% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 116,193 | 72 | -1.97% | -2.05% to -1.89% | 0.04% | 88.24% | 1.13% | -1.52% | -0.03% | 0.00% |
| taker | unobserved | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 18,436 | 23 | -2.10% | -2.16% to -2.07% | 0.17% | 84.45% | 1.03% | -1.12% | 0.06% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 04 85-95c | soccer | h2h_or_binary | 01 1-3c | 70,724 | 16 | -2.06% | -2.16% to -1.97% | 0.10% | 86.78% | 1.11% | -1.76% | -0.00% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 4,891 | 6 | -2.14% | -2.20% to -1.32% | 0.55% | 83.68% | 1.02% | -1.32% | 0.02% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 00 <=1c | 24,289 | 30 | -2.32% | -2.36% to -2.26% | 0.02% | 81.46% | 0.98% | -1.31% | -0.01% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 03 75-85c | basketball_nba | h2h_or_binary | 01 1-3c | 3,371 | 9 | -2.42% | -2.60% to -2.28% | 0.00% | 80.64% | 1.01% | -1.52% | 0.01% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | americanfootball_nfl | h2h_or_binary | 01 1-3c | 26,718 | 24 | -2.63% | -2.73% to -2.50% | 0.47% | 78.41% | 1.08% | -1.73% | -0.05% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | soccer | h2h_or_binary | 01 1-3c | 252,071 | 168 | -2.84% | -2.92% to -2.77% | 0.06% | 78.75% | 1.25% | -1.32% | -0.01% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 03 75-85c | basketball_nba | h2h_or_binary | 01 1-3c | 14,865 | 49 | -2.71% | -2.97% to -2.45% | 0.28% | 79.05% | 1.17% | -1.73% | -0.03% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 02 65-75c | basketball_nba | h2h_or_binary | 01 1-3c | 1,784 | 8 | -3.05% | -3.24% to -2.87% | 0.06% | 71.21% | 1.00% | -0.77% | 0.02% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 02 65-75c | icehockey_nhl | h2h_or_binary | 00 <=1c | 5,344 | 8 | -3.31% | -3.33% to -3.11% | 0.11% | 68.52% | 1.00% | -6.77% | -0.03% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | americanfootball_nfl | h2h_or_binary | 01 1-3c | 59,191 | 30 | -3.23% | -3.36% to -3.12% | 0.19% | 70.95% | 1.08% | -1.15% | -0.01% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | soccer | h2h_or_binary | 00 <=1c | 22,070 | 52 | -3.34% | -3.37% to -3.31% | 0.00% | 68.50% | 1.00% | -1.03% | 0.02% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | americanfootball_nfl | h2h_or_binary | 00 <=1c | 4,554 | 12 | -3.33% | -3.39% to -3.28% | 0.13% | 68.50% | 1.00% | -0.87% | 0.02% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | basketball_nba | h2h_or_binary | 01 1-3c | 27,470 | 71 | -3.29% | -3.40% to -3.18% | 0.37% | 70.27% | 1.09% | -1.39% | -0.00% | 0.00% |
| taker | train | favorite_longshot_fade_v2 | 02 65-75c | basketball_nba | h2h_or_binary | 00 <=1c | 3,047 | 17 | -3.35% | -3.41% to -3.25% | 0.07% | 68.61% | 0.99% | -0.84% | -0.02% | 0.00% |
| taker | val | favorite_longshot_fade_v2 | 02 65-75c | icehockey_nhl | h2h_or_binary | 01 1-3c | 53,312 | 26 | -3.32% | -3.44% to -3.22% | 0.05% | 68.57% | 1.00% | -6.13% | -0.00% | 0.00% |

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
