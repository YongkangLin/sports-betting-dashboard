# Telonex CLOB + Odds Training-Ready Audit

- Generated: 2026-05-31T18:38:29.067533+00:00
- Label rows checked: 5,392,062
- Training-ready rows: 5,097,400 (94.54%)
- Training-ready markets/tokens: 1,225 / 2,449
- Quarantined rows: 294,662
- Unique market-token minute points: 1,245,323
- Median time-series step: 60.0 seconds
- One-minute step rate: 86.99%

## Validation

- feature_rows_have_causal_odds: True
- feature_rows_have_pre_commence_odds: True
- feature_probabilities_in_bounds: True
- feature_quote_age_non_negative: True

## Coverage By Split

| Split | Rows | Ready rows | Coverage | Markets | Ready markets |
| --- | ---: | ---: | ---: | ---: | ---: |
| test | 810,914 | 782,836 | 96.54% | 178 | 172 |
| train | 3,123,944 | 2,872,556 | 91.95% | 828 | 815 |
| unobserved | 531,302 | 531,302 | 100.00% | 74 | 74 |
| val | 925,902 | 910,706 | 98.36% | 177 | 164 |

## Coverage By Sport

| Sport | Rows | Ready rows | Coverage | Markets | Ready markets |
| --- | ---: | ---: | ---: | ---: | ---: |
| americanfootball_nfl | 415,814 | 415,814 | 100.00% | 80 | 80 |
| baseball_mlb | 48,554 | 0 | 0.00% | 22 | 0 |
| basketball_nba | 250,430 | 231,094 | 92.28% | 266 | 266 |
| basketball_wnba | 191,728 | 191,728 | 100.00% | 60 | 60 |
| icehockey_nhl | 1,222,278 | 1,217,522 | 99.61% | 249 | 249 |
| soccer | 3,263,258 | 3,041,242 | 93.20% | 580 | 570 |

## Quarantine Reasons

| Reason | Rows | Markets | Tokens |
| ---: | ---: | ---: | ---: |
| clob_before_first_stored_odds_snapshot | 237,980 | 84 | 168 |
| missing_causal_odds_join | 56,682 | 46 | 92 |

## Top Quarantined Events

| Sport | Event | Reason | Rows |
| --- | --- | ---: | ---: |
| baseball_mlb | San Francisco Giants vs. Arizona Diamondbacks | clob_before_first_stored_odds_snapshot | 24,330 |
| soccer | Fluminense FC vs. São Paulo FC | clob_before_first_stored_odds_snapshot | 20,622 |
| soccer | AC Milan vs. SS Lazio | clob_before_first_stored_odds_snapshot | 11,864 |
| basketball_nba | Warriors vs. Knicks | clob_before_first_stored_odds_snapshot | 11,750 |
| soccer | Werder Bremen vs. 1. FC Köln | clob_before_first_stored_odds_snapshot | 10,302 |
| soccer | Union Berlin vs. 1. FC Heidenheim | clob_before_first_stored_odds_snapshot | 9,724 |
| soccer | Manchester City vs. Leeds United | clob_before_first_stored_odds_snapshot | 9,508 |
| soccer | Bayer Leverkusen vs. Borussia Dortmund | clob_before_first_stored_odds_snapshot | 9,336 |
| soccer | Tottenham vs. Fulham | clob_before_first_stored_odds_snapshot | 8,958 |
| soccer | Everton vs. Newcastle | clob_before_first_stored_odds_snapshot | 8,528 |
| soccer | Sunderland AFC vs. Bournemouth | clob_before_first_stored_odds_snapshot | 8,230 |
| soccer | AS Monaco FC vs. Paris Saint-Germain FC | clob_before_first_stored_odds_snapshot | 7,966 |
| soccer | Juventus FC vs. Cagliari Calcio | clob_before_first_stored_odds_snapshot | 7,360 |
| soccer | Wolves vs. Nottingham Forest | missing_causal_odds_join | 7,170 |
| soccer | Olympique de Marseille vs. Toulouse FC | clob_before_first_stored_odds_snapshot | 7,024 |
| soccer | Genoa CFC vs. Hellas Verona FC | clob_before_first_stored_odds_snapshot | 6,538 |
| soccer | Athletic Club vs. Real Madrid | missing_causal_odds_join | 5,548 |
| soccer | Paris FC vs. AJ Auxerre | clob_before_first_stored_odds_snapshot | 5,400 |
| soccer | Stade Brestois 29 vs. AS Monaco FC | clob_before_first_stored_odds_snapshot | 5,274 |
| soccer | Barcelona vs. Alaves | clob_before_first_stored_odds_snapshot | 4,938 |
| baseball_mlb | Los Angeles Angels vs. Chicago White Sox | clob_before_first_stored_odds_snapshot | 4,712 |
| soccer | Athletic Club vs. Paris Saint-Germain FC | clob_before_first_stored_odds_snapshot | 4,688 |
| basketball_nba | Wizards vs. Magic | clob_before_first_stored_odds_snapshot | 4,630 |
| soccer | Mallorca vs. Osasuna | clob_before_first_stored_odds_snapshot | 4,052 |
| soccer | Olympique Lyonnais vs. Le Havre AC | missing_causal_odds_join | 3,988 |

Training-ready means the row has executable historical Polymarket CLOB entry state and a causal, pre-commence Odds API sportsbook fair probability joined at or before the model timestamp. Rows outside that definition are quarantined from sportsbook-aware model training.
