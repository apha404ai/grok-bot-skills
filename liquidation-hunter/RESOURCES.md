# Open-source repos worth stealing

Free repos that do the heavy lifting behind a liquidation desk. Check each license before you ship anything built on them.

## Liquidation data
- [aoki-h-jp/py-liquidation-map](https://github.com/aoki-h-jp/py-liquidation-map): draws liquidation maps from Binance and Bybit historical trades. MIT. Good for feeding scout.
- [moondevonyt/Hyperliquid-Data-Layer-API](https://github.com/moondevonyt/Hyperliquid-Data-Layer-API): Hyperliquid liquidations, whale positions, orderbooks and candles from Python. Needs a free API key from the author; higher limits are a paid tier.

## Talking to exchanges
- [ccxt/ccxt](https://github.com/ccxt/ccxt): one library for 100+ exchanges. Prices, funding, open interest, orders.
- [hyperliquid-dex/hyperliquid-python-sdk](https://github.com/hyperliquid-dex/hyperliquid-python-sdk): official Hyperliquid SDK. Market data, orders, websockets.
- [bybit-exchange/pybit](https://github.com/bybit-exchange/pybit): official Bybit connector, includes the liquidation websocket stream.

## Running bots
- [freqtrade/freqtrade](https://github.com/freqtrade/freqtrade): full crypto bot with backtesting, dry-run mode and a Telegram remote. Supports futures.
- [hummingbot/hummingbot](https://github.com/hummingbot/hummingbot): market making and arbitrage framework, many exchange connectors.
- [jesse-ai/jesse](https://github.com/jesse-ai/jesse): Python framework for writing and backtesting strategies.
- [nautechsystems/nautilus_trader](https://github.com/nautechsystems/nautilus_trader): fast event-driven engine, same code for backtest and live.

## Backtesting before you trust a single rule
- [polakowo/vectorbt](https://github.com/polakowo/vectorbt): test thousands of parameter combos in seconds.
- [kernc/backtesting.py](https://github.com/kernc/backtesting.py): small, readable backtester. Good first one.

## Multi-agent and Grok
- [TauricResearch/TradingAgents](https://github.com/TauricResearch/TradingAgents): analyst, researcher, trader and risk agents arguing before a trade. Works with xAI Grok models.
- [virattt/ai-hedge-fund](https://github.com/virattt/ai-hedge-fund): a team of AI agents that each analyze a stock from one angle. Educational.
- [xai-org/xai-sdk-python](https://github.com/xai-org/xai-sdk-python): official xAI SDK if you want to wire Grok into your own bot code.

Paper trade first. Every repo here can lose money just as fast as it makes it.
