---
name: liquidation-map
description: Run before entry. Keeps stops out of liquidation clusters and targets in front of them.
---

# liquidation-map

One job: don't trade into liquidation walls.

## When it runs
Before size-calc, once entry, stop and target exist.

## Rules
1. Pull the liquidation heatmap for the pair (whatever data source your bot has).
2. If the stop sits inside or just past a big cluster on your side, move the trade idea to WAIT. Price likes to sweep those.
3. If a big cluster sits between entry and target, set the target in front of it and hand the new target to risk-gate.
4. No liquidation data available: PASS, and log `no liq data`.

## Output
`PASS`, `WAIT · stop inside cluster` or `ADJUST · target -> <price>`.
