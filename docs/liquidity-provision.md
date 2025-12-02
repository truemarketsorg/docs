---
sidebar_position: 3
---

# Liquidity Provision

## Minting YES/NO tokens <a href="#liquidity-provision" id="liquidity-provision"></a>

In Truemarkets, anyone can permissionlessly mint YES and NO tokens for a market once it is initialized. This opens the door for the free market to drive the supply of YES and NO tokens.

Anyone can mint YES and NO tokens after a market is deployed by depositing USDC into the market. For every 1 USDC that is deposited, 1 YES and 1 NO token is minted. Conversely, 1 YES and 1 NO token can always be redeemed together for 1 USDC.

Once a market has been resolved, the YES or NO token corresponding to the correct outcome can be redeemed for 1 USDC each, while the opposing token expires worthless.

Every market has a corresponding YES-USDC pool and NO-USDC Uniswap pool. Although there aren’t any bounds on the range of liquidity, the price of YES or NO tokens should never go above $1, because that is the maximum redeemable value for each token.

The basic strategy for an LP is to mint YES and NO tokens, then sell off the tokens that they forecast will result in the losing outcome.

Remember, at the time of resolution one of the two tokens will expire worthless, so in this strategy, an LP's job is to sell the token that they think will be worthless and retain the one they believe corresponds to the correct outcome.

Another simple strategy is to mint both YES and NO tokens, but attempt to retain an equal number of YES and NO tokens (while providing liquidity) at all times. In this strategy, an LP would like to remain delta-neutral while market making to ensure that they can redeem their USDC in full regardless of outcome.

## LP tutorial&#x20;

To mint YES and NO tokens, users simply approve their USDC and mint 1 YES and 1 NO token for every 1 USDC deposited.

![](/img/liquidity-provision-1.png)

Once a user mints their tokens, they can now position them on the order book.

In the image below, the user is placing their 300 YES tokens (minted in the step before) on the order book, between the spot price and $0.25 USDC.&#x20;

![](/img/liquidity-provision-2.png)

At the current price (\~$0.20), the user's entire position, once deposited, is in YES tokens. If the price were to reach $0.25, the user's entire position would be composed of USDC. As the price of YES tokens fluctuate in the range between $0.20 and $0.25, the user's LP position would be a mixed composition of YES and USDC tokens.&#x20;

At anytime, users are free to withdraw their LP position and its composing tokens. Which means users can also manually execute limit orders by removing liquidity once it enters or passes their desired range.

In the graphic below, the user is providing USDC in a range that begins right at the spot price and ends at the bottom of the price curve.  Effectively, in that range, the user is purchasing YES tokens at every price below the current price, all the way down to zero.

![](/img/liquidity-provision-3.png)

Users can withdraw their liquidity and lock in the composition of their holdings at any given moment. Conversely, users can leave their liquidity in the pool (in a state of  constant flux) with their position churning as the price fluctuates.

## Active liquidity

Passively providing liquidity to prediction markets is tricky business. Markets that don't have long dated expiries with predictable resolution dates are the trickiest of all. These markets can spontaneously resolve or see significant price changes out of the blue.&#x20;

In these cases, LPs that still have liquidity on the order book would be the losing counter parties to spontaneous repricing events. For this reason, all of the onchain LP incentives will be targeted at active liquidity providers who have liquidity within the active ticks.

This design will incentivize users to tighten the bid/ask spread when providing liquidity and to monitor the markets they are LPing to.

