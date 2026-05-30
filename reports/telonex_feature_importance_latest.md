# Telonex Feature Importance Audit

- Generated: 2026-05-30T16:52:46.374598+00:00
- Run: `20260530T163238Z`
- Model version: `20260530T163238Z-4c3569fa30ce`
- Rows audited: 10,000
- Repeats per feature: 10
- FDR alpha / min economic prob shift / min ROI delta: 0.1 / 0.015 / 0.005
- Confirmed features: 15 / 82
- Baseline Brier/ECE/log loss: 0.03203438132608235 / 0.007425116469169704 / 0.11413523329028553
- Baseline selected trades/ROI: 100 / 0.09661918976545841

Positive Brier delta means shuffling the feature made the model worse. A confirmed feature must also pass BH FDR and an economic-size filter, so noisy tiny effects do not get treated as edge.

## Feature Families

```text
             family  features  confirmed_features  fdr_significant_features  economically_significant_features  positive_brier_features  total_positive_brier_delta  max_brier_delta  mean_abs_prob_shift  max_abs_prob_shift  mean_selected_trade_delta  max_abs_roi_delta
        price_level         5                   3                         4                                  3                        4                    0.011707         0.004351             0.019199            0.033838                  -8.780000           0.040232
         book_depth        17                   2                        10                                  4                       11                    0.003475         0.001629             0.001936            0.010226                   1.017647           0.015485
     price_momentum        12                   9                        10                                 10                       10                    0.002882         0.000844             0.004371            0.008941                  -9.866667           0.053828
categorical_context         2                   1                         2                                  1                        2                    0.000200         0.000184             0.001854            0.003648                  -0.650000           0.005810
               odds        18                   0                         4                                  0                        6                    0.000087         0.000039             0.000393            0.002790                  -0.305556           0.001368
        market_pair         1                   0                         0                                  1                        1                    0.000076         0.000076             0.007876            0.007876                   8.700000           0.017572
              other         1                   0                         0                                  0                        1                    0.000010         0.000010             0.001516            0.001516                   2.100000           0.001821
         trade_flow        26                   0                         0                                  0                        0                    0.000000         0.000000             0.000000            0.000000                   0.000000           0.000000
```

## Top Features

```text
                   feature  repeats  mean_brier_delta  std_brier_delta  brier_delta_positive_pvalue  mean_abs_prob_shift  mean_selected_trade_delta  mean_selected_roi_delta  economically_significant  brier_delta_fdr_qvalue  fdr_significant  confirmed_feature
               horizon_sec       10          0.004351         0.000356                2.309452e-295             0.026466                        5.3                -0.040232                      True           1.893751e-293             True               True
              entry_spread       10          0.003649         0.000346                3.303104e-220             0.033838                      -38.6                -0.001567                      True           6.771363e-219             True               True
                 entry_bid       10          0.003139         0.000456                 4.024834e-95             0.029147                      -12.1                -0.038819                      True            5.500607e-94             True               True
             bid_size_best       10          0.001629         0.000142                2.563247e-261             0.010226                       12.5                -0.015485                      True           1.050931e-259             True               True
              bid_depth_1c       10          0.000970         0.000119                1.917005e-133             0.005692                        4.8                -0.002274                     False           3.143888e-132             True              False
         spread_delta_300s       10          0.000844         0.000157                 5.397850e-59             0.008941                      -35.4                 0.022026                      True            4.918041e-58             True               True
        mid_abs_delta_300s       10          0.000726         0.000129                 8.307635e-64             0.008699                      -21.7                -0.009361                      True            8.515325e-63             True               True
                 entry_ask       10          0.000567         0.000054                7.136341e-221             0.002948                        4.4                -0.001366                     False           1.950600e-219             True              False
             ask_size_best       10          0.000400         0.000065                 3.003072e-76             0.003168                        5.0                -0.004003                     False            3.517884e-75             True              False
         lag_quote_age_60s       10          0.000283         0.000084                 2.527889e-24             0.004216                       -1.7                -0.009512                      True            1.480621e-23             True               True
        lag_quote_age_300s       10          0.000213         0.000133                 7.034576e-07             0.006125                       -0.3                -0.013162                      True            2.884176e-06             True               True
            mid_delta_300s       10          0.000201         0.000070                 2.100405e-18             0.004719                        4.8                 0.007791                      True            1.148221e-17             True               True
          spread_delta_30s       10          0.000195         0.000086                 6.576082e-12             0.003660                      -17.1                 0.020531                      True            3.171993e-11             True               True
         lag_quote_age_30s       10          0.000186         0.000049                 1.466112e-30             0.002588                        0.2                -0.001865                     False            9.247781e-30             True              False
              outcome_role       10          0.000184         0.000044                 1.518941e-36             0.003648                       -1.3                 0.005810                      True            1.132301e-35             True               True
          obi_3c_delta_30s       10          0.000175         0.000045                 3.976737e-32             0.001719                       -3.0                -0.006653                      True            2.717437e-31             True               True
              ask_depth_3c       10          0.000127         0.000029                 7.644849e-39             0.000940                        4.6                -0.004681                     False            6.268776e-38             True              False
          spread_delta_60s       10          0.000111         0.000042                 7.331248e-16             0.004229                      -25.6                 0.053828                      True            3.757265e-15             True               True
              ask_depth_1c       10          0.000094         0.000082                 3.065837e-04             0.002316                        0.6                 0.001717                     False            1.047494e-03             True              False
         mid_abs_delta_60s       10          0.000091         0.000065                 1.288939e-05             0.004832                      -14.6                 0.041612                      True            4.595347e-05             True               True
               market_type       10          0.000076         0.000145                 5.645355e-02             0.007876                        8.7                -0.017572                      True            1.493287e-01            False              False
         odds_poly_gap_bid       10          0.000039         0.000095                 1.091789e-01             0.002790                       -3.5                -0.000724                     False            2.797710e-01            False              False
         mid_abs_delta_30s       10          0.000033         0.000022                 5.636032e-06             0.001582                       -8.3                 0.009292                      True            2.100703e-05             True               True
         obi_3c_delta_300s       10          0.000031         0.000020                 2.372667e-06             0.000434                       -0.4                -0.001347                     False            9.264698e-06             True              False
depth_imbalance_delta_300s       10          0.000018         0.000018                 1.155668e-03             0.000256                        0.2                -0.000185                     False            3.509808e-03             True              False
        ask_depth_5_levels       10          0.000018         0.000019                 2.832173e-03             0.000690                        1.3                -0.000543                     False            8.294220e-03             True              False
            odds_fair_mean       10          0.000017         0.000008                 2.253309e-11             0.000077                        0.6                -0.000806                     False            1.026508e-10             True              False
              sport_family       10          0.000016         0.000008                 7.089460e-11             0.000060                        0.0                 0.000000                     False            3.059662e-10             True              False
           odds_book_count       10          0.000012         0.000033                 1.304363e-01             0.000458                       -0.4                 0.001368                     False            3.241146e-01            False              False
             quote_age_sec       10          0.000010         0.000037                 1.992745e-01             0.001516                        2.1                -0.001821                     False            4.806031e-01            False              False
```
