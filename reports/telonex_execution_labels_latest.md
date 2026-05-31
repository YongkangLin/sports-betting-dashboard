# Telonex CLOB Execution Labels

- Generated: 2026-05-31T15:13:22.118724+00:00
- Book files read: 2,876
- Book rows scanned: 120,195,069
- Book files with labels: 2,542
- Labels: 5,768,529
- Markets: 725
- Tokens: 1,436
- Sports: {'soccer': 2625089, 'baseball_mlb': 1755107, 'basketball_nba': 908403, 'americanfootball_nfl': 384029, 'basketball_wnba': 56008, 'tennis': 26200, 'icehockey_nhl': 13693}
- Splits: {'train': 2195358, 'unobserved': 1510528, 'test': 1265120, 'val': 797523}
- Split strategy: market_disjoint_observed_trade_target_stratified_by_fill_positive
- Horizons: {30: 1174195, 60: 1158704, 120: 1151456, 300: 1152704, 900: 1131470}
- Lag seconds: [30, 60, 300]
- Trade files matched/features rows: 1,630 / 3,323,020
- Trade windows seconds: [60, 300]
- Positive LEV rate: 0.0032564627827995664
- Mean ROI on entry: -0.1204666896119908
- Maker positive rate: 0.02711765859199113
- Maker mean ROI on entry: -0.029884055343861727
- Trade-confirmed maker fill-any/queue rates: 0.155150125794635 / 0.010005497068663433
- Trade-confirmed maker fill-positive rate: 0.0008090450789100653
- Trade-confirmed maker fill-adjusted mean ROI: -0.0007892007373308501
- Binary/complement feature rows: 5,750,836
- Binary/complement feature markets: 711
- Start/end filter: asof >= start - 0.0m, future <= end + 10.0m
- Slug-date filter: asof >= slug date - 7.0d, future <= slug date + 1.0d
- Fee rate: 0.03
- Output: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/execution_training/telonex_clob_execution_labels_partitioned`
- Partition files: 24

## Split Fill Coverage

| Split | Rows | Markets | Tokens | Target observed | Past trade rows | Taker+ | Maker+ | Fill any | Fill queue | Fill+ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| train | 2,195,358 | 287 | 567 | 2,090,788 | 1,904,142 | 9,064 | 65,870 | 725,080 | 40,554 | 2,794 |
| val | 797,523 | 62 | 123 | 704,029 | 588,788 | 4,068 | 21,876 | 107,538 | 10,888 | 1,299 |
| test | 1,265,120 | 62 | 123 | 1,091,540 | 830,090 | 2,486 | 25,620 | 62,370 | 6,275 | 574 |
| unobserved | 1,510,528 | 314 | 623 | 0 | 0 | 3,167 | 43,063 | 0 | 0 | 0 |

Taker labels enter at historical best ask and exit at the future best bid. Maker labels assume a bid fill at the historical best bid, then exit at the future best bid. Trade-confirmed maker labels require future sell prints at or below the posted bid to consume the current best-bid queue proxy; they are still historical proxies, not authenticated order lifecycle truth.
