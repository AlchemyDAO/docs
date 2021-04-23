# Earn Staking Rewards

Every buyout that happens for an NFT that was owned by an Alchemy-based NFT DAO sends a small fee to the ALCH DAO which splits the fee between the ALCH Treasury and a staking contract. ALCH holders can stake ALCH tokens to earn these fees, which as the usage for Alchemy DAOs grows so will these fees.

ALCH also controls the Alchemy Treasury, where holders can vote on how the funds should be used to manage and grow the protocol. By allowing for holders to vote as well as have a direct interest in the growth that drives fee revenue, the system incentivizes the best possible uses for funds that will benefit the protocol and the holders symbiotically.

How the fee distribution works in detail:

On certain types of events that happen in the Alchemy protocol a fee will be taken and will be distributed for further processing.

1\) Minty: for every sale of a Minty minted NFT a fixed fee of **1%** of the price will be taken

2\) DutchAuction: For every outcome of a DutchAuction a fixed fee of **0.5%** of the raised value will be taken

3\) AlchemyDAO: For every buyout or single NFT sale a fixed fee of **0.5%** of the price will be taken.



Those fees will be sent to the [AlchemyRouter](https://etherscan.io/address/0xe02eF7BeAc8c723a17545e0F9F2774Caf13466fc). Here the fee will be split 50%:50%.

50% will go to the ALCH staking pool

50% will be sent to the DAO Treasury and will be available for the DAO

For the 50% that goes to the ALCH staking pool the pool will get notified with a rewards duration of 14 days. So the fee that gets sent to the pool will be distributed evenly over 14 days over all the stakers that are in the pool in contrast to their pool share.

