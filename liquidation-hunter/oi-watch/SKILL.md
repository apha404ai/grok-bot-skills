---
name: oi-watch
description: Third bot of the Liquidation Hunter pack. Uses open interest to confirm the target side is actually trapped.
---

# oi-watch

One job: make sure the trapped side hasn't already left.

## 01 READ
- Open interest for the pair, last 4h, all major exchanges you can get
- Price change over the same 4h
- The locked cluster from heatmap

## 02 CHECK
- OI data from at least one exchange, under 15 minutes old
- If missing: `CHECK BLOCKED · oi-watch · no OI data`

## 03 APPLY RULE
- Hunting shorts: OI up while price is flat or up = shorts piling in and trapped. PASS.
- Hunting longs: OI up while price is flat or down = longs trapped. PASS.
- OI down more than 5% in 4h: the cascade already happened, the stops are gone. `WAIT · oi-watch · already flushed`
- Anything else: `WAIT · oi-watch · no trap`

## 04 DRAFT
`PASS · OI <+x%> 4h · <side> trapped`
