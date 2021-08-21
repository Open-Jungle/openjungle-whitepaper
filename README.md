![JungleEx](https://ipfs.io/ipfs/QmSqktoxt6VagJt7azEmxCqKm8C7GbyjWeaREEeFbvvGtz "Logo Title Text 1")

**ToDo**  
- Create architecture scheme
- Update roadmap
- Explain Governance Token

---

Welcome to the community and thank you for your interest in our Open Jungle!

In this document we will try to give you a complete but simple description of the project. If you have any questions left unanswered after reading, we invite you to join our official [discord community](https://discord.gg/VqAVPMyMzB) 🚀

**Goal of the project:**

Create a self governing Dapp to group DeFi products in a single easy-to-use and professional looking interface. We aim for the Open Jungle Platforms to become a set of tools for investors to see clear in the fast evolving DeFi ecosystem.

**Proposed roadmap:** 
1. Team building.   <
2. Specifications.  <
3. Development.
4. Alpha releases of the platform.
5. Seek financial support and marketing teams for our pre launch campaign.
6. Pre-Launch campaign.
7. Official white paper of the governance.
8. Private sale to investors and partners.
9. Public presale of the governance tokens.
10. Audits.
11. Full release. (audited version)
12. Governance update. (Supervised)
13. Ownership renouncement. (Full decentralization)

SPECIFICATIONS
==============
*Last update: 2021-08-06  
Specifications Version: 1
Note: A lot more information is needed to create a complete plan, keep in mind this is a first version.*

The Jungle exchange is built in 4 separate parts interacting with each other. 
1. Solidity Jungle Exchange Contract Collection.
2. Solidity Governance contracts. 
3. React Frontend.
4. IPSF Storage.

These four components together create the fully decentralized order book exchange.

JungleEx Contract Collection
---
These are the backbones of our Dapp, all the payments will be handled by the blockchain. For now it consists of: 
1. The pancake swap contracts and interfaces.
2. The p2p order book contract.
3. The Launchpad contract.
4. Collection of Openzeppelin standards

Governance Contract
---
The governance contract is used by the community to accept or reject coins from the exchanges launchpad. It will also serve to participate early in launchpools and other exclusive rewards. 

*Governance is not necessary and is unsafe for the alpha release. It should only be implemented after the platform has been audited.*

Frontend
---
The frontends main task is to display the information from a bunch of contracts. The problem is it can not know what contracts exist and what are the address without something telling it. If we simply encode these in our frontend it would then become a centralized application. Then, the process to fetch the information directly from the blockchain is slow and would not be pleasing for a user. 

That’s why I propose to make it first fetch from a trusted decentralized source source then validate the information against the chain. The decentralized source will be voted by the holders of the governance tokens.

Note that this way the frontend has absolutely no influence on the mechanism of the exchange and contains no sensible information.

IPFS Off-chain Storages
---
The off chain order book is simply a bunch of files on the IPFS system. These files contain the contracts address and latest logs of the blockchain but condensed in a quick access format. It will be immutable since IPFS stores data according to their hash. Periodically, the files will be updated and a new hash will be accepted and verifiable by the community. Anyone trying to affect that file with bad intentions would change its hash and alert the community. 

The scrapper used to extract the logs from the blockchain is also considered a part of this component. 

The last part of this IPFS storage section is the information for the charts on our exchange and a list of the valid currencies.










