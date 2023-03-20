![Game of NFTs Logo](./asset/GoN.png)

# Game of NFTs

Game of NFTs (GoN) is a program that provides public environments where the Interchain NFT Transfer technology can be extensively tested with community support and innovations can be created pioneeringly.

The program includes two phases:
- **Phase 1 - Public Incentivized Testnets (Kick Off Now!)**
- Phase 2 - Hackathon (April 2023)

Phase 1 of GoN now kicks off at **2023-03-01-06:00 UTC**, and we have a number of tasks and rewards scheduled. Rewards will be distributed based on a point system, and allocated to winners who have completed certain tasks and submit an entry for dedicated awards.

**Table of Contents**

- [Game of NFTs](#game-of-nfts)
  - [Overview](#overview)
  - [Join \& Evidence Submission](#join--evidence-submission)
  - [Disclaimers](#disclaimers)
  - [Timeline](#timeline)
    - [Stage 1: Welcome to GoN](#stage-1-welcome-to-gon)
    - [Stage 2: Let's Dive into Interchain NFTs Transfer](#stage-2-lets-dive-into-interchain-nfts-transfer)
    - [Stage 3: Enjoy the Carnival of GoN](#stage-3-enjoy-the-carnival-of-gon)
      - [**Round 3: Competitive Individual Race**](#round-3-competitive-individual-race)
  - [Challenge](#challenge)
      - [**C1**: Strategy of relaying your tx smoothly.](#c1-strategy-of-relaying-your-tx-smoothly)
      - [**C2**: Strategy of preventing bunch txs stuck on channels.](#c2-strategy-of-preventing-bunch-txs-stuck-on-channels)
  - [Point System](#point-system)
    - [General Tasks](#general-tasks)
    - [Game Tasks](#game-tasks)
    - [Challenging Tasks](#challenging-tasks)
    - [Award](#award)
  - [Rules](#rules)
    - [Entry Requirements](#entry-requirements)
    - [Disqualification](#disqualification)
    - [Prohibited Behavior](#prohibited-behavior)
  - [Acknowledgements](#acknowledgements)
  - [Reference Links](#reference-links)

## Overview

Through the several rounds, participants are expected to gain knowledge and build an understanding of the Interchain NFTs feature and assist in the discovery of interesting attack vectors.	

The testnet infrastructure includes:

- [ICS-721 Enabled SDK and Wasm Chains](./doc/testnet-info.md#chain-information)
- [ICS-721 IBC Channels and Ports](./doc/port-channel-table.md)
- [Support Services in Cosmos Discord](https://discord.com/channels/669268347736686612/1074987031270268958)
- [Testnet Faucets](./doc/testnet-info.md#faucet)
- [Testnet Explorers](./doc/testnet-info.md#explorer)

Participants will utilize all GoN testnets for feature-testing, and for completing multiple tasks.

💬 Event coordinators will be available in the [Cosmos Network Discord](https://discord.gg/cosmosnetwork) #🐇┇gon-testnet channel

📍 A leaderboard will be available at https://interchainnfts.dev/gon/scorecard.html

## Join & Evidence Submission

According to information provided via the [registration form](https://docs.google.com/forms/d/e/1FAIpQLSfIhkXzOUTNu5R2cueCSt-_0Dic4MdsF193I9GSx64YTqNyWw/viewform), eligible participants have been invited into [Cosmos Network Discord](https://discord.gg/cosmosnetwork) #🐇┇gon-testnet channel to start coordinating their participation.

Before you start testing, please kindly check the join & evidence submission guidance provided at [gon-evidence](https://github.com/game-of-nfts/gon-evidence).
 - Step 1. You need to submit [qualification evidence](https://github.com/game-of-nfts/gon-evidence#qualification-evidence-submission) to upload basic team information
 - Step 2. After that, you need to add each [task evidence](https://github.com/game-of-nfts/gon-evidence#task-evidence-submission) into your own `info` sheet as required and submit for verification and scoring
 - Step 3. For special award application, you should submit issues based on [award application](https://github.com/game-of-nfts/gon-evidence#award-application) for judging
 - Step 4. During the testing phase, if you find a bug/issue, please report based on [bug submission](https://github.com/game-of-nfts/gon-evidence#bug-submission)

In order to verify the authenticity of identity, ensure fairness of the game, and protect participants' rights in receiving points and claiming rewards, please make sure to submit evidence as required.

*Please note that all submissions will be public, so please make sure to **create new addresses of test chains** to participate in the public testing.*

## Disclaimers
 1. The final number of points awarded to each participant is at the discretion of the testnet judges.
 2. The timeline for all stages and rounds may change depending on the outcome of previous activities.
 3. Available tasks/awards and points may be adjusted during the course of the testnet program.
 4. All evidence submitted for scoring points must be submitted to [gon-evidence](https://github.com/game-of-nfts/gon-evidence) as required.

## Timeline

The Incentivized Testnets has 3 stages with different tasks. Tasks will be revealed gradually as the game progresses.

Participants can refer [the installation doc](doc/installation.md) to install the client software and [the instruction doc](./doc/instruction-ics721.md) to get familiar with Interchain NFTs Transfer operations.

### Stage 1: Welcome to GoN

Start from **Mar 1**

- Create Collections and NFTs
- Perform Interchain NFTs Transfer

**Round 1: Warm-ups**

IRISnet, Stargaze, Juno, Uptick and OmniFlix have prepared their testnets, allowing participants to create their collections and NFTs. These NFTs can be used for the next transfer tasks of the game, marking the first time participants can experience Interchain NFT Transfer.

**Rules:**
 
- Participant issue their own classes(collections, denoms) and must set class data as the JSON string below
- This allows participants to bind their classes to their GitHub account and prove they have control of the class owner
- All the following tasks related to NFT transfer must be minted under their classes
- Class owner must be the IRISnet address of each pariticipant at the time of registration

```json
{
  "github_username": "username, this is a must",
  "discord_handle": "discord handle, this is optional",
  "team_name": "your team name, this is optional",
  "community": "if you come from a community"
}
```

**Tasks**: A1, A2, A3, A4, A5, A6


### Stage 2: Let's Dive into Interchain NFTs Transfer

Started from **Mar 6**

- Perform Interchain NFT Transfer through different flows

**Round 2: Journey for One**

Participants complete Interchain NFTs Transfer independently, which means they need to perform operations using their own account addresses on each chain. For each task, participants should start transferring with a different NFT. As a result, they need to create multiple NFTs under their collections.

**Rules:**

- Each NFT can only be used as evidence once for tasks in Round 2.
- Participants must use NFT minted under classes/denoms they issued in Round 1.
- Participants must use their own account addresses provided at the registration stage.
- Flow can be queried off-chain with flow-id.

**Tasks**: A7~A20


### Stage 3: Enjoy the Carnival of GoN

Started from **Mar 13**

- Competitive individual race
- Quiz game
- ...

#### **Round 3: Competitive Individual Race**

In this round, participants will receive [NFT airdrops](https://github.com/game-of-nfts/gon-evidence/issues/460) on IRISnet. Each NFT contains `Task Data` in its token data, which includes a `flow` field with a corresponding `flow-id` value that can be used to query the actual flow [in flow table](https://github.com/game-of-nfts/gon-testnets/blob/main/doc/flow-table.md). Participants can then perform Interchain NFT Transfer using the specified flows. After completing the interchain NFT transfer, each participant must transfer that NFT to the `last_owner` to complete the race. **Remember, for the final interchain transfer, transfer the NFT back to your Iris address first, and then transfer it to the `last_owner`**

**Task Data**
```
{
  "type": "individual race round",
  "flow": "the flow id, check flow with flow-id on https://github.com/game-of-nfts/gon-testnets/blob/main/doc/flow-table.md",
  "last_owner": "the ultimate owner of this NFT",
  "start_height": "transfer before this height are considered invalid"
}
```

The airdrop has two rounds: In the first round, all participants will go through the same flow, and the airdrop will start at around `2023-03-15 06:00 UTC`. In the second round, all participants will go through different flows, and the airdrop will start at around `2023-03-16 06:00 UTC`. Before that, participants can prepare their strategies. Please ensure that you have been added to the gon-evidence repository and that your information is correct, otherwise you may not receive the airdrop!

**Rules:**

- The `start_height` is the block height on IRISnet. Any transfer prior to the `start_height` will be considered invalid, which means your first Interchain NFT Transfer must happen after that height. Note that `start_height` is not used for calculate your grade.
- The `last_owner` is an official address on IRISnet, and is the final recipient of the NFT in this game. 
- Considering the time zone difference, the completion time is calculated by the **difference** in height between the last NFT transfer (to the `last_owner`) and the first Interchain NFT transfer (not `start_height`) on IRISnet.
- The participant with the smallest difference in block height will rank higher, and in case of a tie, the ranking will be based on the height of the last transfer, with the participant having the lower height ranking higher.
- Participants must use their own account addresses provided at the registration stage.
- The third round of the competition will conclude at `2023-03-17 23:59:59 UTC`. After this, you can still complete B1 and B2, but your race rank will not be counted, and you will not be eligible to win B3 and B4.
- The top 10 participants in each airdrop round will be awarded B3 and B4 points. Evidence is not required for B3 and B4, as we calculate the height difference from B1 and B2 evidence.

**Tasks:** B1, B2, B3, B4

## Challenge

During the activity on the testnet, we found that there were some issues when transferring through the designated channels, possibly caused by defects or attacks. A large number of transactions needed to wait a long time to be smoothly relayed, which has become a recognized challenge.

However, this is also the meaning of the existence of the testnet. By solving these exposed issues, we can operate better in the formal environment. Therefore, we have set up challenge tasks to encourage participants to solve these problems, ensure the stability and normal operation of the channels, and obtain challenge points.

Open an issue on `gon-evidence` to show you can solve the challenge!

#### **C1**: Strategy of relaying your tx smoothly.

Provide the most effective strategy and tool for transferring a stuck transaction package to the destination chain, ensuring seamless transaction relay between different blockchains.

**Rules:**
- Select only two best solutions
- Explain the principle and provide the code

#### **C2**: Strategy of preventing bunch txs stuck on channels.

Provide the most effective strategy to ensure smooth and uncongested transfer operation between chains, preventing batches of transactions from getting stuck.

**Rules:**
- Select only one best solution
- Explain the principle and provide the code

## Point System

For evidence submission, please refer to [gon-evidence](https://github.com/game-of-nfts/gon-evidence#task-evidence-submission)

### General Tasks

General tasks allow participants to fully experience the NFT-transfer functionality. The deadline for the general task submissions (stage 1&2) originally due on the 13th will be extended to around 27th, considering that more testing would be better.~~These tasks will be locked once the 3rd stage has begun.~~ Participants must submit evidence generated before then (based on the specified block height). Details of flow and flow style in the task description can be found [here](./doc/flow-table.md).

| Id  | Point | Task                                                   | Details                                                                                     |
| --- | ----- | ------------------------------------------------------ | ------------------------------------------------------------------------------------------- |
| A1  | 1     | Create one Collection on IRISnet                       | Must set ClassUri and ClassData                                                             |
| A2  | 1     | Mint NFTs on IRISnet                                   | Must set TokenUri and TokenData and mint at least two NFTs                                  |
| A3  | 1     | Transfer an NFT from IRISnet to Juno or Stargaze       | The NFT must be the one created in A2                                                       |
| A4  | 1     | Transfer an NFT from IRISnet to Uptick or OmniFlix     | The NFT must be the one created in A2                                                       |
| A5  | 1     | Transfer the NFT on Stargaze or Juno back to IRISnet   | The NFT must be the one transferred in A3 <br> Transfer back through the same channel in A3 |
| A6  | 1     | Transfer the NFT on Uptick or OmniFlix back to IRISnet | The NFT must be the one transferred in A4 <br> Transfer back through the same channel in A4 |
| A7  | 2     | Perform cross-chain NFT transfer as flow-a1            | Transfer in a never-go-back style.                                                          |
| A8  | 2     | Perform cross-chain NFT transfer as flow-a2            | Transfer in a never-go-back style.                                                          |
| A9  | 2     | Perform cross-chain NFT transfer as flow-a3            | Transfer in a never-go-back style.                                                          |
| A10 | 2     | Perform cross-chain NFT transfer as flow-a4            | Transfer in a never-go-back style.                                                          |
| A11 | 3     | Perform cross-chain NFT transfer as flow-a5            | Transfer in a never-go-back style.                                                          |
| A12 | 3     | Perform cross-chain NFT transfer as flow-a6            | Transfer in a never-go-back style.                                                          |
| A13 | 2     | Perform cross-chain NFT transfer as flow-b1            | Transfer in a revisit style.                                                                |
| A14 | 2     | Perform cross-chain NFT transfer as flow-b2            | Transfer in a revisit style.                                                                |
| A15 | 2     | Perform cross-chain NFT transfer as flow-b3            | Transfer in a revisit style.                                                                |
| A16 | 2     | Perform cross-chain NFT transfer as flow-b4            | Transfer in a revisit style.                                                                |
| A17 | 2     | Perform cross-chain NFT transfer as flow-c1            | Transfer in a backtrack style.                                                              |
| A18 | 2     | Perform cross-chain NFT transfer as flow-c2            | Transfer in a backtrack style.                                                              |
| A19 | 3     | Perform cross-chain NFT transfer as flow-c3            | Transfer in a backtrack style.                                                              |
| A20 | 3     | Perform cross-chain NFT transfer as flow-c4            | Transfer in a backtrack style.                                                              |

### Game Tasks

| Id  | Point | Task                                         | Details                                             |
| --- | ----- | -------------------------------------------- | --------------------------------------------------- |
| B1  | 5     | Competitive! Individual Race Round 1         | Each participant will go through the same flow      |
| B2  | 5     | Competitive! Individual Race Round 2         | Each participant will go through the different flow |
| B3  | 50    | Competitive! Individual Race Round 1 Winners | The top 10 participants will get 50 points each.    |
| B4  | 50    | Competitive! Individual Race Round 2 Winners | The top 10 participants will get 50 points each.    |
| ... | ...   | ...                                          | ...                                                 |

### Challenging Tasks

| Id  | Point | Task                                   | Details             |
| --- | ----- | -------------------------------------- | ------------------- |
| C1  | 350   | Challenge! Relay your stucking package | At most two winners |
| C2  | 800   | Challenge! Prevent bunch stuck txs     | At most one winner  |


### Award

| Id  | Points | Award              | Details                                                                                                                                                      |
| --- | ------ | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1   | 1200   | Best Auditor       | Discover the most serious potential protocol and code vulnerabilities.                                                                                       |
| 2   | 800    | Public Good Awards | Provide the tools to help test Interchain Transfer NFT, including interchain explorers, NFT path visualization tools, wallets, dashboards, etc. At most two. |
| 3   | 350    | Community Star     | Provide the most help for the game and participants.                                                                                                         |
| 4   | 250    | Best Promoter      | Create the best GoN promotional content on social media. <br> *We will take views and other metrics into consideration*.                                     |
| 5   | 200    | Bug Hunters        | Find bugs that affect the functionality of ICS-721. At most five.                                                                                            |
| 6   | 100    | Best NFT Memes     | Create the most popular NFT memes.                                                                                                                           |

## Rules

The Game of NFTs Phase 1 testing aims to provide mainnet-like environments for participants to better understand and become familiar with Interchain NFTs, and idenetify potential issues. Breaking the rules listed below will result in disqualification.

The rules for Game of NFTs Phase 1 are subject to change at any time through launch, and any changes will be committed here.

### Entry Requirements
To participate, please note that: 

- Employees of Organizer Teams (IRISnet, Stargaze, Juno, Uptick, OmniFlix) are eligible to participate, but ineligible for rewards.
- GitHub account used for testing must be registered more than one year.


### Disqualification

The following behavior will result in disqualification from Game of NFTs Phase 1 Incentivized Testnets:
- Registering multiple teams in order to win more testnet prizes than you otherwise would.
- Copying or tampering with any information of other participants to join testing and win rewards.
- Engaging in any prohibited behavior.


### Prohibited Behavior

- Engaging in any behaviour that might be unethical / not in line with the community ethics of the Cosmos Hub, IRISnet, Stargaze, Juno, Uptick and OmniFlix.
- Any attack against a node that violates the acceptable use policy outlined by that node's cloud service provider. Please familiarize yourself with those policies (such as Google's, Amazon's, or Digital Ocean's).
- Social engineering attacks against organizer-operated nodes. This includes but is not limited to phishing, compromising cloud account credentials, malware, and physical security attacks on data centers.
- Exploiting application-level security vulnerabilities in Cosmos and Tendermint code.

## Acknowledgements

We are grateful to the individuals and teams who have contributed their time and expertise to assist in updating and enhancing this repo and the GoN event.

- [Ping.Pub](https://github.com/liangping)
- [Ark Protocol](https://github.com/taitruong)
- [Gjermund Garaba](https://github.com/gjermundgaraba)
- Xavier Team
- - [Gon WorkShop](https://github.com/xavier200203/gon-workshop)
- - [How To Get Set Up For COSMOS Game of NFTs(video)](https://www.youtube.com/watch?v=knEb_M1EXrM&t=48s)
- - [Chain Transfers For Game of NFTs (GoN)(video)](https://www.youtube.com/watch?v=Y_Y3E5Z7OSQ&t=134s)
- [NFT4good  Dashboard](http://nft4good.xyz/#/transfers)
- [NFTland  Explorer](http://www.nftland.org)

## Reference Links

- [Installation](doc/installation.md)
- [Instruction](doc/instruction-ics721.md)
- [Testnet Info](doc/testnet-info.md)
- [Flow Table](doc/flow-table.md)
- [Channel Table](doc/port-channel-table.md)
- [Evidence Submission](https://github.com/game-of-nfts/gon-evidence)
