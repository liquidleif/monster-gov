# monster-gov

> **Disclaimer**: This is work in progress and ideas/vision, not the final design. This document does not constitute financial advice. Holding, staking, or engaging with PMON or any other mentioned token (fungible or non-fungible) is inherently risky and may result in losses. No rewards are guaranteed.

## TLDR Updates

### April 21st 2023

We've realized the importance of establishing a "PMON flywheel" before initiating the DAO setup. As a result, we'll concentrate on developing PMON use cases first to ensure a solid foundation for our DAO.

Anticipate seamless PMON integration throughout our entire ecosystem.

### March 23rd 2023

The last weeks showed that much of the community embraces the transition towards a single chain and the DAO concept. However, while we are already taking measures to further decentralize Polychain Monsters, we will postpone the transition to a single chain for now. The main reasons for that are

- the current shift of users to L2 Blockchains like Arbitrum and Optimism. It is currently not possible to separete airdrop farming from real adoption, therefore we think it is appropriate to wait with the transition until we have more confidence regarding the target chain
- the interference with the work on CS 2.0 and the DAOmon progress.

Our plan for now is:

1. Current monsters stay on their chains. Only collection which is "bridged" or better "migrated" will be the [Binance Babies](https://opensea.io/collection/binance-nft-mystery-box-polychain-monsters) that should move to the [Gen-1 collection](https://opensea.io/collection/polychainmonsters-bnb) on BNB Chain.

2. CS will stay multi chain as it is already. Rewards shall be provided from treasury. CS2 will be designed as loyalty program. However, as it will get rewards from the treasury, it will be the entry to the DAO.

3. New: We'll launch DAOmon as a separate collection on a new chain and the only entry is $PMON. More info follows soon.

4. Staked DAOmon and/or $PMON will be substantial to receive CS rewards.

---

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

As noted in the [Governance Process section](#governance-process), Polychain Monsters' governance will predominantly occur on-chain. A DAO necessitates transparency and decoupling from centralized infrastructure, which can solely be achieved on-chain. Presently, we do not belive that cross-chain governance of Polychain Monsters is feasible.

Accordingly, assets and systems from the Polychain Monsters ecosystem that require governance or will be utilized in governance must be present on a single chain. This is in contrast to the current situation, wherein Polychain Monster NFTs exist on Ethereum, BNB Chain, Polygon, and Solana and and can only be bridged with non-negligible cost.

Consequently, we must transfer all assets and systems, including the collector staking, to a single chain and rebuild on-chain systems if not already present, like the Collector Staking.

Aside from the governance benefits we have already described, this approach would provide several other advantages, such as:

- Increased liquidity density and superior user experience on the secondary markets
- A radical simplification of development, leading to faster progress
- Relief from high fees, particularly on Ethereum, which impedes participation in features for many early adopters.

## How would the Transition to a Single Chain work ?

Current concept is the following:

- Hardminted Monsters: The monsters have to be burned with a TX and can afterwards be minted on the target chain.
- Softminted Monsters: We deactivate the minting of softminted monsters and allow users to mint them on the target chain.

There are multiples reason why a TX is necessary. One being that this reduces the insecurity involved with a snapshot and another one being that the transition is opt-in by the user.

What does that mean in terms of costs? Let's mainly look at the monsters on Ethereum and BNB Chain. The top 100 holders on Ethereum have on average ~70 monsters, the top 100 holders on BNB Chain have on average ~400 monsters (snapshot date March 14, 2023). If we assume that a burn will cost around $5 per monster on Ethereum and around $0.1 per monster on BNB chain, and if we assume that every collector would bridge 80% of their collection, this would lead to a total cost of $280 per top collector on Ethereum and $32 per collector on BNB Chain. Just as a reference, for somebody to mint and burn pieces of an open edition artwork on Ethereum, it is quite usual to pay $10 per NFT so the gas cost is not due to our collection.

Still, it's fair if people who decide to bridge will receive some sort of reward. This can be a special monster, $PMON or a mix of both.

## Which Monsters give voting power? And how to get them?

Our currently preferred option is "Option B".

**Option A: Release of dedicated monsters with voting power (DAOmon)**

My strategy for the Polychain Monsters DAO involves ensuring that you do not lose the $PMON spent on acquiring new Monsters that come after Generation 1, which I will refer to as DAOmon for clarity.

When you purchase a DAOmon, the $PMON spent on the purchase go directly to the DAO treasury in a 1:1 ratio. The purchased DAOmon each grant you one vote to participate in the decision-making process for the DAO treasury (meaning that you can vote on proposals). Thus, you do not lose any $PMON but you receive a DAOmon.

The current Generation 1 **cannot** give you voting power because no $PMON flew into the treasury when they were purchased. The $PMON was mostly burned or redistributed to Collector Stakers.

Instead, we plan to distribute $PMON from the current treasury through the Generation 1 Collector Staking.

These funds may not be liquid, but they can be utilized to buy DAOmon. If you buy DAOmon, the $PMON flow into the treasury. In this manner, truely longterm oriented Generation 1 holders can obtain voting power for the DAO treasury without violating the rule that DAOmon can only be generated via a flow of $PMON into the DAO treasury.

**Option B: Upgrade of Gen-1 Monsters for Voting Power**

You can use $PMON to upgrade (or "activate") Gen-1 Monsters and give them voting power in the DAO. The $PMON you spend goes into the DAO treasury, and only activated Polymon can vote on proposals. This way, $PMON and Polymon holders have aligned interests. I currently think of 2 $PMON per activation.

We plan to distribute $PMON from the treasury through the Generation 1 Collector Staking. However, only activated Polymon will count toward the Collector Staking.

The funds you receive from staking will not be liquid, but can be used to activate additional Polymon.

Having a high Collector Score is crucial in obtaining $PMON to activate more Polymon, so rarity and thoughtfully-curated collections play a significant role in this system.

</br>

## FAQ

### Do we prefer an EVM chain ?

Yes.

Firstly, our skills are best suited for EVM environments, making it easier to develop and maintain applications. Secondly, EVM has (in my opinion) the best tools and open source code in the crypto industry, with Solana having some edge in certain NFT applications. Additionally, I think that the majority of the best development communities work in EVM, which is important for collaboration and innovation.

Finally, Lindy's Law: EVM has survived numerous competitors, black swan events, and crises, while comparable non-EVM chains/technologies have not (yet). While I wouldn't bet against Solana, betting on them carries a higher risk compared to EVM chains.

### Do you lose your PMON or cant use them for a time lock period after you use them on a proposal?

The possibility of slashing exists in theory, for example, if a proposal fails to pass. However, it is unlikely to occur unless there is persistent misbehavior. I believe the best solution is to allow only $PMON that have been locked for at least a year to be used for making proposals. This will provide appropriate incentives for taking a long-term view when proposing changes.

### Can smaller wallets join together to create a group proposal?

Delegation of voting power will most likely be possible, but we are still deciding whether to enable it directly from the beginning. During a transition period, only limited proposals may be possible.

### Does this mean that the community controls the fate of the project?

It's important to note that a DAO is not necessarily controlled by "The community," but rather by individuals who have a significant and long-term stake in the project.

### How do we prevent the system from getting spammed with lots of unnecessary requests?

Proposals will require a certain amount of locked $PMON, currently set at 100,000+.

### What kind of decisions should be covered by the DAO?

This includes funding features/projects, distributing PMON from the treasury, providing incentives in the ecosystem, and more, all at a high level.

While individuals interested in funded work for the project must submit applications for funding, initiatives can also happen without approval through the DAO. For example, someone may build Dune Dashboards or a similar project independently.

### Will rarity of the DAOmons influence their voting power?

Rarity won't affect voting power. In fact, the idea that rarity is crucial for governance is unfamiliar to most NFT investors, and could be a barrier to entry. Therefore, it's easier to adopt a straightforward approach where one DAOmon equals one vote. Additionally, rarity can be difficult to define, as demonstrated by the current challenges faced for the Collector Staking.

### Is there a way to get liquid rewards from the Collector Staking?

We are considering to offer an option to claim a part of the rewards as liquid $PMON from the Collector Staking. The other part of your rewards would go to the DAO treasury though, basically meaning free $PMON for the DAO treasury. The share could e.g. be 1% claimable and 99% foing to the DAO treasury.
