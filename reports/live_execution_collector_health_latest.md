# Live Execution Collector Health

- Generated: 2026-05-31T01:46:41.774587+00:00
- Loop status: running
- Started: 2026-05-29T22:56:51.160360+00:00
- Loop count: 556
- Capital enabled: false
- Alerts: 2

## Alerts

- telonex_live_score failed (66 consecutive)
- paper_trade failed (1 consecutive)

## Task State

```text
http_capture: ok=True last_success=2026-05-31T01:45:45.704727+00:00 failures=0
ws_capture: ok=True last_success=2026-05-31T01:46:19.873739+00:00 failures=0
telonex_live_score: ok=False last_success=2026-05-30T20:09:38.550837+00:00 failures=66
paper_trade: ok=False last_success=2026-05-31T01:41:32.021482+00:00 failures=1
post_trade_http_capture: ok=True last_success=2026-05-31T01:41:39.801348+00:00 failures=0
live_execution_quality: ok=True last_success=2026-05-31T01:41:49.058669+00:00 failures=0
user_lifecycle: ok=True last_success=2026-05-31T01:41:58.701453+00:00 failures=0
execution_training: ok=True last_success=2026-05-31T01:43:03.641236+00:00 failures=0
queue_training: ok=True last_success=2026-05-31T01:43:18.593142+00:00 failures=0
queue_fill_model: ok=True last_success=2026-05-31T01:28:23.231863+00:00 failures=0
model_monitor: ok=True last_success=2026-05-31T01:28:24.199057+00:00 failures=0
game_state: ok=True last_success=2026-05-31T01:28:32.975687+00:00 failures=0
kalshi_candidates: ok=True last_success=2026-05-31T01:28:43.434857+00:00 failures=0
kalshi_verified: ok=True last_success=2026-05-31T01:28:43.942716+00:00 failures=0
secret_hygiene: ok=True last_success=2026-05-31T01:28:48.810037+00:00 failures=0
dashboard_status: ok=True last_success=2026-05-31T01:29:11.639921+00:00 failures=0
```
