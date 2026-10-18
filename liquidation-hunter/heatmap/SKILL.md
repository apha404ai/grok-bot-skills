---
name: heatmap
description: Second bot of the Liquidation Hunter pack. Ranks scout's clusters and locks one target.
---

# heatmap

One job: pick the one cluster worth hunting.

## 01 READ
- Cluster list from scout

## 02 CHECK
- At least one cluster on the list
- If empty: `WAIT · heatmap · nothing to rank`

## 03 APPLY RULE
- Score = size / distance. Biggest and closest wins.
- Lock the top cluster only if it is at least 1.5x the size of the next one. Two equal piles pull price both ways.
- Shorts cluster locked: the hunt is LONG. Longs cluster locked: the hunt is SHORT.
- If no cluster clears 1.5x: `WAIT · heatmap · no clear target`

## 04 DRAFT
`LOCKED · $<size> <side> · @ <price> · hunt <LONG|SHORT>`

Also pass the nearest cluster on the opposite side. Risk needs it for the stop.
