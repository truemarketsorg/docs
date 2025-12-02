---
sidebar_position: 8
---

# Bonds and Slashing

### Accepted Disputes <a href="#accepted-disputes" id="accepted-disputes"></a>

If a dispute turns out to have merit, the Oracle Council must react accordingly. There are several potential outcomes that can occur after a dispute is accepted:

1\) The resolver gets slashed, market resolves to a different outcome than the proposed resolution.

2\) The resolver does not get slashed, the market resolves to a different outcome than the proposed resolution.

3\) The resolver gets slashed, the market result gets _reset._

4\) The resolver does not get slashed, the market result gets _reset._

If a market has indeed resolved in the real-world, but the resolver proposed the wrong outcome, the Oracle Council would execute options #1 or #2.&#x20;

If the dispute is accepted and the market has simply not resolved yet in the real world, the Oracle Council would execute options #3 or #4.

If you notice, in two of those four options, the Oracle Council can choose to avoid slashing the resolver. This is in place to ensure the protocol isn't overly punitive to participants who make good faith attempts to resolve (or dispute) markets.

This granularity in decision making is essential for the oracle to operate at scale.&#x20;

### Rejected Disputes <a href="#rejected-disputes" id="rejected-disputes"></a>

If a dispute is rejected, the Oracle Council can react in two ways:

1\) keep the proposed resolution as the market outcome, slash the disputer.

2\) keep the proposed resolution as the market outcome, but don't slash the disputer.

The same logic about being friendly to honest resolvers, also applies to disputers as well. Truemarkets loves its disputers :)

### Escalated Disputes <a href="#escalated-disputes" id="escalated-disputes"></a>

Of course, it doesn't end there, Truemarkets has multiple stages of potential escalation.

If anyone is unsatisfied with the Oracle Council's proposed resolution, they can challenge the decision.

To dispute an Oracle Council resolution, a $7500 bond must be pledged. This larger bond is necessary to prevent low-cost griefing of the oracle. Optimistic oracles expend resources most when the protocol must react to disputes. Every escalation must come at an increased cost to that of the previous, so that the protocol may potentially slash the bonds in compensation for the expended resources.

When an escalated dispute is filed, TRUE holders must step in to arbitrate. They too, must decide on which parties to slash in the dispute (if any) and vote accordingly.

Assuming the protocol is functioning honestly as expected, TRUE holders would mostly be deferring their votes back to the Oracle Council's insight based decision. The Oracle Council is a body selected via protocol governance that specializes in assessing prediction markets. In the ideal setting, it's expected that the OC's proposed resolution would reflect the optimal outcome and satisfy the original intention of the market question.

A token holder vote is mainly there to protect against Oracle Council collusion or manipulation. In the absence of these things, and barring the fruition of new evidence since the previous resolution, or gross failure by the OC, TRUE holders should mostly vote consistently with the Oracle Council.

Like the Oracle Council before them, token holders must also decide on the outcome of the market and the slashing conditions for the parties involved. TRUE holders are left with a set of options and must maintain a balance between the interests of the protocol and exercising restraint over the disputing/resolving party's bonds.

The same rule from before applies here as well, if there's merit to the escalated dispute, the $5000 bond should not be slashed, regardless of whether the dispute is accepted or not.

### Final Verdict <a href="#final-verdict" id="final-verdict"></a>

Attesters are the final arbitrators of disputes.

Attesters are provably reputable individuals in the ecosystem who's reputations are unaffiliated with Truemarkets. Attesters are selected from the community based on some proof of reputation (through an onchain governance presence, social rep, industry founder/builder, etc).

Once admitted to Attestership by the protocol, attesters are eligible to opt into "jury-duty" and potentially be selected at random to resolve disputes.

The only way to challenge a token holder proposed resolution, and escalate the matter to an Attester vote, is if a wallet that controls 250,000 TRUE tokens files a dispute.

In the genesis phase of the protocol, a bond will not be required to escalate a dispute to an attester vote. This is because the oracle has not yet been tested in the wild. It also puts too great a burden on attesters to decide the slashing conditions for a substantially large bond, while the oracle is still nascent.

Additionally, in the early stages of the protocol it's beneficial to stress test the entirety of the dispute resolution process thoroughly. Starting things off with substantial bonds to trigger attester verdicts may discourage valuable disputes that would have otherwise been proposed.

To maintain a balance between preventing low cost griefing and exercising the dispute resolution process, another method of spam resistant disputing is necessary. The method chosen here is to give TRUE holders with 250,000 tokens, or equivalent voting power, the ability to trigger an Attester vote.

Attesters do not need to decide the fate of an additional bond at this stage, they simply need to decide the market outcome, followed by the slashing conditions for the lower level disputes.

### Precedence of deferring in arbitration <a href="#precedence-of-deferring-in-arbitration" id="precedence-of-deferring-in-arbitration"></a>

It should be noted that the primary purpose of Attesters is to ensure that token holders are unable to collude and manipulate results, not necessarily to offer deep insights into the intention of a market (that’s the function of the Oracle Council). This means that in the ideal case, where the game theory of the protocol is sustained, Attesters would mostly be deferring to the decisions of TRUE holders, who would likewise be deferring to the resolutions proposed by The Oracle Council.

That philosophy is consistent through-out the dispute resolution process and draws from decades of precedent set by judicial systems in developed countries, where the higher courts often defer to lower court decisions, unless there’s a clear deviation from accepted norms.



