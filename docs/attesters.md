---
sidebar_position: 10
---

# Attesters

## Proof of Reputation

Attesters are the protocol's last line of defence in the search for truth. Attesters are provably reputable individuals in the Eth ecosystem that have earned their respective reputations externally from Truemarkets.

This includes high-ranking governance delegates, reputable founders, and other prominent figures, who stake their reputations behind their attestations. (Eventually this can and should expand to reputable individuals outside of crypto as well).

The sybil-resistance gadget that is being described, and employed for Attesters, is called Proof of Reputation.&#x20;

The genesis Attester Pool, contains individuals in the Ethereum ecosystem that have a provable history of coordinating in decentralized groups to reach consensus and vote on proposals. This behavior uniquely resembles the critical thinking necessary to make subjective assessments about disputes through a decentralized process.

When disputes escalate beyond a token holder decision, Attesters must submit a final verdict. Their role is to provide credibly neutral perspectives to the final layer of dispute resolution.

This human element, which is backed by reputation, adds a layer of nuanced decision making that algorithms simply cannot match.

It enables the discretion necessary to verify virtually any subjective real-world information onchain.

This human element is especially important with the rise of AI.

In the future, it's expected that the majority of lower level disputes and resolutions will be carried out entirely by AI agents, with humans optimistically verifying these inputs and serving as the final arbiters of Truth.

## Selection process

Attester selection is done via protocol governance.&#x20;

The genesis attester list will contain approximately 100 reputable individuals in the Ethereum ecosystem, with an Active Attester target of 75 jurors. These individuals have been selected based on their social reputation or track record of participating in ecosystem governance.&#x20;

Once a candidate is added to an attester pool, they can begin opting into the dispute resolution system. There is no obligation that these Attesters do so, but there are incentives for their participation.

## Lottery System

To incentivize Attesters to opt into dispute resolution activity, the protocol employs a lottery system for Attesters that register for "jury duty" every epoch.

Each epoch, a set of random Attesters win the lottery and receives a reward in TRUE tokens. By registering for the lottery, attesters are signalling to the protocol that they are prepared to vote on disputes if necessary.&#x20;

The prize amount for the lottery winner targets a set number of active attesters every epoch, and the `prizeAdjustment` either increases or decreases, depending on the number of attesters that opt-in relative to the target.

If the number of attesters that register falls below the target, the prize adjusts higher for the next epoch to make it more attractive for attesters to opt in. It then continues increasing (within pre-defined limits) until the number of active attesters in a given epoch reaches the target.

Conversely, if there is a sustained over subscription of active attesters, the prize gradually decreases until the target is reached.

This configuration is inspired by Bitcoins difficulty adjustment which effectively adjusts the hash power necessary to solve the cryptographic hash function required to mine blocks. The parameter targets a set number of Bitcoin blocks every epoch and is in place to encourage participation from miners while allowing the protocol to adjust to fluctuations in block production demand.

The `attesterTarget` and `prizeAdjustment,` like all parameters in the protocol, are configurable via governance.

## The Race for Reputation

At a meta level, Truemarkets is competing in a race to recognize provably reputable humans and allow them to build a long term identity in a sybil-resistant and AI-resistant reputation system.&#x20;

This function is becoming increasingly important as AI agents proliferate on the internet.

As time passes, AI agents may become capable of building long term online reputations that can bypass newer reputation-based identity systems which postdate them.&#x20;

It is therefore very important that humanity begins establishing Proof of Reputation systems (like that of Truemarkets') from now, so they can later be leveraged for Proof of Humanhood as well. Without these reputation based identity systems, every AI-resistant identity tool will inevitably also become a surveillance tool.

In a sense, the Truemarkets oracle is also an identity and reputation establishing protocol.





For more detailed information about Attesters and the design concepts powering the oracle framework, visit the Truth Oracle [whitepaper](https://truth-oracle.gitbook.io/truth-oracle).

