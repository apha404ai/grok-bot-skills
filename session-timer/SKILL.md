---
name: session-timer
description: Run first on every trade idea. Only allows trading during liquid hours.
---

# session-timer

One job: trade only when the market is liquid.

## When it runs
First check on every idea.

## Rules
1. Default liquid window: 07:00-20:00 UTC on weekdays. Set your own per market.
2. Outside the window: BLOCK.
3. Weekends: BLOCK unless you turned weekend trading on.
4. Last 30 minutes before daily close: BLOCK.

## Output
`PASS · <session>` or `BLOCKED · session-timer · off hours`.
