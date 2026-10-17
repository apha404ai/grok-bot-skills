---
name: journal
description: Run on every trade idea, taken or blocked. Logs everything in one line per event.
---

# journal

One job: write it all down.

## When it runs
After every skill decision and every fill or close.

## Rules
1. One line per event: id, time UTC, pair, side, entry, stop, target, size, risk $, each skill's verdict, result.
2. Blocked trades get logged too, with the skill that blocked them and the $ the stop would have cost.
3. Never edit an old line. Corrections go in as a new line.
4. Losses get handed to post-mortem.

## Output
Append to `journal.csv`.
