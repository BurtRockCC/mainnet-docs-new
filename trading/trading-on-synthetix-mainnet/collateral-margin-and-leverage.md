# Collateral, Margin and Leverage

Margin and leverage define the foundation of trading on Synthetix Mainnet. Your collateral determines how large a position you can open, how risk is managed, and what happens if the market moves against you. This section explains how margin types work, how leverage is applied, the role of collateral, and the mechanics of liquidation.

### Supported Collateral

Synthetix supports multiple collateral types at launch. Each type of collateral is subject to a haircut, which discounts its effective value to account for volatility and liquidity risk.

| Assets                  | Tier (USD)              | Collateral Value Ratio | Haircut | Collateral Value Addition |
| ----------------------- | ----------------------- | ---------------------- | ------- | ------------------------- |
| **USDT**                | < 500,000,000           | 100%                   | 0%      | –                         |
| **sUSDe**               | 0 – 5,000,000           | 99%                    | 1%      | –                         |
|                         | 5,000,000 – 20,000,000  | 98%                    | 2%      | 50,000 USDT               |
|                         | 20,000,000 – 50,000,000 | 95%                    | 5%      | 450,000 USDT              |
| **cbBTC, WETH, wstETH** | 0 – 2,500,000           | 99%                    | 1%      | –                         |
|                         | 2,500,000 – 10,000,000  | 97%                    | 3%      | 25,000 USDT               |
|                         | 10,000,000 – 25,000,000 | 95%                    | 5%      | 325,000 USDT              |

* **Haircuts** reduce how much of your deposited collateral counts toward margin.
  * Example: If wstETH has a 5% haircut and you deposit $10,000, only $9,500 is credited toward your margin balance.
* Collateral Value Addition (CVA) formulas apply to tiered deposits, ensuring caps and discounts are applied consistently.

#### Global Deposit Caps

| Asset               | Value (USD) |
| ------------------- | ----------- |
| USDT                | 20,000,000  |
| sUSDe               | 10,000,000  |
| cbBTC, WETH, wstETH | 2,500,000   |

#### Minimum Deposit Amounts

| Asset  | Minimum Deposit |
| ------ | --------------- |
| USDT   | 100             |
| sUSDe  | 100             |
| cbBTC  | 0.001           |
| wstETH | 0.01            |
| WETH   | 0.01            |

### Margin Types

* **Cross Margin** – Collateral is pooled across your account. All open positions share the same margin. Gains on one position can offset losses on another, but liquidation risk is also shared.
* **Isolated Margin** – Collateral is tied to a single position. Only that position is at risk, but your available margin is capped to the collateral assigned.

### Initial and Maintenance Margin

* **Initial Margin (IM)** – The amount of collateral required to open a position. Larger trades and higher leverage require more IM.
* **Maintenance Margin (MM)** – The minimum equity required to keep positions open. If equity falls below MM, liquidation is triggered.
* **Formula** – IMR = 2 × MMR, at minimum.

**Example**\
A trader opens a $10,000 BTC long with 10x leverage.

* Initial Margin = $1,000 (10%).
* Maintenance Margin = $50 (0.5%).
* If equity drops below $50, liquidation occurs.

### Leverage

Leverage allows traders to control positions larger than their collateral.

* Maximum leverage depends on the asset. Major markets like BTC and ETH support higher caps (up to 100x at small sizes, scaling down as size increases).
* Smaller-cap markets support less leverage at size.
* Effective leverage also depends on collateral type — assets with haircuts reduce usable margin, lowering leverage in practice.

#### Leverage Limits and Maintenance Margin Rates

**BTC**

| Position Size (USDT)      | Max Leverage | Default Leverage | Maintenance Margin Rate | Maintenance Deduction |
| ------------------------- | ------------ | ---------------- | ----------------------- | --------------------- |
| 0 – 1,000,000             | 100x         | 20x              | 0.50%                   | 0                     |
| 1,000,001 – 50,000,000    | 50x          | –                | 1.00%                   | 5,000                 |
| 50,000,001 – 150,000,000  | 25x          | –                | 2.00%                   | 505,000               |
| 150,000,001 – 300,000,000 | 10x          | –                | 5.00%                   | 5,005,000             |
| 300,000,001+              | 2x           | –                | 25.00%                  | 65,005,000            |

**ETH**

| Position Size (USDT)     | Max Leverage | Default Leverage | Maintenance Margin Rate | Maintenance Deduction |
| ------------------------ | ------------ | ---------------- | ----------------------- | --------------------- |
| 0 – 500,000              | 100x         | 20x              | 0.50%                   | –                     |
| 500,001 – 20,000,000     | 50x          | –                | 1.00%                   | 2,500                 |
| 20,000,001 – 80,000,000  | 25x          | –                | 2.00%                   | 202,500               |
| 80,000,001 – 250,000,000 | 10x          | –                | 5.00%                   | 2,602,500             |
| 250,000,001+             | 2x           | –                | 25.00%                  | 52,602,500            |

**SOL, BNB, XRP**

(similar tiering: 100x at small notional → 2x at very large notional, with MM scaling 0.5% → 25%).

**DOGE, SUI, ENA, kPEPE, SNX, HYPE**

(similar tiering but smaller notional caps).

***

### Liquidation

Liquidation occurs when account equity falls below Maintenance Margin. At liquidation:

1. Margin ratio is checked and liquidation is triggered.
2. If collateral is not in USDT, auto-exchange converts assets into USDT to settle debt (starting with the asset with the highest haircut).
3. The liquidated position and seized collateral are transferred to the SLP vault.
4. A **Liquidation Clearance Fee** is applied, calculated on notional size.
5. The vault closes the position on the market.

#### Liquidation Clearance Fee

* Applied to the **notional value** of the liquidated position.
* Varies by market, e.g.:
  * BTC/ETH – **1.25%**
  * SOL, XRP, SNX, others – **1.5%**
* Displayed as “Liquidation Clearance” in your account history.

#### Cross vs. Isolated

* **Cross Margin** – If the account falls below MM, all positions are liquidated together.
* **Isolated Margin** – Only the isolated position is liquidated; the rest of your balance remains available.

#### Examples

**Cross Margin Example**

* Deposit: $10,000 USDT
* Positions: +1 BTC long (IM = $6,000), -10 ETH short (IM = $4,000).
* BTC loses $5,000 → equity = $5,000. Both positions remain open but liquidation risk is high.
* If equity falls below MM, both positions are liquidated together.

**Isolated Margin Example**

* Deposit: $10,000 USDT
* Position: $6,000 BTC long in isolated mode.
* BTC loses $6,000 → position equity = $0.
* That position is liquidated, but $4,000 remains in the account.

***

### Auto-Borrow

If you use non-USDT collateral and close a trade with negative PnL, the system may create a **negative USDT balance**.

* Borrow interest accrues at **10.95% annually**, calculated hourly.
* The debt remains until repaid or covered via auto-exchange.

***

### Auto-Exchange

The auto-exchange system protects the protocol and ensures losses are settled.

Triggers include:

* Negative USDT balance breaches borrow limits.
* Loan exceeds allowed Loan-to-Value (LTV).
* Closing a losing trade without enough USDT to cover PnL.
* During liquidation (starting with highest haircut collateral).

#### LTV Caps

| Asset  | LLTV | LTV  |
| ------ | ---- | ---- |
| USDT   | 100% | 100% |
| sUSDe  | 95%  | 90%  |
| cbBTC  | 80%  | 60%  |
| wstETH | 80%  | 60%  |
| WETH   | 80%  | 60%  |

#### Haircuts on Exchange

* **Forced Auto-Exchange Fee** = 2 × lowest tier CVH.
* **Voluntary Auto-Exchange Fee** = lowest tier CVH.

**Example – Multiple Collateral**

* Deposit: $10k cbBTC and $10k wstETH.
* Loss: -$15k PnL.
* cbBTC (higher haircut) exchanged first: $10k.
* Remaining $5k loss covered with wstETH.
* Final balance ≈ $5k wstETH.
