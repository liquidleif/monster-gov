# monster-gov

> **Disclaimer**: This is work in progress and ideas/vision, not the final design.

## About this Repository

This repository will be used for

- documentation of our vision for governance at Polychain Monsters
- development of the governance related smart contracts used at Polychain Monsters

## Governance Process

The Governance Process for Polchain Monsters DAO involves the following steps:

- creating an on-chain proposal
- and voting on it
- queueing the actions (e.g. the tx to send $PMON from treasury to the receiver of a grant)
- executing the actions on-chain

To prevent spam and ensure that the proposed changes serve the Polychain Monstes DAO, proposals require a certain amount of locked $PMON, currently set at 100,000+.

Users can discuss ideas in a dedicated Discord channel and find a sponsor if they lack the required $PMON. Delegating votes is being considered.

Voting power calculation is under development, likely based on the number of owned monsters. Not necessarily the number of owned Gen-1 Monsters.

A similar setup can be found at https://nouns.center/funding/proposals.

## Single Chain vs. Cross Chain

As described in the [Governance Process Section](#governance-process) the governance process will happen mostly on-chain. A DAO system requires a transparency and also a decoupling from centralized infrastructure that can only be achieved onchain. At the current moment we don't belive that a cross-chain-governance of Polychain Monsters is possible.

This makes it necessary that assets and systems from the Polychain Monsters Ecosystem,

- which should be used in the governance
- or which should be governed
  have to be on a single chain.

This is quite the opposite to the current situation, where the Polychain Monster NFTs exist on Ethereum, BNB Chain, Polygon and Solana and can only be bridged with non-negligible cost.

Therefore we have to transfer all assets and systems (like the collector staking) to a single chain and rebuild the onchain, if they are not onchain yet (like the Collector Staking)

As noted in the [Governance Process section](#governance-process), Polychain Monsters' governance will predominantly occur on-chain. A DAO necessitates transparency and decoupling from centralized infrastructure, which can solely be achieved on-chain. Presently, we do not belive that cross-chain governance of Polychain Monsters is feasible.

Accordingly, assets and systems from the Polychain Monsters ecosystem that require governance or will be utilized in governance must be present on a single chain. This is in contrast to the current situation, wherein Polychain Monster NFTs exist on Ethereum, BNB Chain, Polygon, and Solana and and can only be bridged with non-negligible cost.

Consequently, we must transfer all assets and systems, including the collector staking, to a single chain and rebuild on-chain systems if not already present, like the Collector Staking.

Our current preferred approach involves taking a snapshot of the Polychain Monster NFTs across all our chains, followed by reminting them on the target chain we select for Polychain Monsters. We would then stop supporting Polychain Monster NFTs on other chains.

Aside from the governance benefits we have already described, this approach would provide several other advantages, such as:

- Increased liquidity density and superior user experience on the secondary markets
- A radical simplification of development, leading to faster progress
- Relief from high fees, particularly on Ethereum, which impedes participation in features for many early adopters.

</br>
