# Tokens

## SNX
SNX is the governance and utility token of the Synthetix protocol. It is used to vote for governance council members in elections and can be staked to earn SNX rewards. Staked SNX backs Synthetix products.

SNX staking is available on Ethereum Mainnet. Some legacy stakers may participate in the Debt Jubilee on Optimism with their staked SNX tokens, however all new products will be available only on Ethereum Mainnet. Those with tokens on other networks who are not participating in the debt jubilee on Optimism are encouraged to bridge back to Ethereum Mainnet as we deprecate old products.

- [SNX on CoinGecko](https://www.coingecko.com/en/coins/synthetix-network-token)

## sUSD and Stablecoins
- **sUSD** is the primary over-collateralized stablecoin of the Synthetix ecosystem. It is available on Ethereum Mainnet for staking and LPing, and is available on Optimism for trading on Perps v2 (now closed to new users) and settling legacy Debt Jubilee positions.
  - [sUSD on CoinGecko](https://www.coingecko.com/en/coins/susd)

### Bridging sUSD

sUSD can only be bridged between Ethereum Mainnet and Optimism using the official Synthetix bridge interface. Since we are deprecating Optimism products, users should only be bridging **from Optimism back to Mainnet** at this time.

#### How to Bridge sUSD

**Step 1: Visit the Bridge Interface**
1. Go to [legacy-staking.synthetix.io/bridge](https://legacy-staking.synthetix.io/bridge)
2. Connect your wallet and ensure you have sUSD on Optimism

**Step 2: Choose Native Bridge**
- Select **"Native Bridge"** (not Instant Bridge)
- This is the official Synthetix bridge with no fees and no slippage
- The Instant Bridge option is a third-party service and should not be used for sUSD

**Step 3: Configure Your Bridge**
- **From**: Optimism (source network)
- **To**: Ethereum Mainnet (destination network)
- **Asset**: sUSD
- **Amount**: Enter the amount you wish to bridge
- **Acknowledge**: Check the box confirming you understand the 7-day delay

**Step 4: Initiate the Bridge**
- Click "Bridge" to start the withdrawal process
- Confirm the transaction in your wallet

**Step 5: Complete Two-Step Withdrawal Process**

The bridge uses Optimism's two-step withdrawal process for security:

1. **Initiate withdrawal** ✅ (completed when you click "Bridge")
2. **Wait a few minutes** for proving to become available ⏰
3. **Prove withdrawal** on Ethereum L1:
   - Visit [Optimistic Etherscan Message Relayer](https://optimistic.etherscan.io/messagerelayer)
   - Enter your Optimism transaction ID to find your pending bridge transaction
   - Complete the prove withdrawal step on Ethereum L1 with the same wallet
4. **Wait 7 days** for the challenge window ⏰
5. **Claim withdrawal** on Ethereum L1:
   - Return to the [Message Relayer](https://optimistic.etherscan.io/messagerelayer)
   - Enter your transaction ID again
   - Complete the finalize withdrawal step

#### Important Notes

- **Only bridge from Optimism to Mainnet** - we are deprecating Optimism products
- **Use Native Bridge only** - do not use Instant Bridge or third-party bridges
- **7-day delay** applies when bridging from Optimism to Ethereum Mainnet
- **No fees and no slippage** with the Native Bridge
- **Same wallet required** - use the same wallet for both Optimism and Ethereum transactions

{% hint style="warning" %}
Always use the official Synthetix bridge interface at [legacy-staking.synthetix.io/bridge](https://legacy-staking.synthetix.io/bridge) and the [Optimistic Etherscan Message Relayer](https://optimistic.etherscan.io/messagerelayer) for completing withdrawal steps. Third-party bridges are not supported for sUSD.
{% endhint %}

#### Additional Resources

- [OP Labs Blog: Two-Step Withdrawals](https://blog.oplabs.co/two-step-withdrawals/) - Technical details about the withdrawal process
- [Optimistic Etherscan Message Relayer](https://optimistic.etherscan.io/messagerelayer) - Tool for proving and finalizing withdrawals



- **snxUSD (v3)** was a previous stablecoin for Synthetix v3 and is now deprecated.
- **USDx** was a stablecoin on Arbitrum, now deprecated along with the Arbitrum V3 deployment.

