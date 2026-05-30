# Live Game State

- Generated: 2026-05-30T23:55:35.265438+00:00
- ESPN scoreboard rows: 36
- Polymarket event matches: 23
- Rows appended: {'scoreboards': 36, 'matches': 23}
- Scoreline regimes: {'pre': 22, 'blowout': 7, 'one_run': 4, 'tied': 2, 'close': 1}
- Garbage-time proxy rows: 0

This feed supplies score/status timestamps for post-event overreaction research. It is a public scoreboard snapshot, not a low-latency official league feed. Scoreline and garbage-time fields are segmentation guardrails, not a trading trigger.

## Matches

```text
                                   poly_event               score_sport            home_team             away_team  home_score  away_score status_state scoreline_regime  garbage_time_proxy  match_score
           Atlanta Braves vs. Cincinnati Reds              baseball_mlb      Cincinnati Reds        Atlanta Braves           2           1           in          one_run               False          1.0
         Milwaukee Brewers vs. Houston Astros              baseball_mlb       Houston Astros     Milwaukee Brewers           0           0          pre              pre               False          1.0
        Paris Saint-Germain FC vs. Arsenal FC soccer_uefa_champs_league  Paris Saint-Germain               Arsenal           1           1         post             tied               False          1.0
        Los Angeles Angels vs. Tampa Bay Rays              baseball_mlb       Tampa Bay Rays    Los Angeles Angels           3          14         post          blowout               False          1.0
         Kansas City Royals vs. Texas Rangers              baseball_mlb        Texas Rangers    Kansas City Royals           7           6         post          one_run               False          1.0
    San Diego Padres vs. Washington Nationals              baseball_mlb Washington Nationals      San Diego Padres           9           4         post          blowout               False          1.0
              Miami Marlins vs. New York Mets              baseball_mlb        New York Mets         Miami Marlins           6           1         post          blowout               False          1.0
      Toronto Blue Jays vs. Baltimore Orioles              baseball_mlb    Baltimore Orioles     Toronto Blue Jays           6           5         post          one_run               False          1.0
       Boston Red Sox vs. Cleveland Guardians              baseball_mlb  Cleveland Guardians        Boston Red Sox           1           9         post          blowout               False          1.0
       Minnesota Twins vs. Pittsburgh Pirates              baseball_mlb   Pittsburgh Pirates       Minnesota Twins          10           9         post          one_run               False          1.0
Philadelphia Phillies vs. Los Angeles Dodgers              baseball_mlb  Los Angeles Dodgers Philadelphia Phillies           0           0          pre              pre               False          1.0
               New York Yankees vs. Athletics              baseball_mlb            Athletics      New York Yankees           0           0          pre              pre               False          1.0
    San Diego Padres vs. Washington Nationals              baseball_mlb Washington Nationals      San Diego Padres           9           4         post          blowout               False          1.0
         Chicago Cubs vs. St. Louis Cardinals              baseball_mlb  St. Louis Cardinals          Chicago Cubs           0           0           in             tied               False          1.0
    Arizona Diamondbacks vs. Seattle Mariners              baseball_mlb     Seattle Mariners  Arizona Diamondbacks           0           0          pre              pre               False          1.0
              Miami Marlins vs. New York Mets              baseball_mlb        New York Mets         Miami Marlins           6           1         post          blowout               False          1.0
         Detroit Tigers vs. Chicago White Sox              baseball_mlb    Chicago White Sox        Detroit Tigers           7           1         post          blowout               False          1.0
         Kansas City Royals vs. Texas Rangers              baseball_mlb        Texas Rangers    Kansas City Royals           7           6         post          one_run               False          1.0
         Milwaukee Brewers vs. Houston Astros              baseball_mlb       Houston Astros     Milwaukee Brewers           9           2         post          blowout               False          1.0
    San Francisco Giants vs. Colorado Rockies              baseball_mlb     Colorado Rockies  San Francisco Giants           0           0          pre              pre               False          1.0
```
