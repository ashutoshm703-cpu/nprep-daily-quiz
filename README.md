# NPrep — Daily Quiz prototype

Interactive prototype of the NORCET daily-quiz surface: home card, 3-question flow,
result screen, streak model and the post-attempt home state.

Single self-contained HTML file. No build, no dependencies.

## Reviewing it

The control bar at the bottom of the page switches build and state.

| Control | Options |
|---|---|
| **Build** | `Refined` (default) · `Classic` (before the final design pass) |
| **Day** | `0`–`7` — walks the habit arc |
| **Then** | `Attempted` · `Evening` · `Missed a day` |

They compose, e.g. `?day=5&risk=1` or `?day=0&ui=classic`.

## Notes

- Streak: the number carries length, the flame carries today (hollow = not done, solid = done).
- At-risk state is gated to day 4+ — a threat about losing a 2-day streak spends a mechanism you need later.
- One grace per week absorbs a missed day rather than resetting to zero.
- The `243 nurses attempted today` count is **simulated** in this prototype. In production it must come from a real event, never a timer.
- Avatars and the instructor thumbnail are SVG placeholders.
