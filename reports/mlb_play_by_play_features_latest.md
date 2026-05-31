# MLB Play-By-Play Feature Backfill

- Generated: 2026-05-31T04:42:34.342115+00:00
- Requested MLB markets: 149
- Matched MLB games: 149
- Markets with normalized events: 86
- Normalized event rows: 6,560
- Feature rows: 174,624
- Feature markets: 86
- MLB decision coverage: 86.13%
- MLB market coverage: 57.72%

These features are causal: each decision timestamp only sees official MLB events with `event_ts <= asof_ts`.

## Known Limits

- This is plate-appearance level, not pitch-level, so it is enough for score/base/out state and post-run shocks but not pitch-by-pitch microstructure.
- Win-probability deltas are placeholders until an MLB WPA model is added.
- Features are market-level right now; token-side mapping is the next layer for exact buy/sell explanation.

## Sample Failures

- `mlb-tb-nyy-2026-05-23`: empty_feed_events
- `mlb-tb-nyy-2026-05-23-nrfi`: empty_feed_events
- `mlb-kc-tex-2026-05-31-nrfi`: empty_feed_events
- `mlb-bos-cle-2026-05-31-nrfi`: empty_feed_events
- `mlb-mia-nym-2026-05-31-nrfi`: empty_feed_events
- `mlb-ari-sea-2026-05-31-nrfi`: empty_feed_events
- `mlb-laa-tb-2026-05-31-nrfi`: empty_feed_events
- `mlb-chc-stl-2026-05-31-nrfi`: empty_feed_events
- `mlb-det-cws-2026-05-31-nrfi`: empty_feed_events
- `mlb-atl-cin-2026-05-31-nrfi`: empty_feed_events
