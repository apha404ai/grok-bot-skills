---
name: news-filter
description: Run before entry. Blocks trades within 15 minutes of high-impact (red) news.
---

# news-filter

One job: stay out of red news.

## When it runs
Early, together with session-timer.

## Rules
1. Check the economic calendar for high-impact events on the currencies or asset in the pair.
2. Red event within 15 minutes before or after now: BLOCK.
3. Open trade and red news coming in 15 minutes: tell the human, don't close on your own.

## Output
`PASS` or `BLOCKED · news-filter · <event> in 9 min`.
