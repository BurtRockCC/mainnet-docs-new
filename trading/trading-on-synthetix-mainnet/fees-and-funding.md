# Fees and Funding

Trading on Synthetix Mainnet involves several types of fees and periodic payments that help maintain the health of the system and keep perp markets aligned with their underlying assets. This section explains how trading fees work, how funding is applied between longs and shorts, what liquidation costs look like, and how slippage may affect your execution.

### Trading Fees

Every order pays a trading fee, which depends on whether the order adds or removes liquidity from the orderbook.

* **Maker Fee** – Applied when your order _adds_ liquidity by sitting on the book before filling.
* **Taker Fee** – Applied when your order _removes_ liquidity by executing immediately against existing orders.

**Example:**\
Maker Fee: 0.02%\
Taker Fee: 0.05%

You place a **limit buy** for 1 ETH at $3,000, and it sits on the orderbook until matched.\
Fee = $0.60 (1 ETH × $3,000 × 0.02%).

You place a **market buy** for 1 ETH at $3,000, and it fills instantly.\
Fee = $1.50 (1 ETH × $3,000 × 0.05%).

### Funding Rates

Perpetual futures use funding to keep prices in line with the spot market. Funding is a recurring payment between longs and shorts based on the difference between the perp’s mark price and the index price of the underlying asset.

* Funding is paid **every 8 hours** on most assets.
* **Positive funding** → longs pay shorts.
* **Negative funding** → shorts pay longs.

**Example:**\
A trader opens a $20,000 BTC long while the funding rate is +0.01% per 8 hours.\
Funding = $20,000 × 0.0001 = $2 every 8h.\
If the rate stays constant for 24h, the trader pays $6 total.

#### Funding Caps and Impact Prices

| Market                     | Funding Cap/Floor (per 8h) | Funding Rate Impact Price |
| -------------------------- | -------------------------- | ------------------------- |
| BTC, ETH                   | ±1.20%                     | 20,000 USDT               |
| SOL, BNB, XRP              | ±1.50%                     | 5,000 USDT                |
| DOGE                       | ±1.50%                     | 5,000 USDT                |
| SUI, ENA, kPEPE, SNX, HYPE | ±1.50%                     | 5,000 USDT                |

### Liquidation Clearance Fee

When your position is liquidated, an additional fee is charged on the notional value of the position. This is the **Liquidation Clearance Fee**, and it compensates the protocol for managing liquidations and ensures solvency of the system.

* Applied as a % of notional (varies by market, e.g., 1.25%–1.5%).
* Deducted automatically when liquidation occurs.
* Displayed in your transaction history as **“Liquidation Clearance.”**

#### Liquidation Fees by Market

| Market   | Liquidation Clearance Fee |
| -------- | ------------------------- |
| BTCUSD   | 1.25%                     |
| ETHUSD   | 1.25%                     |
| SOLUSD   | 1.50%                     |
| BNBUSD   | 1.25%                     |
| XRPUSD   | 1.25%                     |
| DOGEUSD  | 1.50%                     |
| SUIUSD   | 1.50%                     |
| ENAUSD   | 1.50%                     |
| kPEPEUSD | 1.50%                     |
| SNXUSD   | 1.50%                     |
| HYPEUSD  | 1.50%                     |

### Slippage and Price Protections

Large orders can cause **price impact** by consuming available liquidity on the orderbook. To protect traders, several safeguards are in place:

* **Order Confirmation** – Displayed before orders are sent to the market, allowing traders to review size and expected price impact before finalizing the order.
* **Limit Order Price Cap/Floor Ratio** – Ensures that limit buy prices cannot exceed a set % above mark price, and limit sell prices cannot fall below a set % below mark price.
* **Market Order Price Cap/Floor Ratio** – In extreme volatility, market orders may only fill within a defined % range. Orders outside this range may partially fill or expire.

#### Price Protection Parameters

| Market   | Limit Order Cap/Floor Ratio | Market Order Cap/Floor Ratio |
| -------- | --------------------------- | ---------------------------- |
| BTCUSD   | 5% / 5%                     | 5%                           |
| ETHUSD   | 5% / 5%                     | 5%                           |
| SOLUSD   | 5% / 5%                     | 5%                           |
| BNBUSD   | 5% / 5%                     | 5%                           |
| XRPUSD   | 5% / 5%                     | 5%                           |
| DOGEUSD  | 10% / 10%                   | 10%                          |
| SUIUSD   | 15% / 15%                   | 15%                          |
| ENAUSD   | 15% / 15%                   | 15%                          |
| kPEPEUSD | 15% / 15%                   | 15%                          |
| SNXUSD   | 15% / 15%                   | 15%                          |
| HYPEUSD  | 15% / 15%                   | 15%                          |
