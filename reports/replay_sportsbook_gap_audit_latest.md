# Replay Sportsbook Gap Audit

- Generated: 2026-05-31T07:55:23.927208+00:00
- Replay events: 277
- Events with sportsbook points: 265
- Events without sportsbook points: 12
- Starts more than 1h after CLOB start: 7
- Ends more than 1h before CLOB end: 2
- Internal sportsbook gap over 30m: 37
- Internal sportsbook gap over 2h: 29
- Median sportsbook points per covered event: 92
- Median CLOB-window overlap ratio: 100.0%

## Interpretation

These gaps are not automatically safe to fill. A missing sportsbook point can mean the sportsbook did not offer that market yet, stopped offering it near/in-play, or the historical API snapshot did not include the matched market. The dashboard shows gaps instead of drawing fake continuous sportsbook prices.

## Worst Late Starts

| Event | Market | Book start late | Book points | Overlap |
|---|---:|---:|---:|---:|
| Vålerenga vs Kristiansund BK total 1.5 | Soccer | 186.3h | 2 | 0.0% |
| Knicks vs Grizzlies | NBA | 132.6h | 101 | 15.1% |
| Wizards vs Magic | NBA | 131.0h | 105 | 15.5% |
| 76ers vs Nuggets | NBA | 130.6h | 115 | 17.2% |
| Pacers vs Knicks | NBA | 129.6h | 107 | 16.6% |
| Warriors vs Knicks | NBA | 129.1h | 127 | 17.6% |
| Rockets vs Wizards | NBA | 128.4h | 117 | 17.1% |
| Jazz vs Spurs | NBA | 0.6h | 97 | 97.2% |
| Pacers vs Hornets | NBA | 0.4h | 98 | 98.0% |
| ATA vs GEN | Soccer | -0.1h | 91 | 100.0% |
| ATA vs TOR | Soccer | -0.1h | 96 | 100.0% |
| Angers vs Paris Saint Germain | Soccer | -0.1h | 80 | 97.9% |
| Elche CF vs Barcelona | Soccer | -0.1h | 95 | 100.0% |
| Hornets vs Knicks | NBA | -0.1h | 106 | 100.0% |
| Le Havre vs Paris Saint Germain | Soccer | -0.1h | 96 | 99.7% |

## Worst Early Ends

| Event | Market | Book end early | Book points | Overlap |
|---|---:|---:|---:|---:|
| Ducks vs Oilers total 4.5 | NHL | 1.9h | 12 | 46.8% |
| Hamburger SV vs Bayern Munich | Soccer | 1.1h | 85 | 94.9% |
| Patriots vs Jets | NFL | 1.0h | 82 | 95.0% |
| Grizzlies vs Rockets | NBA | 0.8h | 112 | 64.9% |
| Spurs vs Bucks | NBA | 0.7h | 102 | 96.8% |
| Pistons vs Pacers | NBA | 0.6h | 100 | 97.7% |
| Wizards vs Trail Blazers | NBA | 0.6h | 102 | 97.7% |
| Suns vs Nuggets | NBA | 0.5h | 17 | 84.8% |
| Real Madrid vs Real Sociedad | Soccer | 0.5h | 92 | 97.8% |
| Wizards vs Suns | NBA | 0.4h | 16 | 85.9% |
| Bucks vs Clippers | NBA | 0.4h | 121 | 90.0% |
| Angers vs Paris Saint Germain | Soccer | 0.4h | 80 | 97.9% |
| Pacers vs Rockets | NBA | 0.2h | 18 | 94.4% |
| Suns vs Thunder | NBA | 0.2h | 92 | 99.1% |
| Borussia Dortmund vs SC Freiburg | Soccer | 0.2h | 74 | 99.0% |

## Worst Internal Gaps

| Event | Market | Max gap | Book points |
|---|---:|---:|---:|
| Wizards vs Bulls | NBA | 21.0h | 35 |
| Wizards vs Hawks | NBA | 10.5h | 74 |
| Real Madrid vs Celta Vigo | Soccer | 9.5h | 157 |
| Bayern Munich vs VfB Stuttgart | Soccer | 8.5h | 141 |
| ATA vs PAR | Soccer | 8.5h | 137 |
| ROM vs GEN | Soccer | 8.3h | 158 |
| VfB Stuttgart vs VfL Wolfsburg | Soccer | 7.5h | 142 |
| Manchester United vs Crystal Palace | Soccer | 7.2h | 144 |
| PAR vs Napoli | Soccer | 6.0h | 146 |
| VfB Stuttgart vs Hamburger SV | Soccer | 6.0h | 154 |
| Napoli vs BOL | Soccer | 6.0h | 169 |
| VER vs MIL | Soccer | 6.0h | 146 |
| Juventus vs BOL | Soccer | 6.0h | 169 |
| ROM vs CAG | Soccer | 5.8h | 172 |
| CRE vs MIL | Soccer | 5.0h | 143 |
