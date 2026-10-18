---
name: risk
description: Fifth bot of the Liquidation Hunter pack. Builds entry, stop, target and size, and kills anything under 2x reward.
---

# risk

One job: no hunt is worth more than 1%.

## 01 READ
- Account balance
- Mark price
- Locked cluster and opposite cluster from heatmap

## 02 CHECK
- Balance and price present
- If missing: `CHECK BLOCKED · risk · missing balance or price`

## 03 APPLY RULE
- Entry: current price, or a pullback limit no more than 0.3% away
- Target: just in front of the locked cluster. Price often reverses inside the pile, so take profit at its near edge.
- Stop: beyond the opposite cluster, never inside it. If the opposite cluster is too far for 2x, the trade dies.
- Size: risk exactly 1% of balance. Size = (balance x 0.01) / |entry - stop|
- Reward / risk must be 2.0 or more. Under that: `BLOCKED · risk · reward <x>x risk`
- Never move the stop or the target to make the numbers pass.

## 04 DRAFT
`<LONG|SHORT> · entry <p> · stop <p> · target <p> · size <qty> · R:R <x> · risk 1%`
