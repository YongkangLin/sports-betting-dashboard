# Model Data Audit - 20260529T204400Z

## Verdict

Brazil is not modeled as a sport. `brazil` is an internal dataset key for the Odds API league `soccer_brazil_campeonato`; reports should show the human label **Brazil Serie A**.

## Model Dataset

- Raw rows loaded by trainer: 171,460.
- Clean model rows: 94,098.
- Dropped rows during model cleaning: 77,362.
- Legacy spread rows quarantined: 28,008.
- Inconsistent outcome rows quarantined: 204 from 102 groups.
- Event identity collision rows quarantined: 608 from 11 event ids.
- Clean events: 5,041.
- Clean internal observation keys: 22.
- Date span: 2025-06-07T13:20:00+00:00 to 2026-05-29T02:10:00+00:00.

## Quality Flags

- `info` / `coverage`: data/processed/poly_wh_obs_ahl.parquet is empty and contributes no model rows.
- `info` / `label_mapping`: Internal alias for soccer_brazil_campeonato, rendered as Brazil Serie A.
- `info` / `label_mapping`: Internal alias for soccer_epl, rendered as English Premier League.
- `info` / `coverage`: data/processed/poly_wh_obs_j_league.parquet is empty and contributes no model rows.
- `info` / `label_mapping`: Internal alias for soccer_spain_la_liga, rendered as Spanish La Liga.
- `info` / `label_mapping`: Internal alias for soccer_conmebol_copa_libertadores, rendered as Copa Libertadores.
- `info` / `label_mapping`: Internal alias for soccer_france_ligue_one, rendered as French Ligue 1.
- `info` / `label_mapping`: Internal alias for soccer_uefa_champs_league, rendered as UEFA Champions League.
- `info` / `coverage`: data/processed/poly_wh_obs_world_cup.parquet is empty and contributes no model rows.
- `warning` / `cleaning`: Cleaning dropped 77,362 of 171,460 rows.
- `warning` / `spreads`: 28,008 legacy spread rows were quarantined because they lack stable Polymarket market/condition identifiers.
- `warning` / `outcomes`: 204 rows were quarantined from 102 groups whose winner counts were not exactly one.
- `warning` / `coverage`: 8 sport/market segments are thin (<50 total events or <20 test events).

## Clean Segments Fed To Model

| Sport / league | Internal key | Market | Rows | Events | Test events | Dates | Win rate | All-row ROI | Avg edge |
| --- | --- | --- | ---: | ---: | ---: | --- | ---: | ---: | ---: |
| NHL | `nhl` | Moneyline | 15,630 | 1,384 | 50 | 2025-10-07 to 2026-05-28 | 50.00% | 0.65% | 0.00% |
| NBA | `nba` | Moneyline | 14,210 | 1,268 | 55 | 2025-10-21 to 2026-05-29 | 50.00% | 0.63% | -0.00% |
| NBA | `nba_total` | Total | 11,984 | 958 | 54 | 2025-12-06 to 2026-05-27 | 50.00% | -0.26% | -0.02% |
| MLB | `mlb` | Moneyline | 9,742 | 841 | 443 | 2025-10-01 to 2026-05-28 | 50.00% | 1.14% | 0.00% |
| NHL | `nhl_total` | Total | 9,474 | 782 | 50 | 2025-12-27 to 2026-05-28 | 50.00% | -2.40% | -0.00% |
| MLB | `mlb_total` | Total | 7,466 | 792 | 429 | 2026-03-26 to 2026-05-28 | 50.00% | 0.67% | -0.02% |
| English Premier League | `epl` | 3-way moneyline | 3,981 | 224 | 41 | 2025-11-29 to 2026-05-24 | 33.48% | 3.91% | -0.12% |
| Italian Serie A | `serie_a` | 3-way moneyline | 3,941 | 223 | 46 | 2025-11-29 to 2026-05-24 | 33.34% | -0.24% | 0.00% |
| Spanish La Liga | `la_liga` | 3-way moneyline | 3,396 | 191 | 50 | 2025-11-29 to 2026-05-24 | 33.33% | 2.06% | -0.03% |
| German Bundesliga | `bundesliga` | 3-way moneyline | 3,120 | 174 | 30 | 2025-11-29 to 2026-05-25 | 33.33% | -1.93% | -0.01% |
| French Ligue 1 | `ligue1` | 3-way moneyline | 2,262 | 131 | 32 | 2025-11-29 to 2026-05-17 | 34.39% | 4.74% | 0.09% |
| Brazil Serie A | `brazil` | 3-way moneyline | 2,046 | 114 | 41 | 2025-12-03 to 2026-05-25 | 33.33% | 0.10% | -0.01% |
| UEFA Champions League | `ucl` | 3-way moneyline | 1,371 | 78 | 4 | 2025-12-09 to 2026-05-06 | 33.33% | 6.77% | -0.06% |
| NFL | `nfl` | Moneyline | 1,218 | 103 | 0 | 2025-11-25 to 2026-01-25 | 50.00% | 3.13% | 0.01% |
| French Open Tennis | `tennis` | Moneyline | 1,202 | 108 | 106 | 2025-06-07 to 2026-05-28 | 50.00% | -1.10% | -0.00% |
| NFL | `nfl_total` | Total | 980 | 91 | 0 | 2025-11-30 to 2026-02-08 | 50.00% | 0.03% | 0.00% |
| Copa Libertadores | `libertadores` | 3-way moneyline | 839 | 48 | 35 | 2025-11-29 to 2026-05-28 | 33.49% | 2.45% | -0.09% |
| WNBA | `wnba` | Moneyline | 512 | 53 | 53 | 2026-05-08 to 2026-05-29 | 50.00% | 19.03% | 0.00% |
| Italian Serie B | `serie_b` | 3-way moneyline | 459 | 36 | 10 | 2025-11-28 to 2026-05-01 | 33.33% | -10.70% | 0.07% |
| KBO | `kbo` | Moneyline | 240 | 20 | 10 | 2026-04-07 to 2026-05-27 | 50.00% | -2.94% | 0.04% |
| UFC / MMA | `ufc` | Moneyline | 24 | 2 | 2 | 2026-05-17 to 2026-05-17 | 50.00% | -28.52% | -0.00% |
| Boxing | `boxing` | Moneyline | 1 | 1 | 1 | 2026-05-03 to 2026-05-03 | 100.00% | 21.16% | -0.50% |

## Observation Files Selected By Trainer

| Sport / league | Internal key | File | Rows | Events | Dates | Odds API sport keys |
| --- | --- | --- | ---: | ---: | --- | --- |
| AHL | `ahl` | `data/processed/poly_wh_obs_ahl.parquet` | 0 | 0 | None to None | n/a |
| Boxing | `boxing` | `data/processed/poly_wh_obs_boxing_20260503_20260503.parquet` | 1 | 1 | 2026-05-03 to 2026-05-03 | `boxing_boxing` |
| Brazil Serie A | `brazil` | `data/processed/poly_wh_obs_brazil_20251203_20260525.parquet` | 1,368 | 76 | 2025-12-03 to 2026-05-25 | `soccer_brazil_campeonato` |
| Brazil Serie A | `brazil` | `data/processed/poly_wh_obs_brazil_20260128_20260525.parquet` | 1,956 | 109 | 2026-01-28 to 2026-05-25 | `soccer_brazil_campeonato` |
| German Bundesliga | `bundesliga` | `data/processed/poly_wh_obs_bundesliga_20251129_20260525.parquet` | 3,048 | 170 | 2025-11-29 to 2026-05-25 | `soccer_germany_bundesliga` |
| German Bundesliga | `bundesliga` | `data/processed/poly_wh_obs_bundesliga_20251212_20260525.parquet` | 2,832 | 158 | 2025-12-12 to 2026-05-25 | `soccer_germany_bundesliga` |
| English Premier League | `epl` | `data/processed/poly_wh_obs_epl_20251129_20260524.parquet` | 4,101 | 228 | 2025-11-29 to 2026-05-24 | `soccer_epl` |
| English Premier League | `epl` | `data/processed/poly_wh_obs_epl_20251213_20260524.parquet` | 3,591 | 199 | 2025-12-13 to 2026-05-24 | `soccer_epl` |
| J.League | `j_league` | `data/processed/poly_wh_obs_j_league.parquet` | 0 | 0 | None to None | n/a |
| KBO | `kbo` | `data/processed/poly_wh_obs_kbo_20260407_20260501.parquet` | 180 | 15 | 2026-04-07 to 2026-05-01 | `baseball_kbo` |
| KBO | `kbo` | `data/processed/poly_wh_obs_kbo_20260407_20260527.parquet` | 240 | 20 | 2026-04-07 to 2026-05-27 | `baseball_kbo` |
| Spanish La Liga | `la_liga` | `data/processed/poly_wh_obs_la_liga_20251129_20260524.parquet` | 3,411 | 191 | 2025-11-29 to 2026-05-24 | `soccer_spain_la_liga` |
| Spanish La Liga | `la_liga` | `data/processed/poly_wh_obs_la_liga_20251212_20260524.parquet` | 3,141 | 176 | 2025-12-12 to 2026-05-24 | `soccer_spain_la_liga` |
| Copa Libertadores | `libertadores` | `data/processed/poly_wh_obs_libertadores_20251129_20260528.parquet` | 855 | 49 | 2025-11-29 to 2026-05-28 | `soccer_conmebol_copa_libertadores` |
| French Ligue 1 | `ligue1` | `data/processed/poly_wh_obs_ligue1_20251129_20260517.parquet` | 2,577 | 143 | 2025-11-29 to 2026-05-17 | `soccer_france_ligue_one` |
| French Ligue 1 | `ligue1` | `data/processed/poly_wh_obs_ligue1_20251212_20260517.parquet` | 2,415 | 134 | 2025-12-12 to 2026-05-17 | `soccer_france_ligue_one` |
| MLB | `mlb` | `data/processed/poly_wh_obs_mlb_20251001_20260522.parquet` | 8,776 | 755 | 2025-10-01 to 2026-05-22 | `baseball_mlb` |
| MLB | `mlb` | `data/processed/poly_wh_obs_mlb_20260326_20260528.parquet` | 9,682 | 835 | 2026-03-26 to 2026-05-28 | `baseball_mlb` |
| MLB | `mlb_spread` | `data/processed/poly_wh_obs_mlb_spread_20260326_20260528.parquet` | 7,774 | 811 | 2026-03-26 to 2026-05-28 | `baseball_mlb` |
| MLB | `mlb_total` | `data/processed/poly_wh_obs_mlb_total_20260326_20260528.parquet` | 7,474 | 792 | 2026-03-26 to 2026-05-28 | `baseball_mlb` |
| NBA | `nba` | `data/processed/poly_wh_obs_nba_20251021_20260529.parquet` | 14,308 | 1,270 | 2025-10-21 to 2026-05-29 | `basketball_nba` |
| NBA | `nba` | `data/processed/poly_wh_obs_nba_20251206_20260527.parquet` | 10,640 | 948 | 2025-12-06 to 2026-05-27 | `basketball_nba` |
| NBA | `nba_spread` | `data/processed/poly_wh_obs_nba_spread_20251206_20260527.parquet` | 9,552 | 904 | 2025-12-06 to 2026-05-27 | `basketball_nba` |
| NBA | `nba_total` | `data/processed/poly_wh_obs_nba_total_20251206_20260527.parquet` | 12,016 | 960 | 2025-12-06 to 2026-05-27 | `basketball_nba` |
| NFL | `nfl` | `data/processed/poly_wh_obs_nfl_20251125_20260208.parquet` | 1,230 | 104 | 2025-11-25 to 2026-02-08 | `americanfootball_nfl` |
| NFL | `nfl` | `data/processed/poly_wh_obs_nfl_20251130_20260208.parquet` | 1,170 | 99 | 2025-11-30 to 2026-02-08 | `americanfootball_nfl` |
| NFL | `nfl_spread` | `data/processed/poly_wh_obs_nfl_spread_20251130_20260208.parquet` | 1,144 | 89 | 2025-11-30 to 2026-02-08 | `americanfootball_nfl` |
| NFL | `nfl_total` | `data/processed/poly_wh_obs_nfl_total_20251130_20260208.parquet` | 1,140 | 91 | 2025-11-30 to 2026-02-08 | `americanfootball_nfl` |
| NHL | `nhl` | `data/processed/poly_wh_obs_nhl_20251007_20260528.parquet` | 15,663 | 1,386 | 2025-10-07 to 2026-05-28 | `icehockey_nhl` |
| NHL | `nhl` | `data/processed/poly_wh_obs_nhl_20251227_20260528.parquet` | 8,989 | 799 | 2025-12-27 to 2026-05-28 | `icehockey_nhl` |
| NHL | `nhl_spread` | `data/processed/poly_wh_obs_nhl_spread_20251227_20260528.parquet` | 9,538 | 793 | 2025-12-27 to 2026-05-28 | `icehockey_nhl` |
| NHL | `nhl_total` | `data/processed/poly_wh_obs_nhl_total_20251227_20260528.parquet` | 9,512 | 784 | 2025-12-27 to 2026-05-28 | `icehockey_nhl` |
| Italian Serie A | `serie_a` | `data/processed/poly_wh_obs_serie_a_20251129_20260524.parquet` | 3,923 | 222 | 2025-11-29 to 2026-05-24 | `soccer_italy_serie_a` |
| Italian Serie A | `serie_a` | `data/processed/poly_wh_obs_serie_a_20251212_20260524.parquet` | 3,623 | 205 | 2025-12-12 to 2026-05-24 | `soccer_italy_serie_a` |
| Italian Serie B | `serie_b` | `data/processed/poly_wh_obs_serie_b_20251128_20260501.parquet` | 459 | 36 | 2025-11-28 to 2026-05-01 | `soccer_italy_serie_b` |
| Italian Serie B | `serie_b` | `data/processed/poly_wh_obs_serie_b_20251227_20260501.parquet` | 420 | 28 | 2025-12-27 to 2026-05-01 | `soccer_italy_serie_b` |
| French Open Tennis | `tennis` | `data/processed/poly_wh_obs_tennis_20250607_20250608.parquet` | 20 | 2 | 2025-06-07 to 2025-06-08 | `tennis_atp_french_open`, `tennis_wta_french_open` |
| French Open Tennis | `tennis` | `data/processed/poly_wh_obs_tennis_20260524_20260528.parquet` | 1,182 | 106 | 2026-05-24 to 2026-05-28 | `tennis_atp_french_open`, `tennis_wta_french_open` |
| UEFA Champions League | `ucl` | `data/processed/poly_wh_obs_ucl_20251209_20260506.parquet` | 1,371 | 78 | 2025-12-09 to 2026-05-06 | `soccer_uefa_champs_league` |
| UEFA Champions League | `ucl` | `data/processed/poly_wh_obs_ucl_20260120_20260506.parquet` | 1,110 | 63 | 2026-01-20 to 2026-05-06 | `soccer_uefa_champs_league` |
| UFC / MMA | `ufc` | `data/processed/poly_wh_obs_ufc_20260517_20260517.parquet` | 24 | 2 | 2026-05-17 to 2026-05-17 | `mma_mixed_martial_arts` |
| WNBA | `wnba` | `data/processed/poly_wh_obs_wnba_20260508_20260528.parquet` | 492 | 51 | 2026-05-08 to 2026-05-28 | `basketball_wnba` |
| WNBA | `wnba` | `data/processed/poly_wh_obs_wnba_20260508_20260529.parquet` | 512 | 53 | 2026-05-08 to 2026-05-29 | `basketball_wnba` |
| FIFA World Cup | `world_cup` | `data/processed/poly_wh_obs_world_cup.parquet` | 0 | 0 | None to None | n/a |

## Split Summary

```json
{
  "test": {
    "rows": 18845,
    "events": 1009,
    "date_min": "2026-04-25T16:00:00+00:00",
    "date_max": "2026-05-29T02:10:00+00:00",
    "positive_rate": 0.45555850358185196
  },
  "train": {
    "rows": 54213,
    "events": 3024,
    "date_min": "2025-06-07T13:20:00+00:00",
    "date_max": "2026-03-24T02:40:00+00:00",
    "positive_rate": 0.46131001789238746
  },
  "val": {
    "rows": 21040,
    "events": 1008,
    "date_min": "2026-03-24T23:08:00+00:00",
    "date_max": "2026-04-25T14:15:00+00:00",
    "positive_rate": 0.47138783269961976
  }
}
```

## Outcome Group Shape

- Snapshot-side groups: 43,518.
- Average rows per group: 2.162.
- Side-count distribution: `{'1': 13, '2': 36430, '3': 7075}`.
- Groups with no winner: 6.
- Groups with multiple winners: 0.

Example no-winner groups:

```json
[
  {
    "sport_key": "nfl",
    "event_id": "12bbffdcd65d53436b56c68a811ca610",
    "market_kind": "h2h_2way",
    "lead_hours": 1.0,
    "condition_key": "point:999999.0000",
    "rows": 1,
    "sides": 1,
    "won_sum": 0
  },
  {
    "sport_key": "nfl",
    "event_id": "12bbffdcd65d53436b56c68a811ca610",
    "market_kind": "h2h_2way",
    "lead_hours": 2.0,
    "condition_key": "point:999999.0000",
    "rows": 1,
    "sides": 1,
    "won_sum": 0
  },
  {
    "sport_key": "nfl",
    "event_id": "12bbffdcd65d53436b56c68a811ca610",
    "market_kind": "h2h_2way",
    "lead_hours": 4.0,
    "condition_key": "point:999999.0000",
    "rows": 1,
    "sides": 1,
    "won_sum": 0
  },
  {
    "sport_key": "nfl",
    "event_id": "12bbffdcd65d53436b56c68a811ca610",
    "market_kind": "h2h_2way",
    "lead_hours": 6.0,
    "condition_key": "point:999999.0000",
    "rows": 1,
    "sides": 1,
    "won_sum": 0
  },
  {
    "sport_key": "nfl",
    "event_id": "12bbffdcd65d53436b56c68a811ca610",
    "market_kind": "h2h_2way",
    "lead_hours": 12.0,
    "condition_key": "point:999999.0000",
    "rows": 1,
    "sides": 1,
    "won_sum": 0
  },
  {
    "sport_key": "nfl",
    "event_id": "12bbffdcd65d53436b56c68a811ca610",
    "market_kind": "h2h_2way",
    "lead_hours": 24.0,
    "condition_key": "point:999999.0000",
    "rows": 1,
    "sides": 1,
    "won_sum": 0
  }
]
```

Example multi-winner groups:

```json
[]
```

## Event Key Collisions

- Event IDs: 5,041.
- Event IDs reused across observation keys: 2,581.
- Event IDs reused across unrelated sport bases: 0.

## Trading Bot Data Note

For a trading bot, H2H/spread/total labels alone are not enough. The next dataset layer should include Polymarket 1-minute price paths, Odds API 5-minute historical snapshots, line movement, staleness, book dispersion, and close-vs-entry movement.
