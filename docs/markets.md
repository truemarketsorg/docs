---
sidebar_position: 4
---

# Markets

## Life cycle <a href="#life-cycle" id="life-cycle"></a>

The life cycle of a market starts with its creation.&#x20;

In the early days of the project, market creation is delegated to whitelisted addresses and AI agents that generate them using the market creation guidelines. These actors are part of the Oracle Council, which is also responsible for arbitrating low level disputes.

After a market is initialized, users can begin minting YES/NO tokens to provide liquidity and trade with.

Once the market question has been satisfied,  markets can be permissionlessly resolved by anyone willing to pledge a bond behind their proposed resolution.

Truemarkets resolves outcomes using an _optimistic_ oracle, meaning that in the ideal case, resolutions are "optimistically" considered valid unless otherwise disputed.

When a resolution is proposed, a challenge window begins during which anyone can dispute the proposed resolution. If a dispute does not occur during this time, the market successfully resolves and users can redeem their YES or NO tokens for USDC.

## Market Contents <a href="#market-contents" id="market-contents"></a>

Every market contains three `strings` that exist onchain inside of the market creation transaction.

`_marketQuestion` - string representing the market question

`_marketSource` - the source through which the market rules are expected to be verified (this field can also contain URLs referencing the exact sources that must be used).

`_additionalInfo` - the market description and rules of resolution.

All of the market defining strings can be easily identified and read on etherscan. Below is an example market creation transaction for Fed interest rates in November 2024:

![](/img/markets.jpg)

One of the advantages of using onchain strings for market questions and descriptions, is that these strings can never be altered once a market has been initiated. This approach provides strong immutable guarantees regarding the subject of disputes, enabling a highly credible resolution process that is not subject to retroactive rule changes.

Each market also has a set of parameters based on its inherent properties:

`_endOfTrading` is the earliest timestamp that a market can be resolved.

`_yesNoTokenCap` represents a potential discretionary cap for a market.

`_rewardToken` address of the token that will be used to incentivize resolvers or disputers for that market (either TRUE or USDC).

`_rewardAmount` the amount of tokens to be paid for resolving the market.



## Fees

In Truemarkets, all markets have configurable fees that go to the protocol and the market creator upon successful resolution. Initially, these fees will be set to negligible levels since market creation is limited to whitelisted actors. However, as the app enables permissionless market creation, applying these fees will be essential for the protocol and oracle to function securely.
