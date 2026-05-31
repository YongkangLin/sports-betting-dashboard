# Secret Hygiene

- Generated: 2026-05-31T00:22:44.888188+00:00
- Findings: 0
- Critical: 0
- Rotation required for credentials pasted in chat: yes

The scanner masks values and never writes full secrets. `.env` is ignored by git; real credentials should stay there or in an external secret manager.

## Required Manual Action

- Rotate any GitHub/Odds/Polymarket/Kalshi keys that were pasted into chat or logs.
- Keep live trading private keys out of this repo; use environment variables or a secret manager.
