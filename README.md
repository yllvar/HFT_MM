## Overview 🤖

This repository contains a Python trading bot utilizing the ccxt library. The bot is designed to follow a market maker strategy, aiming to generate profits by providing liquidity to the market.

## Setup 🛠️

To set up the bot:
1. Fetch API credentials from environment variables.
2. Initialize an instance of the Kucoin Futures exchange using ccxt.

## Parameters 📊

The bot allows customization of parameters such as:
- Trade size
- Trading pair (symbol)
- Percentage from the high (lh)
- Timeframe
- Risk parameters

## Key Functions 📝

The bot includes the following key functions:
- **get_bid_ask**: Retrieve bid and ask prices from the order book.
- **open_positions**: Obtain information about open positions.
- **size_kill**: Check if position size exceeds maximum risk and close positions if necessary.
- **kill_switch**: Cancel all orders and close positions.
- **active_orders2**: Check for active orders and place stop-loss or close orders if necessary.
- **tr, atr, notrade_atr**: Calculate true range (TR) and average true range (ATR) indicators.
- **get_pnl**: Calculate and print profit/loss percentage based on open positions.
- **stop_order**: Place a stop-loss order based on bid/ask price.
- **bot**: Main function orchestrating the trading logic.

## Trading Strategy 📈

The bot's trading strategy involves:
- Continuously assessing market conditions, including ATR, price range, and open positions.
- Deciding whether to buy/sell based on predefined conditions such as bid/ask prices, open ranges, and ATR.
- Managing risk through stop-loss orders and ensuring position size stays within the maximum risk threshold.
- Monitoring time limits for open positions and closing them if necessary.

## How to Run ▶️

To run the bot:
1. Install required Python libraries: ccxt, pandas, dotenv from requirements.txt
2. Set up environment variables (API_KEY, SECRET_KEY, PASSPHRASE) with your Kucoin API credentials.
3. Copy and paste the code into a Jupyter Notebook cell.
4. Execute the cell to run the bot.

Before running the bot, ensure to thoroughly review and understand the code, especially if using it for live trading. Incorrect configurations or logic errors could lead to financial losses. Implement appropriate risk management strategies.

