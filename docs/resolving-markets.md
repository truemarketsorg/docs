---
sidebar_position: 5
---

# Resolving markets

### Resolvers <a href="#resolvers" id="resolvers"></a>

After a market has been created, it may be resolved at anytime if the criteria defined in the market description has been met. The market description will contain a set of rules by which the market can be resolved. These rules will be referenced against the market source field to verify whether a market is resolvable or not.&#x20;

\*Note:  Markets should be primarily referenced against their listed sources for resolution, however, markets can also be resolved using alternative sources if the listed sources are otherwise unreliable (due to being faulty, offline, or in light of new provable data, etc). &#x20;

Based on the rules of resolution in a market description, anyone is allowed to determine whether the market question has been answered and permissionlessly propose a resolution by posting a bond behind their selected outcome.

This process initiates a twelve hour challenge window during which anyone can dispute the proposed resolution.

If the conditions necessary to resolve a market have indeed been met, and there are no disputes, the market will successfully resolve to the proposed outcome at the end of the challenge period.

By resolving a market correctly to YES or NO, resolvers receive a reward from the protocol based on the pre-defined `_rewardAmount`  for that market. The reward and bond pledged by the resolver is automatically released to them in the initial redemption transaction, which can be executed by anyone who redeems YES or NO tokens.

![](/img/resolving-markets.png)

The resolver role is completely permissionless and open to the community. Anybody that's observing the real-world events surrounding a market, who thinks the market question has been answered, can post a bond and propose a resolution.

If the market question has _not_ been answered, and the market is _not_ resolvable based on the rules in its description, the resolver's bond will be subject to slashing by the oracle council and the market status will be reset to undecided.

If the market has resolved by the proposed resolution is incorrect, the resolver's bond will again be subject to slashing by the oracle council and the market result will be set to the correct outcome.

It is trivial to verify whether a resolution is legitimate or not by checking the cited sources in the market and seeing if they match the claim. If they do not match up, the maliciously proposed resolution will be slashed and the disputer will receive a reward.

The more tricky case occurs when the proposed resolution and the dispute both have merit. In such instances (which do occasionally occur due to the inherent nature of prediction markets), neither party will be subject to slashing and the enshrined oracle will come to consensus on the "true" market outcome (pun intended).

### Cancelled markets <a href="#cancelled-markets" id="cancelled-markets"></a>

The overwhelming majority of resolutions will result in YES or NO outcomes. In the odd case, however, there's a chance that the event that a market is based upon gets cancelled, or more commonly, an event results in a draw. In these cases, the appropriate resolution to be proposed is `cancelled`.

If a market is successfully cancelled, all YES and NO tokens are redeemable for their minted value (50c). The cancellation of a market, unless it ends in a draw, is an unwelcome event for prediction markets because users whose tokens were priced at a greater probability than 50%, and who end up losing that upside.

Given these dynamics, a `cancelled` outcome should only be proposed in very specific circumstances, or in the event of a Draw, and doing so outside of those situations will result in the resolver's bond being slashed.

Even more trivial than verifying a YES/NO outcome, is verifying whether an event has indeed been cancelled or has ended in a draw. Thus, resolutions that propose to cancel a market incorrectly, face zero leniency when being slashed.&#x20;

For more info on this subject see the Bonds and Slashing section.

