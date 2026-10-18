# Liquidation Hunter

6 Grok Bots that hunt liquidation cascades. One job each.

Every cascade starts at a pile of stops. This pack finds the pile, checks that the trapped side is really trapped, and drafts a trade that rides price into it. The bots propose, you say yes.

| # | Bot | Job |
|---|---|---|
| 1 | [scout](scout/SKILL.md) | Finds liquidation clusters near price |
| 2 | [heatmap](heatmap/SKILL.md) | Ranks the clusters and locks one target |
| 3 | [oi-watch](oi-watch/SKILL.md) | Confirms the side is trapped |
| 4 | [funding](funding/SKILL.md) | Checks who is paying to stay wrong |
| 5 | [risk](risk/SKILL.md) | 1% risk, 2x reward or no trade |
| 6 | [executor](executor/SKILL.md) | Drafts the limit order and waits for yes |

## How to use

1. Copy all 6 `SKILL.md` files into your Grok Bot, in the order above.
2. Ask it: `run liquidation-hunter on <pair>`.
3. Any `BLOCKED` or `WAIT` stops the hunt. A clean run ends with one order draft and a yes/no question.

Pair it with [journal](../journal/SKILL.md) and [post-mortem](../post-mortem/SKILL.md) from the main desk so every hunt gets logged and every loss becomes a rule.

## Heads up

[liquidation-map](../liquidation-map/SKILL.md) in the main desk keeps your stop away from clusters. This pack does the opposite and aims the target at them. Run one or the other on the same trade, never both.

## Defaults

Clusters within 3% of price, minimum cluster $20M, target locked when it is at least 1.5x the next cluster, OI lookback 4h, funding threshold 0.03% per 8h, 1% risk, 2x reward to risk, order expires after 30 minutes. Tune per pair.

## Want more?

[RESOURCES.md](RESOURCES.md) lists the open-source repos worth using next to this pack: liquidation data, exchange connectors, backtesting, multi-agent frameworks.

Not financial advice. Liquidation data is an estimate on every platform, including this one.
