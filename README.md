# Grok Bot skills

10 trading skills for Grok Bot. One job each.

Every trade idea runs through them top to bottom. Any `BLOCKED` stops the trade. The bot proposes, you say yes.

| # | Skill | Job |
|---|---|---|
| 1 | [session-timer](session-timer/SKILL.md) | Only trades liquid hours |
| 2 | [news-filter](news-filter/SKILL.md) | No red news within 15 min |
| 3 | [trend-filter](trend-filter/SKILL.md) | Only trades with the 4h trend |
| 4 | [funding-watch](funding-watch/SKILL.md) | Skips crowded funding |
| 5 | [liquidation-map](liquidation-map/SKILL.md) | Keeps stops out of liquidation walls |
| 6 | [spread-check](spread-check/SKILL.md) | Spread under 0.05% |
| 7 | [size-calc](size-calc/SKILL.md) | Risks exactly 1% of balance |
| 8 | [risk-gate](risk-gate/SKILL.md) | Blocks anything under 2x reward |
| 9 | [journal](journal/SKILL.md) | Logs every trade, blocked ones too |
| 10 | [post-mortem](post-mortem/SKILL.md) | Turns every loss into a new rule |

## How to use

1. Open a skill, copy its `SKILL.md`.
2. Add it to your Grok Bot as a skill, or paste all 10 into its instructions.
3. Keep the order above. Cheap filters (time, news, trend) run first, sizing and risk-gate run last, right before the order.

## Defaults

2x reward to risk, 1% risk per trade, spread 0.05%, 15 minutes around red news, funding 0.03% per 8h, 4h trend on the 50 EMA, liquid hours 07:00-20:00 UTC. Change them to fit your market.

## License

MIT. Steal all of them.

Not financial advice.
