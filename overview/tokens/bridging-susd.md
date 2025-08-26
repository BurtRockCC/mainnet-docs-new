# Bridging sUSD

## How to Bridge sUSD from Optimism to Ethereum Mainnet (via Superbridge)

All sUSD products and liquidity incentives on Optimism are deprecated. It’s recommended to move any remaining sUSD to Ethereum Mainnet. See: [Mainnet is Where the Heart Is](https://blog.synthetix.io/mainnet-is-where-the-heart-is/).

sUSD can be bridged from OP to ETH on Superbridge:\
[superbridge.app/?fromChainId=10\&toChainId=1\&tokenAddress=0x8c6f28f2F1A3C87F0f938b96d27520d9751ec8d9](https://superbridge.app/?fromChainId=10\&toChainId=1\&tokenAddress=0x8c6f28f2F1A3C87F0f938b96d27520d9751ec8d9)

### Before you start

**Superbridge usees the native Optimism bridge, enabling 0 slippage, and no bridging fees. Please be aware that bridging using the native Optimism bridge takes 7 fees, and requires 3 transactions, including 2 transactions on Ethereum Mainnet which may be gas intensive. Once the bridging process has begun, it cannot be canceled or reversed.**

**If you're ready to start bridging, follow the steps below:**

<figure><img src="../.gitbook/assets/Screenshot 2025-08-26 at 2.38.11 AM (1).png" alt=""><figcaption></figcaption></figure>

### Step 1 — Initiate the bridge (on Optimism)

1. Open the [Superbridge app](https://superbridge.app/?fromChainId=10\&toChainId=1\&tokenAddress=0x8c6f28f2F1A3C87F0f938b96d27520d9751ec8d9) and **connect your wallet**.
2. **Select amount** of **sUSD** to bridge (or **Max**).
3. Select **Native Bridge** and verify you are bridging **From: OP Mainnet → To: Ethereum**.
4. **Confirm details**, click **Continue**, and **confirm the transaction in your wallet on Optimism**.
5. **Wait \~1 hour.** You can close the page and return later; bring up pending actions by selecting the clock icon at the top of the page when you reconnect (next to the settings wheel).

<figure><img src="../.gitbook/assets/Screenshot 2025-08-26 at 2.46.44 AM (1).png" alt=""><figcaption></figcaption></figure>

### Step 2 — Prove on Ethereum (\~1 hour later)

1. Return to Superbridge and **switch your wallet to Ethereum Mainnet**.
2. Click the **clock icon** (pending actions), select your withdrawal, and click **Prove**.
3. **Approve the Ethereum transaction** (requires ETH for gas).
4. Wait **\~7 days.**

### Step 3 — Finalize on Ethereum (\~7 days later)

1. Return to Superbridge on **Ethereum Mainnet**.
2. Open **pending actions** (clock icon), select your withdrawal, and click **Get**.
3. **Approve the Ethereum transaction** (requires ETH for gas).
4. Your **sUSD is now on Ethereum Mainnet**.
