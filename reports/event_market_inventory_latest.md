# Event And Market Inventory

- Generated: 2026-05-30T22:23:37.159539+00:00
- Row definition: One row is one token/outcome at one minute timestamp for one forecast horizon, not one game.
- Total events/markets/tokens: 108 / 216 / 429
- Active model events/markets/tokens: 89 / 109 / 217
- Active model label rows: 1,984,815
- Active test market ratio: 18 / 109 = 16.51%
- Excluded unobserved rows: 539,748
- Excluded censored rows inside train/val/test: 364,022
- Time span: 2026-03-02 00:03:00+00:00 to 2026-05-29 23:59:00+00:00
- Complete enough for profitable bot claim: False
- Completeness reasons: active observed markets 109 < 200 research target; test Odds API coverage 32.54% < 50% target; Odds API point-in-time features have insufficient test coverage

## Active Market Types

| Sport | Market type | Markets |
|---|---|---:|
| soccer | moneyline | 40 |
| baseball_mlb | moneyline | 34 |
| baseball_mlb | nrfi | 15 |
| soccer | draw | 6 |
| soccer | total | 5 |
| soccer | spread | 3 |
| baseball_mlb | total | 2 |
| basketball_wnba | moneyline | 2 |
| baseball_mlb | spread | 1 |
| soccer | exact_score | 1 |

## Split Summary

| Split | Rows | Markets | Tokens | Target observed | Past trade rows | Fill+ |
|---|---:|---:|---:|---:|---:|---:|
| test | 226,224 | 18 | 36 | 159,230 | 116,762 | 97 |
| train | 1,776,863 | 75 | 149 | 1,513,571 | 1,177,192 | 2,820 |
| unobserved | 539,748 | 107 | 212 | 0 | 0 | 0 |
| val | 345,750 | 16 | 32 | 312,014 | 230,990 | 208 |

## Per-Event Data

- Median active event rows: 19,886.00
- Median active event minute points: 2,415.00
- Median active event span hours: 137.52
- Median markets per active event: 1.00

## Per-Market Data

- Median active market rows: 20,268.00
- Median active market minute points: 2,550.00
- Median active market span hours: 144.13
- Median active market tokens: 2.00

## Odds Coverage

- Odds rows/markets/tokens: 1,414,160 / 79 / 157
- Overall Odds row coverage: 48.96%

| Split | Coverage | Matched markets | Matched rows |
|---|---:|---:|---:|
| test | 32.54% | 5 | 73,604 |
| train | 52.69% | 44 | 936,300 |
| unobserved | 42.49% | 24 | 229,330 |
| val | 50.59% | 6 | 174,926 |

## Largest Active Events

| Event | Sport | Markets | Minute points | Rows | Fill+ |
|---|---|---:|---:|---:|---:|
| CR Flamengo vs. Coritiba FBC | soccer | 3 | 8,755 | 213,100 | 0 |
| CA Boca Juniors vs. CD Universidad Católica | soccer | 1 | 6,792 | 65,352 | 1 |
| SE Palmeiras vs. Associação Chapecoense de Futebol | soccer | 2 | 6,733 | 74,222 | 0 |
| Switzerland vs. Jordan | soccer | 1 | 5,935 | 57,690 | 0 |
| Texas Rangers vs. Los Angeles Angels | baseball_mlb | 2 | 5,606 | 53,710 | 196 |
| Rosenborg BK vs. FK Bodø/Glimt | soccer | 1 | 4,316 | 28,914 | 0 |
| Brazil vs. Panama | soccer | 1 | 4,183 | 34,332 | 0 |
| Los Angeles Dodgers vs. Toronto Blue Jays | baseball_mlb | 1 | 3,937 | 36,690 | 78 |
| Grêmio FBPA vs. SC Corinthians Paulista | soccer | 1 | 3,911 | 26,678 | 0 |
| Colorado Rockies vs. Arizona Diamondbacks | baseball_mlb | 1 | 3,901 | 35,600 | 128 |
| Clube do Remo vs. São Paulo FC | soccer | 1 | 3,896 | 25,688 | 0 |
| SK Brann vs. Sarpsborg 08 FF | soccer | 1 | 3,879 | 26,674 | 0 |

This inventory separates games/events, Polymarket markets, tokens, minute points, and ML rows. The active model intentionally excludes rows whose maker-fill target is not observable from historical trade data.
