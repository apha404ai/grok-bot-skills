---
name: funding
description: Fourth bot of the Liquidation Hunter pack. Reads funding to see who is paying to hold a losing side.
---

# funding

One job: check who is paying to stay wrong.

## 01 READ
- Current funding rate per 8h, averaged across the exchanges you have
- Hunt direction from heatmap

## 02 CHECK
- Funding under 1h old
- If missing: PASS and log `no funding data`

## 03 APPLY RULE
- Hunt LONG and funding negative: shorts are paying to hold. That is fuel. PASS.
- Hunt SHORT and funding positive: longs are paying to hold. PASS.
- Hunt LONG and funding above +0.03%: you would be joining crowded longs. `BLOCKED · funding · crowded longs`
- Hunt SHORT and funding below -0.03%: `BLOCKED · funding · crowded shorts`
- Near zero: PASS, note `neutral funding`

## 04 DRAFT
`PASS · funding <rate> · <shorts|longs> paying`
