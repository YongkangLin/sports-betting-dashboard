# Edge Investigation - 2026-05-28

Pulled latest `main` through `a3d9efb` and refreshed the live scanners at
`2026-05-28T19:20Z`.

## Current Decision

**Executable now:** cross-book H2H arbs only. Recheck both legs manually before
placing; lines are perishable and venue access/legal availability matters.

**No strict prediction-market trade now:** the validated MLB Polymarket config
has no qualifying side inside the 2h decision window, even with min edge relaxed
to 0.5pp and depth floor lowered to $10.

## Live Arbs

`data/processed/execute_now.json` has 6 arbs over 0.5%:

| ROI | Profit / $1k | Start UTC | Leg A | Leg B |
| ---: | ---: | --- | --- | --- |
| 4.455% | $44.55 | 2026-05-31 00:30 | Lourdes Juarez +280 DraftKings, $275 | Yokasta Valle -227 Pinnacle, $725 |
| 1.397% | $13.97 | 2026-05-30 18:00 | Kevin Lerena -137 Pinnacle, $586 | Ryad Merhy +145 BetUS, $414 |
| 1.051% | $10.51 | 2026-05-29 18:15 | Quentin Halys +1160 FanDuel, $80 | Alexander Zverev -1014 GTBets, $920 |
| 0.976% | $9.76 | 2026-06-13 21:00 | Arturo Cardenas -125 BetUS, $561 | Jordan Martinez +130 Bally Bet, $439 |
| 0.697% | $6.97 | 2026-05-30 12:15 | Kai Asakura -275 Hard Rock, $738 | Cameron Smotherman +285 BetOnline, $262 |
| 0.678% | $6.78 | 2026-05-30 09:35 | Western Bulldogs -170 BetUS, $634 | Collingwood +175 DraftKings, $366 |

The first two arbs also appear as one-sided sharp-anchored +EV:

- Lourdes Juarez +280 DraftKings: +6.87pp edge vs Pinnacle fair.
- Ryad Merhy +145 BetUS: +3.54pp edge vs Pinnacle fair.

One-sided bets are lower confidence than two-leg arbs. Use them only if one
leg is unavailable and stake much smaller.

## Prediction Markets

Strict scanner result:

- MLB Polymarket, 2h target, min edge 0.5pp, min depth $10: **0 trades**.
- `data/processed/live_mlb_poly_picks.json` was cleared to an empty list so no
stale Polymarket pick survives on disk.

Watchlist from the wide diagnostic scan, **not executable yet** because these
are roughly 28-30h before first pitch, not the validated 2h window:

- Los Angeles Angels at Tampa Bay Rays: Angels 0.360 ask vs 0.3744 sharp fair.
- Padres at Nationals: Nationals 0.470 ask vs 0.4838 sharp fair.
- Yankees at Athletics: Athletics 0.430 ask vs 0.4395 sharp fair.
- Tigers at White Sox: White Sox 0.450 ask vs 0.4580 sharp fair.

Re-scan those near 2h before first pitch. Do not buy now solely from the early
diagnostic edge.

## New Warehouse Read

Latest warehouse after pull:

- 10,094 events.
- 9,218,469 quotes.
- 7,630 scores.
- Latest snapshot: 2026-05-28 11:55 UTC.

Vectorized historical arb scan on the expanded warehouse:

| Market | Arbs | Events | Arbs >= 0.5% | Events >= 0.5% | Mean ROI |
| --- | ---: | ---: | ---: | ---: | ---: |
| H2H | 3,880 | 1,653 | 2,612 | 1,194 | 1.43% |
| Totals | 2,986 | 1,148 | 2,468 | 957 | 2.30% |
| Spreads | 891 | 660 | 564 | 462 | 1.86% |

Interpretation: the new exploitable research direction is not a new prediction
market signal; it is **live totals/spreads arb coverage**, especially NHL totals,
MLB totals/spreads, and recurring pairs involving Pinnacle, OnexBet, Bovada,
DraftKings, FanDuel, LowVig, and William Hill US. The current live scan found
H2H arbs only, but history says totals/spreads deserve a dedicated monitor.

## Validation State

Polymarket ranker still has only 2 strict passes, both MLB H2H at 2h lead:

- min edge 1.0pp: test n=27, test ROI=41.5%, CI lower=4.6%.
- min edge 0.5pp: test n=59, test ROI=27.7%, CI lower=2.1%.

Both are still below the 90-day observation gate. MLB spread observations are
larger (5,662 rows, 56d) and positive, but not validated: best visible config
has test ROI around 10% with negative CI lower bound.

## Next Work

1. Build a dedicated live totals/spreads arb dashboard section and alert path.
2. Keep MLB Polymarket H2H on the 2h-before-start scanner only.
3. Extend Polymarket collection forward; CLOB history still cannot backfill the
   90-day validation gate.
4. Paper-track the wide diagnostic MLB Polymarket watchlist when it reaches the
   2h window.
