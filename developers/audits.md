# Audits

Synthetix has been audited extensively by several security specialists: Macro, Iosiro, Omniscia, 0xCommit, and other highly respected independent auditors.

The latest audits of any Synthetix smart contracts can be found below or within respective GitHub repositories.

## Bug Bounty Program

Synthetix has a bug bounty program administered by [Immunefi](https://immunefi.com/bug-bounty/synthetix/) with up to $100,000 in rewards.

## Live Products Audits

### 420 Pool (SIP-420) - Protocol Managed Staking

The 420 Pool represents Synthetix's transition from self-staking to delegated staking, where the protocol manages debt and deploys capital across DeFi protocols to generate yield.

**Key Features:**
- Protocol-managed debt at 200% c-ratio
- Yield generation across Ethena, Aave, Maker, and Berachain Boyco Vaults
- Simple Staking for new users without debt
- Debt Jubilee for legacy stakers with debt forgiveness

**Audit Status:** Audit information for the 420 Pool contracts is not currently available in the documentation. The contracts are live on Ethereum Mainnet.

### Debt Jubilee Contracts

The Debt Jubilee allows existing SNX stakers to burn their outstanding debt over 12 months through the 420 Pool.

**Key Features:**
- Linear debt forgiveness over 12 months
- 20% sUSD requirement for participants
- Early exit penalties
- Integration with 420 Pool

**Audit Status:** Audit information for the Debt Jubilee contracts is not currently available in the documentation.

### Core Tokens

#### SNX Token
- **Contract:** [0xC011a73ee8576Fb46F5E1c5751cA3B9Fe0af2a6f](https://etherscan.io/token/0xC011a73ee8576Fb46F5E1c5751cA3B9Fe0af2a6f)
- **Audit Status:** The SNX token contract has been extensively audited and is live on Ethereum Mainnet

#### sUSD Stablecoin
- **Contract:** [0x57Ab1ec28D129707052df4dF418D58a2D46d5f51](https://etherscan.io/token/0x57Ab1ec28D129707052df4dF418D58a2D46d5f51)
- **Audit Status:** The sUSD stablecoin contract has been extensively audited and is live on Ethereum Mainnet

## Legacy Product Audits (Deprecated)

### Smart Margin v3 Audits

The following audit reports are available in the [Smart Margin v3 GitHub repository](https://github.com/Kwenta/smart-margin-v3/tree/main/audits/external/v3.0.0):

#### External Audits
- [Kwenta A-11 Audit Report](https://github.com/Kwenta/smart-margin-v3/blob/main/audits/external/v3.0.0/Kwenta%20A-11.pdf)
- [Kwenta SMv3 Guhu Audit](https://github.com/Kwenta/smart-margin-v3/blob/main/audits/external/v3.0.0/kwenta-smv3-guhu.md)
- [Omniscia Audit Report - September 19, 2023](https://github.com/Kwenta/smart-margin-v3/blob/main/audits/external/v3.0.0/09192023_Omniscia_Audit_Kwenta_SmartMarginV3.pdf)
- [Kwenta A-8 Macro Audits Report](https://github.com/Kwenta/smart-margin-v3/blob/main/audits/external/v3.0.0/Kwenta%20A-8%20%7C%20Macro%20Audits%20%7C%20The%200xMacro%20Library.pdf)

#### Internal Audits
- [Kwenta Mentorship Internal Audit](https://github.com/Kwenta/smart-margin-v3/blob/main/audits/internal/v3.0.0/kwenta-mentorship-internal-audit.md)

### SCW-Contracts Audits

The following audit report is available in the [SCW-Contracts GitHub repository](https://github.com/Kwenta/scw-contracts/tree/main/audits):

- [0xCommit Audit Report](https://github.com/Kwenta/scw-contracts/blob/main/audits/0xCommit.pdf)

## Additional Resources

For more detailed information about audits, visit the [Synthetix V3 Developer Documentation](https://docs.synthetix.io/v/v3/for-developers/smart-contract-audits). 