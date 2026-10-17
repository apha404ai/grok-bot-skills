---
name: size-calc
description: Run before every entry. Sizes the position so the stop costs exactly 1% of balance.
---

# size-calc

One job: risk exactly 1% per trade.

## When it runs
After all filters pass, before risk-gate.

## Rules
1. Risk in $ = balance x 0.01.
2. Size = risk in $ / |entry - stop|.
3. Round size down to the exchange step, never up.
4. If leverage needed is above your max (default 5x), BLOCK.
5. Fees count. Add taker fee for entry and exit to the risk.

## Output
`size <qty> · risk $<amount> · 1% of balance`.
