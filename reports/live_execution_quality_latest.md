# Live Execution Quality

- Generated: 2026-05-30T23:29:12.905607+00:00
- Quality gate: False
- Gate reasons: need >=500 alpha paper fills with 3s post-fill books within 5s lag, 3s alpha average LEV is not positive, 3s alpha favorable post-fill move rate is not >52%, wallet-level whale detector unavailable from current trade feed, favorite_longshot_bias has only 13 timely 3s LEV rows after 692 fills
- Paper fills analyzed: 850
- Alpha/probe fills analyzed: 692 / 158
- Paper fills with model version: 210
- Strategy health gate: False
- Quarantined strategies: none
- LEV drift alerts: 0 / max score 0.007296857142857149

## Alpha LEV By Horizon

| Horizon | Rows | Avg LEV/share | Median | P05 | Favorable | Avg lag | P95 lag | Max lag |
|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 3s | 13 | -0.015682615384615375 | -0.0144279999999999 | -0.023609000000000015 | 0.00% | 1.1217640000000002 | 1.121764 | 1.121764 |
| 30s | 3 | -0.01461700000000001 | -0.014617000000000008 | -0.014617000000000008 | 0.00% | 3.2043613333333334 | 4.7737419 | 4.908083 |
| 120s | 59 | -0.02346764338521336 | -0.012457000000000008 | -0.15531299999999998 | 38.98% | 0.7315217288135591 | 3.3586316999999988 | 3.637549 |
| 300s | 23 | -0.009517874957788098 | -0.01382500000000001 | -0.05161700000000004 | 26.09% | 0.4988534347826088 | 3.150141799999998 | 3.286158 |

## Probe LEV By Horizon

| Horizon | Rows | Avg LEV/share | Favorable | Avg lag |
|---:|---:|---:|---:|---:|
| 3s | 156 | -0.01129436538964255 | 2.56% | 0.7093661217948719 |
| 30s | 0 | None | n/a | None |
| 120s | 0 | None | n/a | None |
| 300s | 5 | 0.0764522 | 40.00% | 2.0927555999999994 |

## Price Hold/Revert

- Rows with 3s and 120s follow-up: 0
- Hold rate 3s to 120s: n/a
- Revert rate 3s to 120s: n/a

## LEV By Strategy

| Strategy | Model | Side | Fills | 3s rows | 3s avg LEV | 3s favorable | 120s rows | 120s avg LEV | 120s favorable |
|---|---|---|---:|---:|---:|---:|---:|---:|---:|
| favorite_longshot_bias | None | buy | 640 | 0 | None | n/a | 59 | -0.02346764338521336 | 38.98% |
| data_collection_probe | data-collection-probe-v1 | buy | 158 | 156 | -0.01129436538964255 | 2.56% | 0 | None | n/a |
| favorite_longshot_bias | favorite_longshot_bias:rules-v1 | buy | 52 | 13 | -0.015682615384615375 | 0.00% | 0 | None | n/a |

## Strategy Health

| Strategy | Fills | 3s rows | 3s avg LEV | 3s favorable | Quarantined |
|---|---:|---:|---:|---:|---:|
| favorite_longshot_bias | 692 | 13 | -0.015682615384615375 | 0.00% | False |

## LEV Drift

- Rows: 13
- Alerts: 0
- Latest mean / latest 50 mean: -0.015682615384615375 / -0.015682615384615375
- Max score / latest score: 0.007296857142857149 / 0.004593543020867838

## Large Trade Flow

- Trades / large trades: 1314 / 59
- Large threshold USD: 250.0
- Wallet identity available: False
- Wallet identity note: market-channel last_trade_price payload lacks wallet identifiers; whale scoring needs on-chain fill decode or authenticated/user trade source

| Horizon | Rows | Avg signed move | Favorable | Avg notional |
|---:|---:|---:|---:|---:|
| 30s | 0 | None | n/a | None |
| 120s | 17 | 0.0014705882352941222 | 35.29% | 1372.1087350111763 |
| 300s | 3 | -0.05833333333333331 | 66.67% | 958.1365666666666 |

This report measures whether paper executions are followed by favorable CLOB movement. It is still not authenticated fill proof; the gate remains blocked until real order lifecycle/fill data is available.
