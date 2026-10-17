---
name: risk-gate
description: Run before every entry. Blocks any trade where the reward is under 2x the risk.
---

# risk-gate

One job: kill trades with bad reward-to-risk.

## When it runs
Last check before the order goes out, right after size-calc.

## Rules
1. Read entry, stop and target from the trade plan.
2. Risk = |entry - stop|. Reward = |target - entry|.
3. If reward / risk < 2.0, BLOCK.
4. If the stop or the target is missing, BLOCK.
5. Never move the stop or the target to make the numbers pass.

## Output
`PASS` or `BLOCKED · risk-gate · reward 1.4x risk`. Send the line to journal.
