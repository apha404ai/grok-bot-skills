---
name: spread-check
description: Run right before the order. Blocks entry if the spread is above 0.05%.
---

# spread-check

One job: don't pay a wide spread.

## When it runs
Right before sending the order.

## Rules
1. Spread % = (ask - bid) / mid x 100.
2. Above 0.05%: BLOCK and recheck in 60 seconds, max 3 tries.
3. Spread fine but the top of the book can't fill your size: BLOCK.

## Output
`PASS · spread 0.02%` or `BLOCKED · spread-check · 0.11%`.
