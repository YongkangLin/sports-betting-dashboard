# Proxy Convergence Model

Built at: `2026-05-29T21:26:09.007892+00:00`
Source ML run: `20260529T212018Z`
Label: `fixed` buy YES proxy PnL at `60s`, delay `0s`, adverse `0.01`.
LEV monitor: entry price minus market midpoint after `3s`; negative is favorable for a buy.
No-new-entry midpoint bounds: `0.03` to `0.97`.

## Verdict

Research gate: `HOLD`
Live-capital gate: `HOLD`

## Dataset

Training rows with labels: `88,276`
Events: `4,924`
Target positive rate: `0.03%`
Skipped rows: `{'no_sport_series': 0, 'no_side_series': 1179}`
Post-hoc probability calibration: `isotonic`.

## Classification

| Split | Rows | Positive | AUC | Log loss | Brier | ECE-10 |
|---|---:|---:|---:|---:|---:|---:|
| train | 51,615 | 0.02% | 0.999 | 0.001 | 0.000 | 0.000 |
| val | 19,543 | 0.04% | 0.619 | 0.003 | 0.000 | 0.000 |
| test | 17,118 | 0.03% | 0.605 | 0.003 | 0.000 | 0.000 |

## Trading Threshold

Selected threshold from validation: `0.000`

| Split | Trades | Events | ROI | 95% CI | PnL | Win rate | Avg LEV | Favorable LEV |
|---|---:|---:|---:|---|---:|---:|---:|---:|
| train | 4,998 | 1,740 | -7.30% | -7.48% to -7.27% | $-36,470.20 | 0.24% | 0.0099 | 0.78% |
| val | 3,202 | 802 | -7.33% | -7.55% to -7.28% | $-23,456.16 | 0.09% | 0.0100 | 0.34% |
| test | 3,471 | 792 | -7.05% | -7.30% to -7.05% | $-24,484.58 | 0.06% | 0.0100 | 0.23% |

## Validation Threshold Grid

| Threshold | Trades | Events | ROI | CI low | CI high |
|---:|---:|---:|---:|---:|---:|
| 0.000 | 19543 | 987 | -7.76% | -7.94% | -7.74% |
| 0.000 | 19543 | 987 | -7.76% | -7.94% | -7.74% |
| 0.000 | 19543 | 987 | -7.76% | -7.94% | -7.74% |
| 0.000 | 19543 | 987 | -7.76% | -7.94% | -7.74% |
| 0.000 | 19543 | 987 | -7.76% | -7.94% | -7.74% |
| 0.000 | 19543 | 987 | -7.76% | -7.94% | -7.74% |
| 0.000 | 3202 | 802 | -7.33% | -7.55% | -7.28% |
| 0.000 | 3202 | 802 | -7.33% | -7.55% | -7.28% |
| 0.001 | 1182 | 558 | -7.90% | -7.94% | -7.44% |
| 0.001 | 1182 | 558 | -7.90% | -7.94% | -7.44% |
| 0.001 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.001 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.002 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.002 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.003 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.005 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.007 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.010 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.015 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.020 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.030 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.050 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.100 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.200 | 4 | 4 | 6.91% | -16.53% | 49.93% |
| 0.500 | 0 | 0 | 0.00% |  |  |

## Limitations

- Uses historical Polymarket midpoint as a proxy, not executable CLOB bid/ask/depth.
- Labels are fixed-horizon proxy PnL by default, not realized fills or queue-aware order outcomes.
- This is a better training target for trading than winner prediction, but it still cannot prove live profitability without CLOB capture.
