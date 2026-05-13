# Design Notes

## Concept

- Source inspiration: Endless Jumper
- Twist: `Dynamic obstacles`
- Format: finite deterministic proof route instead of a literal endless survival loop
- Goal: preserve the feeling of a reactive endless hopper while giving unattended automation a stable finish state

## Mechanics

- The player auto-runs on a single lane and only needs one primary input: jump.
- Eight named pulse lanes animate on fixed cycles, but each lane settles into a bounded pass phase near the runner so the route stays fair.
- Rings act as optional score pickups above or between lanes.
- The route supports pause, reset, restart, fullscreen, `window.advanceTime(ms)`, and `window.render_game_to_text()`.

## Visual Direction

- Warm ivory and sunrise orange foregrounds against a muted navy city silhouette.
- Large editorial type on the left, compact canvas stage on the right, and live state telemetry beneath.
- The runner silhouette uses a teal body and pale motion glow so the jump arc reads cleanly in screenshots and GIFs.

## Proof Route

- Verified proof result: `13.13s`, `2875` score, `8/8` gates, `6/8` rings, peak combo `8`.
- Capture set covers title, live opening, pulse-ladder midpoint, paused state, finish banner, and reset state.
