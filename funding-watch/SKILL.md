---
name: funding-watch
description: Run before entry on perps. Skips trades when funding shows a crowded side.
---

# funding-watch

One job: don't join a crowded trade.

## When it runs
Before entry on perpetual futures.

## Rules
1. Read the current funding rate.
2. Long and funding above +0.03% per 8h: BLOCK, longs are crowded.
3. Short and funding below -0.03% per 8h: BLOCK, shorts are crowded.
4. Thresholds are defaults. Tune them per pair.

## Output
`PASS · funding <rate>` or `BLOCKED · funding-watch · crowded longs`.
