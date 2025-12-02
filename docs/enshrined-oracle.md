---
sidebar_position: 7
---

# Enshrined Oracle

## Dispute resolution <a href="#dispute-resolution" id="dispute-resolution"></a>

Truemarkets uses a dispute resolution implementation which follows the [Truth Oracle](https://truth-oracle.gitbook.io/truth-oracle) framework.

Like most optimistic oracles, proposed resolutions are "optimistically" considered valid unless disputed.

If a proposed resolution is disputed, the protocol’s oracle system kicks in. The enshrined oracle has three stages of escalation with intersubjective perspectives applied through the progression.

![](/img/enshrined-oracle.png)

An initial dispute can be filed permissionlessly during the challenge window, by anyone who pledges a bond equal to that of the resolver. Upon dispute, the Oracle Council will resolve the matter by setting a result for the market as well as the slashing conditions for the two bonds.

After an Oracle Council resolution, another challenge window is triggered during which a dispute can be filed again. Doing so requires pledging a bond of $5000.

This escalation is arbitrated by TRUE holders who cast votes for the correct result and corresponding slashing conditions.

If the community is further dissatisfied by a TRUE holder decision, they can once again dispute that outcome and escalate the matter to the highest arbiters in the protocol: Attesters.

Attesters submit the final verdict for disputed markets. An attester pool is currently comprised of provably reputable individuals. When a dispute is escalated to attesters, 11 of them are randomly selected to vote on what they believe to be the market's "true" outcome (pun intended).

## Oracle progression

Stage 0)

Resolution is proposed:

* Resolver puts up a $750 bond and proposes resolution

Stage 1)

Resolution is disputed during the \[12 hour] challenge window:

* Someone disagrees and disputes the result by putting up an equal bond

Stage 2)

Oracle Council resolves dispute:

* Oracle Council votes on resolution
* Oracle Council decides slashing conditions for the resolver
* Oracle Council decides slashing conditions for the disputer

Stage 3)

Escalation occurs during the \[12 hour] challenge window:

* Disputer puts up a $7500 bond to escalate the matter to token holders for voting

Stage 4)

TRUE holders propose a resolution:

* Vote on outcome of the market
* Vote on slashing conditions

Stage 5)

Escalation occurs during the \[12 hour] challenge window:

* Disputer holding 250,000 TRUE tokens disputes the previous vote

Stage 6)

A random selection of Attesters from the jury pool submit a final verdict:

* 11 Attesters are randomly selected to resolve dispute
* If an Attester is non-responsive, another is selected from the Attester Pool
* Attesters vote on outcome of the market
* Attesters vote on slashing conditions of resolver
* Attesters vote on slashing conditions of 1st disputer
* Attesters vote on slashing conditions of 2nd disputer



