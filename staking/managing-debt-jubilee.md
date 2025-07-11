# Managing Debt Jubilee and Legacy Staking Positions

As of April 2025, the 420 Pool has replaced all previous SNX staking mechanisms. Stakers no longer manage individual debt positions, and debt is now managed by the protocol. If you previously migrated to the 420 Pool under the Debt Jubilee, or were force-migrated due to recent changes to liquidation thresholds, this page will help you manage your position.

***

### The End of Solo Staking

Solo staking [has been deprecated](https://blog.synthetix.io/the-end-of-solo-staking/). As part of the transition, liquidation thresholds were progressively raised to migrate all remaining stakers into the 420 Pool. If your position was below 160% c-ratio and you did not migrate, it was liquidated as part of this process.

{% hint style="info" %}
**Important:** Liquidated SNX positions are recoverable for a period of **6 months**. If your account was liquidated and you wish to reclaim your SNX and sUSD, contact the Synthetix Treasury on Discord with your wallet address.
{% endhint %}

* [Join Discord](https://discord.gg/synthetix) and create a ticket to claim your position. If you need assistance joining Discord, you may reach out through Twitter or Telegram.

***

### Managing a Debt Jubilee Position

If you migrated your position to the 420 Pool during the Debt Jubilee period (March–April 2025), your debt began reducing linearly over 12 months.

{% hint style="info" %}
All Debt Jubilee participants are required to stake sUSD equal to 20% of your initial debt. If you do not meet this requirement, your debt forgiveness will be paused. See [the blog](../../) for more information.
{% endhint %}

#### Here's how the Debt Jubilee Works:

* Your SNX was automatically delegated to the 420 Pool.
* Your debt is burning linearly: 50% after 6 months, 100% after 12 months.
* You cannot be liquidated.
* Once 12 months have passed, your debt reaches 0, and your SNX is fully unlocked.
* SNX rewards for Simple Staking are not provided to Debt Jubilee Participants. You may repay your debt any time to transition to Simple Staking.

<figure><img src="../../.gitbook/assets/uiburnsuccessfuldebtview.png" alt=""><figcaption><p>Once deposited, monitor the progress of your debt burn</p></figcaption></figure>

#### Exiting Early:

You can unstake at any time by withdrawing your SNX. However:

* A **7-day cooldown** applies before you can claim your SNX.
* If you exit before your debt is fully burned, you must **repay the remaining debt** after subtracting any burned amount and applying the **early exit penalty**.
* The **early exit penalty** applies only to the % of debt reduced. You can never owe more debt than when you entered the pool.

{% hint style="info" %}
Early Exit Example 1: Enter the 420 Pool with $1000 of debt and withdraw after 6 months

* Initial Debt: $1000
* Debt forgiven: $500
* Early withdrawal penalty on debt forgiven: 50% + 25%
* Debt needed to repay in order to exit: $875



Early Exit Example 2: Enter the 420 Pool with $1000 of debt and withdraw after 9 months

* Initial Debt: $1000
* Debt forgiven: $750
* Early withdrawal penalty on debt forgiven: 50% + 12.5%
* Debt needed to repay in order to exit: $718.75
{% endhint %} 