# W3F Grant Proposal

> This document will be part of the terms and conditions of your agreement and therefore needs to contain all the required information about the project. Don't remove any of the mandatory parts presented in bold letters or as headlines! Lines starting with a `>` (such as this one) can be removed.
>
> See the [Grants Program Process](https://github.com/w3f/Grants-Program/#pencil-process) on how to submit a proposal.

- **Project Name:** HE-Chain
- **Team Name:** Cryptoviet
- **Payment Address:** 0x7fD4b72d3Bf681C2e80D6076D7997B21DEf45130 (USDT)
- **[Level](https://github.com/w3f/Grants-Program/tree/master#level_slider-levels):** 2

> ⚠️ *The combination of your GitHub account submitting the application and the payment address above will be your unique identifier during the program. Please keep them safe.*

## Project Overview :page_facing_up:


### Overview

- Abstract

  HE-Chain: The decentralized blockchain platform is built for high-frequency applications and customization for NFT blockchain game projects. Applications running on top of HE-Chain will never bother about security, spamming, transaction fees, malicious accounts, and many other bad factors. They can just focus on gameplay, game experience. HE-Chain supports EVM (Ethereum Virtual Machine) that projects deploy from Ethereum, Binance Smart Chain to HE-Chain with little or no change.

- Thanks to Parity technologies
  
  HE-Chain is layer one that builds from the Substrate and is EVM compatible using [Frontier](https://github.com/paritytech/frontier).
  
- Motivating the Cryptoviet team

  As the current project titled [Heroes And Empires](https://heroesempires.com/) is running on Binance Smart Chain, mostly due to the scalability and the cost of operating, we build the platform for Heroes And Empires and many other NFT Blockchain Games.
  We have the experience of What NFT blockchain games need, Why we have to build HE-Chain, and How to build HE-Chain to solve the problems that current NFT games face when they run on Ethereum, BSC, or even Solana.
  
### Project Details


![HE-Chain Architecture](https://github.com/cryptoviet/he-chain/blob/dev/HE-Chain%20Architecture.jpg)


- **HE-Chain Architecture**:

  Two parts of the HE-Chain are Heroes and Empires. The Empires are inside the red rounded rectangle and the outside is the Heroes.
  
  **Empires**:
  
  Players have to join Empires to get the privileges. When they are in the Empires, they won't bother about the transaction fee but they can only make the limited of transactions per minute that are handled by TX-Handler, and they will be charged the amount of fee based on the period of time they stay in the Empire Pool. The Empire Pool will also ban 'bad' players with the Autoban mechanism.
  
  **Heroes**:
  
  As heroes, players can do anything with no restrictions, but with the 'high' transaction fee. 
  

  
- **Pallet structure**

  The project is broken down into 4 pallets:

  pallet-pool: Manage players in the Empires by limiting the number of players, changing upfront every 'x' amount of time (x depends on the number of players staying in the pool and number of projects running on HE-Chain, x will be determined when testnet goes live). Ban players with bad activities followed by the DAO rules.

  pallet-tx-handler: Manage player's transactions on the Empires, every minute or hour players can only make 'x' transactions. Reduce 'y' percentage of transaction fee. 'x' and 'y' will be determined by DAO.

  pallet-player: Handle player information likes id, name, friends...

  pallet-evm: create an Ethereum compatible environment for deploying Solidity code.


- **DAO**

  Currently, by design, there are three objects that need to determine through DAO:

    1. Autoban mechanism
  
     There are several rules of Empires that players must follow when they join the pool. These are ideas to keep the pool 'as clean as possible' such as ban/kick     AFK(away from keyboard) players, ban/kick players on the Spamming Blacklist.
  
    2. The Empire Pool fee
  
     Pool fee is another base idea to keep the pool clean, with a reasonable fee determined by DAO, the Empires Pool can prevent the network from malicious accounts. When many players join the pool, the total network fee charged by the pool can be significant to grow the ecosystem by granting the projects. 
  
    3. The number transaction limit of TX-Handler

     The idea of TX-Handler is to protect the network from the DDOS, also determining the right number is important because if the number is not appropriate, it's can drive away many goof projects for example. Currently, our Heroes & Empires only need a maximum of 10 TXs/minute but another good PvP game can require 30 TXs/minutes, at this point the limit number is 30 is reasonable for the HE-Chain network.
  
Although these ideas would be different in blockchain, we must deploy Heroes & Empires on HE-Chain to determine those numbers.

### Ecosystem Fit

  At this moment, most of the NFT Gaming projects are running on Ethereum, BSC, or Solana name Axie Infinity, the Sandbox, Decentraland... and as we do the [Heroes and Empires](https://heroesempires.com/). We consider these platforms are "common" chains because they can fit many purposes but don't specialize in NFT Blockchain Games. Inspired by Substrate philosophy that 'builders can just focus on the chain logic', so we built HE-Chain that specialized in NFT Blockchain Game.
  
  We know the 'pain' of scalability and  the cost of operating that Heroes & Empires spent more than $3M just for the transaction fees, we do think if we brought that money to grow the H&E ecosystem that could be game-changing.
  
  Our current user target is the NFT Gaming projects, high-frequency applications, and, of course, is Heroes and Empires. HE-Chain will bring fully decentralized platform and web3 to around 40k users of H&E and millions of users in the cryptocurrency world.
  
  At this time, in the Kusama/Polkadot ecosystem, all the EVM compatible can be the same as HE-Chain at this time but with specialization of HE-Chain chain logic, there is no project nearly the same as HE-Chain according to [Dotmarketcap](https://dotmarketcap.com/ecosystem).

## Team :busts_in_silhouette:

### Team members

- Huynh Van Quyet (Jack) - CEO + Leader
- Phan Dang Quy (David) - Technical Lead
- Truong Ngoc Vuong (Michael) - CTO + UX/UI
- Do Tan Trung (Jackson) - Full-Stack Developer + DevOps
- Luu Hoang Trung (Mike) - UI/UI + DevOps
- Bui Minh Thanh (Stefan Muto) - Substrate developer

### Contact

- **Contact Name:** Stefan
- **Contact Email:** stefan@cryptoviet.com
- **Contact Telegram:** @stefan_muto
- **Website:** https://team.cryptoviet.com/

### Legal Structure

- **Registered Address:** 
- **Registered Legal Entity:** 

### Team's experience

Cryptoviet team started in the crypto industry in 2017. Back then we did the social media, marketing plans. In 2020 we build web3 products starting with [CasperStats](https://casperstats.io/) as an Explorer for Casper Network that granted by DEVxDAO, NFT Blockchain Game named [Heroes and Empires](https://heroesempires.com/) with ~400k total users and ~40k daily users.

Team experiences comes from many aspects, but focus is on 'build to last'. Good model design and clean code is the philosophy of the Cryptoviet developer team

CEO + Leader Jack has created the most active social media in Vietnam (Bitcoin Vietnam News).

David has designed and built smart contract models for H&E, a grant project from Contentos for [wallet](https://play.google.com/store/apps/details?id=com.xonic.wallet) [source code](https://github.com/quyphandang/xonic_wallet).

Michael with more than 4 years of experience with Nodejs and React, Nuxtjs. UX/UI for https://casperstats.io and https://heroesempires.com/

Jackson, back then as Technical Lead for a well-known bank in Vietnam, with 4 years of experience in static languages (Java, C++, Typescript)

Mike, with 4 years of experience in UX/UI and Nodejs, has designed and built  [marketplace](https://market.heroesempires.com/) for H&E and https://casperstats.io

Stefan with 5 years of experience as Software Engineer working on the top crypto exchange in Vietnam, he is best on design pattern, SOLID, and Substrate

### Team Code Repos

- [Cryptoviet](https://github.com/cryptoviet)
- [Heroes and Empires](https://github.com/HeroesEmpires)

### Team Member Github

[David](https://github.com/quyphandang)
[Michael](https://github.com/satoshiman)
[Jackson](https://github.com/dttr278)
[Mike](https://github.com/lhtrung307)
[Stefan](https://github.com/mutobui)


### Team LinkedIn Profiles (if available)

[Cryptoviet](https://www.linkedin.com/company/cryptoviet/mycompany/)

[Jack](https://www.linkedin.com/in/quyethuynh2002/)
[David](https://www.linkedin.com/in/phan-dang-quy/)
[Michael](https://www.linkedin.com/in/truongngocvuong/)
[Jackson](https://www.linkedin.com/in/trung-dt/)
[Mike](https://www.linkedin.com/in/l%C6%B0u-ho%C3%A0ng-trung-53036a168/)
[Stefan](https://www.linkedin.com/in/thanhbuiminh/)

## Development Status :open_book:

HE-Chain Repos: https://github.com/cryptoviet/he-chain

[Heroes & Empires 2021 Roundup](https://medium.com/@stefan_muto/heroes-and-empires-2021-roundup-a6617941ef5a)

Whitepaper + Yellowpaper: Coming soon


## Development Roadmap :nut_and_bolt:

![HE-Chain Development Roadmap](https://github.com/cryptoviet/he-chain-assets/blob/main/HE-Chain%20Development%20Roadmap%20v2.jpg)

### Overview

- **Total Estimated Duration:** 9 months
- **Full-Time Equivalent (FTE):**  1.2 FTEs
- **Total Costs:** 39,000 USDT

### Milestone 1 — The Heroes & Empires

- **Estimated duration:** 4 months
- **FTE:**  1.2
- **Costs:** 20,000 USD

At this milestone, we build modules for Player, Empires. The requirements will fall into acceptance criteria:
+ Users can join Empires
+ Users can leave Empires
+ Charge an upfront fee when users join the pool
+ Charge a fee based on the period of time they stay in the pool
+ Refund the correct amount when users leave the pool
+ Solidity code can be deployed and called on HE-Chain
+ Create pallet-player
+ Unittest
+ Code coverage > 80%
+ Dispatchable functions must have comments


| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | Apache 2.0|
| 0b. | Whitepaper & Yellowpaper |
| 0c. | Documentation | We will comment on code, publish documents as text articles and videos to show users how Empire Pool works, how to create a player account, how to join and leave the pool |
| 0d. | Testing Guide | Every internal and external function must have the comment followed by a unittest, and the community will be rewarded for finding bugs |
| 0e. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0f. | Article | This will merge with Documentation, mostly on SubSocial, Medium, and Twitter)
| 1. | Substrate module: pallet_player | module to store player information like (name, id, friends, tokens) |  
| 2. | Substrate module: pallet_pool | module to manage players in the Empires |
| 3. | Weights/Benchmarking | implement benchmarking for pallet_player + pallet_pool to determine appropriate weights |


### Milestone 2 — DAO + TX-Handler + HE-Chain Testnet

- **Estimated duration:** 3 month
- **FTE:**  1.2
- **Costs:** 19,000 USD

In this milestone, we build modules DAO, TX-Handler, HE-Chain Testnet, the requirements will fall into acceptance criteria:
+ HE-Chain Testnet launch with at least 5 nodes
+ Build DAO to vote on-chain governance
+ Determine the 'x' number of limit transactions per minute by Testnet and vote by on-chain governance
+ TX-Handler manage the transaction limit with the 'x' above
+ Determine the 'y' percentage to reduce transaction fee by Testnet and vote by on-chain governance
+ TX-Handler reduce 'y' percentage with the number above
+ Unittest
+ Code coverage > 80%
+ Dispatchable functions must have comments


| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | Apache 2.0|
| 0b. | Documentation | We will comment on code, publish documents as text articles and videos to show users how to run HE-Chain Node, how HE-Chain on-chain governance works, why 'x' and 'y' are reasonable|
| 0c. | Testing Guide | Every internal and external function must have the comment followed by a unittest, and the community will be rewarded for finding bugs |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | This will merge with Documentation, mostly on SubSocial, Medium, and Twitter)
| 1. | Substrate module: pallet_tx_handler | module to limit the transaction and reduce transaction fee|  
| 2. | Substrate module: pallet_dao | module to vote on-chain runtime data |  
| 3. | Weights/Benchmarking | implement benchmarking for pallet_tx_handler + pallet_dao to determine appropriate weights  |
| 4. | End-user Test + Article/Tutorial | Testing as an end-user product along with articles/tutorials of how to use HE-Chain | 


## Future Plans

Fortunately, we will integrate Heroes & Empires into HE-Chain first, allowing us to devote all of our resources (20 team members including marketing, QA, and QC) to expanding, using, and testing HE-Chain.

We will work with several top NFT Game projects and teams in Vietnam such as [Axie Infinity](https://axieinfinity.com/), [Imba Game](https://imba.co/), and [StarPunk](https://starpunk.io/) to deploy on HE-Chain.

