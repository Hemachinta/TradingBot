
## What is "SockTrader"?

SockTrader is an open source cryptocurrency trading bot. You can use it to automatically buy and/or sell cryptocurrencies based on a strategy that you've programmed.
The strategy basically contains a set of rules that will define when and how the bot should act in the cryptocurrency market. These rules can be based on technical analysis ([what is technical analysis?](https://www.investopedia.com/terms/t/technicalanalysis.asp))
or you could simply tell the bot to buy/sell at certain price levels. In fact, it's up to you to decide the rules of the game!

The name "SockTrader" comes from web**sock**et based trading bot. Which means that SockTrader will try to make use of a realtime connection with the exchange. This has the advantage
that one can act very quickly in a changing market with low latency.

## Looking for SockTrader v1?

The [dashboard](https://socktrader.io/) is currently incompatible with SockTrader v2.
Use [SockTrader v1](https://github.com/SockTrader/SockTrader/tree/socktrader-v1) instead

## Features

- 🚀 Realtime super-fast websocket trading.
- 🌈 Written in TypeScript!
- 🌿 Unit tested source code.
- 📝 Paper trading a strategy on LIVE exchange data.
- 🏡 Backtesting engine with local data.
- 🚢 Run SockTrader inside a docker container.
- More features soon..

## Getting started

# Quickstart

1. Git clone 
2. Install NodeJS dependencies. `npm i`
3. Copy `config/default.json` to `config/local.json` and edit.
4. Start postgres database `docker-compose up`
5. Run the MovingAverageStrategy on LocalExchange. `npm run start:backtest`

## Connect your Binance account

You feel like your strategy is production ready?
Good! We'll help you to connect your SockTrader strategy to your Binance account.

1. Copy `config/default.json` to `config/local.json`
2. Go to your Binance account under API Management, create a new API key
3. Provide the apiSecret and apiKey in `config/local.json`
4. Don't forget to change the exchange in your strategy to `new Binance()` and you're good to go!

### API key restrictions

By default, the newly created API key does not allow you to place orders, only reads are allowed.
To get started:

1. Go to your Binance account
2. Under API restrictions enable 'Enable Spot & Margin Trading'

