# Telonex CLOB Execution Labels

- Generated: 2026-05-31T17:14:56.106230+00:00
- Book files read: 2,593
- Book rows scanned: 222,788,999
- Book files with labels: 2,573
- Labels: 5,392,062
- Markets: 1,257
- Tokens: 2,513
- Sports: {'soccer': 3263258, 'icehockey_nhl': 1222278, 'americanfootball_nfl': 415814, 'basketball_nba': 250430, 'basketball_wnba': 191728, 'baseball_mlb': 48554}
- Splits: {'train': 3123944, 'val': 925902, 'test': 810914, 'unobserved': 531302}
- Split strategy: market_disjoint_observed_trade_target_stratified_by_fill_positive
- Horizons: {30: 1151784, 60: 1054811, 120: 1055565, 300: 1058155, 900: 1071747}
- Lag seconds: [30, 60, 300]
- Trade files matched/features rows: 2,429 / 4,622,236
- Trade windows seconds: [60, 300]
- Positive LEV rate: 0.0016943425353788588
- Mean ROI on entry: -0.06299227204977903
- Maker positive rate: 0.009948884118914062
- Maker mean ROI on entry: -0.030133042996785816
- Trade-confirmed maker fill-any/queue rates: 0.2863730053549087 / 0.021631056912921255
- Trade-confirmed maker fill-positive rate: 0.000507041647518148
- Trade-confirmed maker fill-adjusted mean ROI: -0.0011759081084533913
- Binary/complement feature rows: 5,388,976
- Binary/complement feature markets: 1,256
- Start/end filter: asof >= start - 0.0m, future <= end + 10.0m
- Slug-date filter: asof >= slug date - 7.0d, future <= slug date + 1.0d
- Fee rate: 0.03
- Output: `/private/tmp/telonex_clob_execution_labels_partitioned`
- Partition files: 22

## Split Fill Coverage

| Split | Rows | Markets | Tokens | Target observed | Past trade rows | Taker+ | Maker+ | Fill any | Fill queue | Fill+ |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| train | 3,123,944 | 828 | 1,655 | 3,119,178 | 2,976,794 | 3,471 | 24,753 | 961,889 | 80,603 | 1,171 |
| val | 925,902 | 177 | 354 | 925,902 | 890,126 | 3,161 | 8,706 | 372,014 | 21,678 | 1,026 |
| test | 810,914 | 178 | 356 | 808,062 | 755,316 | 2,240 | 9,951 | 210,238 | 14,355 | 537 |
| unobserved | 531,302 | 74 | 148 | 0 | 0 | 264 | 10,235 | 0 | 0 | 0 |

Taker labels enter at historical best ask and exit at the future best bid. Maker labels assume a bid fill at the historical best bid, then exit at the future best bid. Trade-confirmed maker labels require future sell prints at or below the posted bid to consume the current best-bid queue proxy; they are still historical proxies, not authenticated order lifecycle truth.
