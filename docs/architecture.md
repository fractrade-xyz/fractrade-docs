# Core Architecture

The fractrade.xyz platform consists of multiple components. The main components are:

- **fractrade.xyz**  
  Main website with some infos

- **fractrade.xyz App**  
  The webapp is the main interface for interacting with your Agents, creating new agents, researching strategies, etc. 

- **fractrade docs**  
  This documentation

- **Fractrade ExecutionClient**  
  Open source Python client for executing trades on Hyperliquid, receives signals from your Agents.

- **Fractrade Telegram Bot**  
  Telegram bot for getting notifications from your Agents.

- **Fractrade Client API**  
  API for interacting with your Agents.

- **Fractrade Publisher API**  
  API for publishing trading signals and data.

- **Fractrade AI Agent Framework**  
  Open Source framework for creating and training AI agents which can publish signals and data to the Publisher API.

- **Fractrade Worker**  
  Distributed task queue for executing all platform tasks like sending signals, executing trades, doing custom calculations, scanning the Hyperliquid ecosystem, monitoring on-chain data and offchain data, etc.

# How it works for users

Users can signup on the fractrade.xyz App. They can research strategies and configure custom AI agents which execute their preferred strategies. Some strategies are generic, which means the send the same signals/data for all users. Other strategies are custom, which means the send different signals/data for each user.

## Generic strategies
Examples include:

- A new token launched on Hyperliquid
- A new PERP is available on Hyperliquid
- The Market sentiment on Twitter changed

## Custom strategies
Examples include:

- Your portfolio made 300% profit in token X, you might want to rebalance part of the profits into token Y
- There is a big TWAP order executing for one of the tokens in your portfolio 
- The smart wallet you are following just bought a new token XYZ
- Your current open long position on BTC-PERP is at risk. There is an upcoming FOMC meeting increasing the volatility of the market and you are near a resistance level

When your agent and strategy are setup, you can start the agent and see the signals in the UI, on the Websockets and can subscribe to them with the Telegram Bot. If you trade manually on Hyperliquid, using the fractrade.xyz App UI makes sense. For users who want to trade in Telegram with out Telegram Bot integration, setting up the agent subscription in Telegram is useful. And for fully automated algorithmic trading, you want to use the websocket connection to your agent, which gives you all signals in real time and allows you to act on the data or execute trades.

Agents each have an input and an output. We are basically just passing a JSON data structure from one agent to the next. The output of the previous agent is the input for the next agent and so on. That way we can easily combine multiple agents to create more complex strategies. Your execution client then would just connect to the websocket of the last ageent in the chain and receive the final data / signals. 

# How it works for Publishers

Developers can use our publisher framework to create custom strategies and data endpoints. They can be published on the marketplace and also require a subscription payment in USDC. Especially running complex AI models might require some resources and a subscription is the only way to make it sustainable.

To get our marketplace started, fractrade.xyz will offer a set of strategies, data endpoints and agents ready to use, but eventually our goal is to have a marketplace with thousands of strategies, data endpoints and agents. We want to learn and develop together with our community and make it work for everyone.

