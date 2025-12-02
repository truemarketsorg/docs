---
sidebar_position: 6
---

# Disputing outcomes

In Truemarkets, disputers are basically the same participants as resolvers. Anyone who disagrees with a proposed outcome, can dispute it during the challenge window after it is proposed.

Disputers play a particularly critical role in Truemarkets, they are the stewards of truth.&#x20;

Disputers are the first line of defence for the protocol. They prevent manipulation and ensure that the oracle operates orderly.

By posting a bond equal to that of the resolver, anyone can call the `openDispute` function on a resolution-pending market and provide a `_disputeString` containing the reasons for their dispute.

If the challenge is accepted, the disputer's bond is released and they receive a reward for the successful dispute.

Below is an example image of the data in a dispute transaction on etherscan:

![](/img/disputing-outcomes-1.png)

There are three stages of arbitration in Truemarkets, with each escalation being prompted by a dispute.

To challenge an initial proposal, a small bond is required. To dispute an Oracle Council decision, a larger bond must be pledged. Finally, in order to dispute a token holder vote, a wallet with at least 250,000 TRUE tokens (or equivalent vote power) must file a dispute.

Below is an illustration with example values:

![](/img/disputing-outcomes-2.png)



