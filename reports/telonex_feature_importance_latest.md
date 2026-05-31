# Telonex Feature Importance Audit

- Generated: 2026-05-31T16:05:51.111984+00:00
- Run: `20260531T153530Z`
- Model version: `20260531T153530Z-aeeeb0172cb0`
- Rows audited: 200,000
- Repeats per feature: 5
- FDR alpha / min economic prob shift / min ROI delta: 0.1 / 0.015 / 0.005
- Confirmed features: 0 / 83
- Baseline Brier/ECE/log loss: 0.0004334839229684664 / 5.278201467340086e-05 / 0.0018058785251927208
- Baseline selected trades/ROI: 0 / None

Positive Brier delta means shuffling the feature made the model worse. A confirmed feature must also pass BH FDR and an economic-size filter, so noisy tiny effects do not get treated as edge.

## Feature Families

```text
             family  features  confirmed_features  fdr_significant_features  economically_significant_features  positive_brier_features  total_positive_brier_delta  max_brier_delta  mean_abs_prob_shift  max_abs_prob_shift  mean_selected_trade_delta  max_abs_roi_delta
         book_depth        17                   0                         6                                  0                        7                    0.000075         0.000072             0.000060            0.000674                        0.0                0.0
         trade_flow        26                   0                        16                                  0                       18                    0.000060         0.000028             0.000048            0.000320                        0.0                0.0
        price_level         5                   0                         4                                  0                        4                    0.000056         0.000054             0.000096            0.000450                        0.0                0.0
               odds        19                   0                         8                                  0                       12                    0.000049         0.000015             0.000040            0.000257                        0.0                0.0
categorical_context         2                   0                         1                                  0                        2                    0.000004         0.000004             0.000018            0.000020                        0.0                0.0
        market_pair         1                   0                         1                                  0                        1                    0.000003         0.000003             0.000041            0.000041                        0.0                0.0
     price_momentum        12                   0                         5                                  0                        5                    0.000003         0.000002             0.000018            0.000115                        0.0                0.0
              other         1                   0                         1                                  0                        1                    0.000003         0.000003             0.000077            0.000077                        0.0                0.0
```

## Top Features

```text
                        feature  repeats  mean_brier_delta  std_brier_delta  brier_delta_positive_pvalue  mean_abs_prob_shift  mean_selected_trade_delta mean_selected_roi_delta  economically_significant  brier_delta_fdr_qvalue  fdr_significant  confirmed_feature
                  bid_size_best        5      7.179615e-05     5.491024e-06                4.880343e-151             0.000674                        0.0                    None                     False           4.500761e-150             True              False
                    horizon_sec        5      5.399542e-05     4.259753e-06                4.332829e-142             0.000450                        0.0                    None                     False           3.596248e-141             True              False
               trade_count_300s        5      2.805067e-05     7.638507e-07                 0.000000e+00             0.000320                        0.0                    None                     False            0.000000e+00             True              False
odds_source_minutes_to_commence        5      1.479612e-05     1.325738e-06                1.146554e-110             0.000257                        0.0                    None                     False           8.651275e-110             True              False
             last_trade_age_sec        5      9.955757e-06     3.455263e-06                 4.139889e-09             0.000198                        0.0                    None                     False            1.431712e-08             True              False
             odds_quote_age_sec        5      9.619571e-06     3.567754e-06                 3.474058e-08             0.000114                        0.0                    None                     False            1.153387e-07             True              False
              odds_poly_gap_mid        5      7.787435e-06     3.624822e-07                 0.000000e+00             0.000045                        0.0                    None                     False            0.000000e+00             True              False
                     odds_sport        5      6.249599e-06     4.019690e-06                 9.370421e-04             0.000108                        0.0                    None                     False            2.430453e-03             True              False
            trade_notional_300s        5      5.301153e-06     4.962633e-07                1.436389e-101             0.000110                        0.0                    None                     False           9.935026e-101             True              False
                trade_size_300s        5      5.074220e-06     7.068981e-07                 4.864397e-47             0.000146                        0.0                    None                     False            2.523406e-46             True              False
                   sport_family        5      3.915649e-06     5.564575e-07                 2.763653e-45             0.000020                        0.0                    None                     False            1.349313e-44             True              False
              odds_poly_gap_bid        5      3.732996e-06     1.704069e-07                 0.000000e+00             0.000020                        0.0                    None                     False            0.000000e+00             True              False
                    market_type        5      3.358614e-06     3.234585e-06                 1.891513e-02             0.000041                        0.0                    None                     False            4.025528e-02             True              False
              odds_poly_gap_ask        5      3.308624e-06     5.529214e-07                 2.620235e-33             0.000034                        0.0                    None                     False            1.208219e-32             True              False
                  quote_age_sec        5      2.939259e-06     1.964194e-06                 1.381973e-03             0.000077                        0.0                    None                     False            3.475871e-03             True              False
             mid_abs_delta_300s        5      2.490057e-06     6.097885e-07                 1.581365e-16             0.000115                        0.0                    None                     False            6.562666e-16             True              False
           trade_buy_ratio_300s        5      2.404112e-06     4.954802e-07                 1.447140e-22             0.000026                        0.0                    None                     False            6.321717e-22             True              False
                  odds_fair_std        5      1.798625e-06     7.169852e-07                 2.621645e-07             0.000027                        0.0                    None                     False            8.369098e-07             True              False
           trade_buy_count_300s        5      1.755288e-06     1.645072e-07                2.417328e-101             0.000056                        0.0                    None                     False           1.543371e-100             True              False
                trade_count_60s        5      1.688256e-06     2.742349e-08                 0.000000e+00             0.000010                        0.0                    None                     False            0.000000e+00             True              False
           trade_sell_size_300s        5      1.288182e-06     7.264860e-07                 1.953136e-04             0.000068                        0.0                    None                     False            5.403676e-04             True              False
         trade_signed_size_300s        5      1.255027e-06     1.162520e-08                 0.000000e+00             0.000005                        0.0                    None                     False            0.000000e+00             True              False
     depth_imbalance_delta_300s        5      1.034670e-06     2.742609e-07                 2.258844e-14             0.000016                        0.0                    None                     False            8.522001e-14             True              False
                   entry_spread        5      8.984152e-07     8.104129e-07                 1.330544e-02             0.000013                        0.0                    None                     False            2.906187e-02             True              False
                last_trade_size        5      7.764494e-07     8.215978e-07                 2.937255e-02             0.000018                        0.0                    None                     False            6.094805e-02             True              False
             ask_depth_5_levels        5      7.414629e-07     2.074333e-06                 2.373377e-01             0.000020                        0.0                    None                     False            4.191282e-01            False              False
                   obi_5_levels        5      7.380069e-07     3.439186e-07                 8.863397e-06             0.000015                        0.0                    None                     False            2.627364e-05             True              False
                      entry_bid        5      6.964516e-07     5.540550e-07                 5.968251e-03             0.000013                        0.0                    None                     False            1.376013e-02             True              False
                         obi_3c        5      6.709178e-07     5.448437e-07                 6.893028e-03             0.000029                        0.0                    None                     False            1.546274e-02             True              False
             trade_notional_60s        5      6.674381e-07     1.807033e-07                 7.502369e-14             0.000020                        0.0                    None                     False            2.707377e-13             True              False
```
