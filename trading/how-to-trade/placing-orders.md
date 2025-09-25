# Placing Orders

## Order Types

When placing a trade on Synthetix, you’ll choose an order type. Each order type determines how and when your trade is executed.

#### Market Orders

Market orders execute immediately at the best available price in the order book.

* Useful when you want to enter or exit a position quickly.
* May incur slippage if liquidity is thin or the market is volatile.

#### Limit Orders

Limit orders execute only at the price you set, or better.

* Useful if you want to control the price of your entry or exit.
* Orders remain open until they are filled or canceled.
* Can result in partial fills if only part of your size is matched.

#### Stop Orders

Stop orders trigger once the market hits the price you set.

* Commonly used for stop-loss or take-profit strategies.
* Two types are supported:
  * **Stop Market** – converts to a Market order once triggered.
  * **Stop Limit** – converts to a Limit order once triggered, allowing a trader to buy or sell in a range.

### Advanced Options

Several options can be applied when placing an order. These appear directly in the order entry panel.

* **Reduce-Only**\
  Ensures the order can only reduce or close an existing position. Useful for safely exiting without flipping direction. Take&#x20;
* **Post-Only**\
  Ensures the order adds liquidity to the order book. If it would immediately execute, it is canceled.
* **Take-Profit / Stop-Loss (TP/SL)**\
  A toggle that allows you to attach exit levels to your trade when placing the order. Enter a target price to automatically close for profit, or a stop price to cap losses.

***
