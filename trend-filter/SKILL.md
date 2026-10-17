---
name: trend-filter
description: Run before entry. Only allows trades in the direction of the 4h trend.
---

# trend-filter

One job: no trading against the 4h trend.

## When it runs
Early, right after the session and news checks.

## Rules
1. On the 4h chart: price above the 50 EMA and the 50 EMA rising = uptrend. Below and falling = downtrend. Anything else = no trend.
2. Long only in an uptrend. Short only in a downtrend.
3. No trend: BLOCK.

## Output
`PASS · 4h up`, `BLOCKED · trend-filter · long vs 4h down`.
