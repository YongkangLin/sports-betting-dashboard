# Telonex CLOB Execution Labels

- Generated: 2026-05-30T21:46:52.045837+00:00
- Book files read: 1,745
- Book rows scanned: 34,575,311
- Book files with labels: 1,440
- Labels: 2,888,585
- Markets: 216
- Tokens: 429
- Sports: {'baseball_mlb': 1731351, 'soccer': 1108317, 'basketball_wnba': 43570, 'icehockey_nhl': 5347}
- Splits: {'train': 1776863, 'unobserved': 539748, 'val': 345750, 'test': 226224}
- Split strategy: market_disjoint_observed_trade_target_stratified_by_fill_positive
- Horizons: {30: 587727, 60: 581790, 120: 575400, 300: 579188, 900: 564480}
- Lag seconds: [30, 60, 300]
- Trade files matched/features rows: 944 / 1,524,944
- Trade windows seconds: [60, 300]
- Positive LEV rate: 0.0038309414471099173
- Mean ROI on entry: -0.16852317793555677
- Maker positive rate: 0.035664867054284365
- Maker mean ROI on entry: -0.030099886372275203
- Trade-confirmed maker fill-any/queue rates: 0.06383402254044801 / 0.007950259383054332
- Trade-confirmed maker fill-positive rate: 0.0010818445709577526
- Trade-confirmed maker fill-adjusted mean ROI: -0.000742474793472224
- Binary/complement feature rows: 2,879,908
- Binary/complement feature markets: 213
- Start/end filter: asof >= start - 0.0m, future <= end + 10.0m
- Slug-date filter: asof >= slug date - 7.0d, future <= slug date + 1.0d
- Fee rate: 0.03
- Output: `/Users/yongkanglin/Documents/Codex/2026-05-28/i-have-this-repo-git-github-3/Sports-Betting-ml/data/processed/execution_training/telonex_clob_execution_labels_partitioned`
- Partition files: 12

## Split Fill Coverage

| Split | Rows | Markets | Tokens | Target observed | Past trade rows | Taker+ | Maker+ | Fill any | Fill queue | Fill+ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| train | 1,776,863 | 75 | 149 | 1,513,571 | 1,177,192 | 9,036 | 68,137 | 151,169 | 19,156 | 2,820 |
| val | 345,750 | 16 | 32 | 312,014 | 230,990 | 934 | 7,298 | 23,146 | 2,716 | 208 |
| test | 226,224 | 18 | 36 | 159,230 | 116,762 | 538 | 6,798 | 10,075 | 1,093 | 97 |
| unobserved | 539,748 | 107 | 212 | 0 | 0 | 558 | 20,788 | 0 | 0 | 0 |

Taker labels enter at historical best ask and exit at the future best bid. Maker labels assume a bid fill at the historical best bid, then exit at the future best bid. Trade-confirmed maker labels require future sell prints at or below the posted bid to consume the current best-bid queue proxy; they are still historical proxies, not authenticated order lifecycle truth.
