# Telonex CLOB Execution Labels

- Generated: 2026-05-31T14:29:28.375106+00:00
- Book files read: 2,692
- Book rows scanned: 105,207,694
- Book files with labels: 2,367
- Labels: 5,418,878
- Markets: 632
- Tokens: 1,261
- Sports: {'soccer': 2625089, 'baseball_mlb': 1731351, 'basketball_nba': 900769, 'americanfootball_nfl': 66302, 'basketball_wnba': 55474, 'tennis': 26200, 'icehockey_nhl': 13693}
- Splits: {'train': 2060552, 'unobserved': 1546280, 'val': 959378, 'test': 852668}
- Split strategy: market_disjoint_observed_trade_target_stratified_by_fill_positive
- Horizons: {30: 1101514, 60: 1089637, 120: 1082302, 300: 1083306, 900: 1062119}
- Lag seconds: [30, 60, 300]
- Trade files matched/features rows: 1,444 / 2,942,966
- Trade windows seconds: [60, 300]
- Positive LEV rate: 0.0026457506517031755
- Mean ROI on entry: -0.12448851758803799
- Maker positive rate: 0.02742357366229688
- Maker mean ROI on entry: -0.029853399742837464
- Trade-confirmed maker fill-any/queue rates: 0.132539983369251 / 0.008560259153278594
- Trade-confirmed maker fill-positive rate: 0.0006281743194808963
- Trade-confirmed maker fill-adjusted mean ROI: -0.0006685706175986763
- Binary/complement feature rows: 5,408,446
- Binary/complement feature markets: 629
- Start/end filter: asof >= start - 0.0m, future <= end + 10.0m
- Slug-date filter: asof >= slug date - 7.0d, future <= slug date + 1.0d
- Fee rate: 0.03
- Output: `/Users/yongkanglin/Documents/Codex/2026-05-30/can-you-check-why-the-dashboard/Sports-Betting/data/processed/execution_training/telonex_clob_execution_labels_partitioned`
- Partition files: 22

## Split Fill Coverage

| Split | Rows | Markets | Tokens | Target observed | Past trade rows | Taker+ | Maker+ | Fill any | Fill queue | Fill+ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| train | 2,060,552 | 220 | 439 | 1,948,779 | 1,749,456 | 6,751 | 65,912 | 594,490 | 33,418 | 2,009 |
| val | 959,378 | 47 | 94 | 823,070 | 648,626 | 3,573 | 21,848 | 80,140 | 8,566 | 1,084 |
| test | 852,668 | 48 | 96 | 730,124 | 544,884 | 1,509 | 18,488 | 43,588 | 4,403 | 311 |
| unobserved | 1,546,280 | 317 | 632 | 0 | 0 | 2,504 | 42,357 | 0 | 0 | 0 |

Taker labels enter at historical best ask and exit at the future best bid. Maker labels assume a bid fill at the historical best bid, then exit at the future best bid. Trade-confirmed maker labels require future sell prints at or below the posted bid to consume the current best-bid queue proxy; they are still historical proxies, not authenticated order lifecycle truth.
