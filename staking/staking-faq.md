# Staking FAQ

#### What is the 420 Pool?

The 420 Pool is the new unified staking system for SNX. It allows SNX holders to stake into a protocol-managed pool that earns yield from Synthetix and external integrations. This replaces legacy solo staking, and there are no liquidations, c-ratios, or debt management required. Simply stake and start earning.

Staking is currently supported on **Ethereum Mainnet** for new users. Legacy stakers who entered during the Debt Jubilee may still manage their positions on **Optimism** by switching the network in the UI.

***

### **Simple Staking (New Stakers)**

#### What is Simple SNX Staking?

Simple Staking is a new mode within the 420 Pool for SNX holders **without existing debt**. It allows users to earn pro-rata SNX rewards over 12 months, without managing debt or a c-ratio. Rewards begin unlocking after the 12-month period and vest linearly over 3 months.

#### What are the penalties for early exit?

If you exit early, you forfeit a portion of your earned SNX rewards. The penalty starts at 100% and decreases linearly to 0% by the end of the 12 month program. Only earned rewards are charged a penalty, and you can withdraw your full principal at any time after a 7-day cooldown.

#### How do I switch from Jubilee to Simple Staking?

To move from the Debt Jubilee to Simple Staking, you must **repay all remaining debt**. Once cleared, you can re-enter the pool under the Simple Staking configuration.

***

### **Debt Jubilee (Legacy Stakers)**

#### What is the Debt Jubilee?

The Debt Jubilee offers existing SNX stakers the opportunity to burn their outstanding debt over 12 months. Stakers who migrated into the 420 Pool during the Jubilee window are eligible. Debt is forgiven linearly, with 50% forgiven at the 6-month mark and 100% at 12 months.

#### What is the sUSD requirement for Jubilee participants?

To remain eligible for debt forgiveness, Jubilee participants must maintain a **minimum sUSD balance equal to 20% of their original debt**. This sUSD must remain in the wallet associated with the staking position. If the ratio drops below 20%, the Jubilee clock pauses. Once the ratio is restored, forgiveness resumes. It is **not possible** to fall out of compliance once the threshold has been reached.

#### Can I leave during the Jubilee period?

Yes, but you’ll be required to **repay any remaining debt**, adjusted for partial forgiveness and the early exit penalty, before your SNX can be withdrawn.

#### What is the early exit penalty? (Debt Jubilee Only, Simple Stakers see above)

Jubilee participants who exit early forfeit a portion of their debt forgiveness. The penalty starts at 100% on day one and decreases linearly to 50% by day 365. For example, leaving halfway through the year results in a 75% effective debt relief instead of 50%.

#### What happens if I have escrowed SNX?

Legacy escrowed SNX continues to vest on its original schedule and cannot be withdrawn before it matures, even if you migrate into the 420 Pool. Find your legacy escrow at [https://legacy-staking.synthetix.io/](https://legacy-staking.synthetix.io/).

***

### **Yield & Distributions**

#### How does the 420 Pool earn yield?

The protocol can mint sUSD against SNX collateral at a 200% c-ratio and deploy it to earn yield across platforms like **Ethena, Aave, Maker, and Berachain Boyco Vaults**, as well as to bootstrap liquidity for Synthetix products.

#### Who receives the yield?

SNX stakers. Yield is distributed pro-rata based on your share of the pool. If you hold 1% of the staked SNX, you are entitled to 1% of the distributed yield.

#### How often is yield distributed?

Distribution timing is not fixed and will occur periodically. The mechanism will be transparent, and distributions may include stablecoins, SNX buybacks, or additional protocol-managed rewards.

***

### **Mechanics & Safety**

#### Are stakers locked in?

There is no hard lock, but **withdrawing SNX requires a 7-day cooldown**. You can initiate an exit at any time, subject to the terms of your staking mode (Jubilee or Simple).

#### Can I be liquidated?

No. There are **no liquidations** in the 420 Pool. That’s part of what makes it a safer and simpler way to stake SNX. 