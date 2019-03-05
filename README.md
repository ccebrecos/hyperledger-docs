<div style="text-align:center">

![logo](https://www.hyperledger.org/wp-content/uploads/2016/09/logo_hl_new.png)

</div>

___

Means:
- using distributed ledger technologies in a permission setting,
- using smart contracts to automate various business processes,
- building a really exciting new world, secure, trustworthy information
systems and automation of business processes.
___

## Learning Objectives

- [ ] Describe Business Blockchain and Distributed Ledger Technologies.
- [ ] Gain familiarity with current Hyperledger projects and cross-industry use cases.
- [ ] Perform clean installations of the Hyperledger Sawtooth and Hyperledger Fabric frameworks.
- [ ] Explore a sample use case/application in the context of the Hyperledger Sawtooth and Hyperledger Fabric frameworks.
- [ ] Build simple applications on top of Hyperledger Sawtooth and Hyperledger Fabric.
- [ ] Become involved in and contribute to the open source Hyperledger projects
___

It aims at advancing and promoting cross-industry blockchain technologies to ensure accountability, transparency, and trust among business partners. As a result, Hyperledger makes business network and transactions more efficient.


# Chapter 1. Discovering Blockchain Technologies > Distributed Ledger Technology (DLT)  
In summary, distributed ledger technology generally consists of three basic components:

- A **data model** that captures the current state of the ledger.

- A **language of transactions** that changes the ledger state.

- A **protocol** used to build consensus among participants around which transactions will be accepted, and in what order, by the ledger.

A blockchain is a peer-to-peer distributed ledger, forged by consensus, combined with a system for smart contracts and other assistive technologies.
Together, these can be used to build a new generation of transactional applications that establish trust, accountability, and transparency at their core.

**Smart contracts** are simply computer programs that execute predefined actions when certain conditions within the system are met.

**Consensus** refers to a system of ensuring that parties agree to a certain state of the system as the true state.
___

# Chapter 2. Introduction to Hyperledger
<div style="text-align: center">
![umbrella](https://d37djvu3ytnwxt.cloudfront.net/assets/courseware/v1/7adde90b7e1bca2dd7ac50e437291be0/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/modular_umbrella.jpg)
</div>
Hyperledger business blockchain frameworks are used to build enterprise blockchains for a consortium of organizations. They are different than public ledgers like the Bitcoin blockchain and Ethereum. The Hyperledger frameworks include:

- An append-only distributed ledger
- A consensus algorithm for agreeing to changes in the ledger
- Privacy of transactions through permissioned access
- Smart contracts to process transaction requests.

<div style="text-align: center">
![](https://d37djvu3ytnwxt.cloudfront.net/assets/courseware/v1/0747265232da64643d21679294cbbe19/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Components_of_blockchain.jpg)
</div>

### Hyperledger Iroha
Is a blockchain framework contributed by Soramitsu, Hitachi, NTT Data, and Colu. Hyperledger Iroha is designed to be simple and easy to incorporate into infrastructure projects requiring distributed ledger technology. Hyperledger Iroha emphasizes mobile application development with client libraries for Android and iOS, making it distinct from other Hyperledger frameworks. Inspired by Hyperledger Fabric, Hyperledger Iroha seeks to complement Hyperledger Fabric and Hyperledger Sawtooth, while providing a development environment for C++ developers to contribute to Hyperledger.

In conclusion, Hyperledger Iroha features a simple construction, modern, domain-driven C++ design, along with the consensus algorithm YAC.

### Hyperledger Sawtooth
Hyperledger Sawtooth, contributed by Intel, is a blockchain framework that utilizes a modular platform for building, deploying, and running distributed ledgers. Distributed ledger solutions built with Hyperledger Sawtooth can utilize various consensus algorithms based on the size of the network. By default, it uses the Proof of Elapsed Time (PoET) consensus algorithm, which provides the scalability of the Bitcoin blockchain without the high energy consumption. PoET allows for a highly scalable network of validator nodes. Hyperledger Sawtooth is designed for versatility, with support for both permissioned and permissionless deployments.

### Hyperledger Fabric
Hyperledger Fabric was the first proposal for a codebase, combining previous work done by Digital Asset Holdings, Blockstream's libconsensus, and IBM's OpenBlockchain. Hyperledger Fabric provides a modular architecture, which allows components such as consensus and membership services to be plug-and-play. Hyperledger Fabric is revolutionary in allowing entities to conduct confidential transactions without passing information through a central authority. This is accomplished through different channels that run within the network, as well as the division of labor that characterizes the different nodes within the network. Lastly, it is important to remember that, unlike Bitcoin, which is a public chain, Hyperledger Fabric supports permissioned deployments.

"If you have a large blockchain network and you want to share data with only certain parties, you can create a private channel with just those participants. It is the most distinctive thing about Fabric right now."

- Brian Behlendorf, Executive Director of Hyperledger, The Linux Foundation

### Hyperledger Indy
Hyperledger Indy is a distributed ledger purpose-built for decentralized identity. Hyperledger Indy's goal is to achieve this by developing a set of

"(...) decentralized identity specs and artifacts that are independent of any particular ledger and will enable interoperability across any DLT that supports them."

### Hyperledger Burrow
Formally known as eris-db, Hyperledger Burrow was released in December 2014. Currently under incubation, Hyperledger Burrow is a permissionable smart contract machine that provides a modular blockchain client with a permissioned smart contract interpreter built- in part to the specification of the Ethereum Virtual Machine (EVM). It is the only available Apache-licensed EVM implementation.

Following are the major components of Burrow:

- The Gateway provides interfaces for systems integration and user interfaces
- The Smart contract application engine facilitates integration of complex business logic
- The Consensus Engine serves the dual purpose of:
  - a. Maintaining the networking stack between the nodes, and,
  - b. Ordering transactions
- The Application Blockchain Interface (ABCI) provides interface specification for the consensus engine and smart contract application engine to connect.

### Hyperledger modules

#### Cello
For businesses that want to deploy Blockchain-as-a-Service, Hyperledger Cello provides a toolkit that fulfills this need. Particularly for lean businesses and small enterprises, who want to reduce or eliminate the effort required in creating, managing, and terminating blockchains, Hyperledger Cello allows blockchains deployment to the cloud. Operators can create and manage such blockchains through a dashboard, and users (typically, chaincode developers) can obtain a blockchain instance immediately.

As a Hyperledger module, "Cello aims to bring the on-demand 'as-a-service' deployment model to the blockchain ecosystem", thus helping in furthering the development and deployment of Hyperledger's frameworks. Hyperledger Cello was initially contributed by IBM, with sponsors from Soramitsu, Huawei, and Intel.

Application developers and system administrators using Cello can provision and maintain Hyperledger networks. For instance, you can create a group of distributed ledger networks in virtual clouds known as 'container clusters', and then, manage and monitor those networks with a configurable dashboard. Additionally, you can build a Blockchain-as-a-Service (BaaS) platform.

##### Cello’s Architecture
Cello leverages the Docker APIs to manage the blockchain clusters in remote hosts, including physical servers and virtual machines. Hence Cello can be easily deployed to Cloud environments that provide virtual machines on demand.
The design architecture is as follows:
- Orchestration Engine: Core to handle resource management and workload scheduling, which is mainly implemented in Python;
- Dashboard: Operational interface, implemented with JavaScript;
- Restful Server: Operational interface, which is implemented with Python;
- Drivers: Currently we utilize Docker API lib, to support native host and Swarm cluster The driver layer is designed to be pluggable to support more types in future;
- Tools: We have also designed several tools to handle tasks like monitoring and logging, which are mainly implemented in Golang. However, the framework is pluggable, hence we can also integrate existing open-source tools.
<div style="text-align: center">
![arch](https://www.hyperledger.org/wp-content/uploads/2017/01/architecture-768x282.png)
</div>
[more info](https://www.hyperledger.org/blog/2017/01/17/hyperledger-says-hello-to-cello)

#### Composer
Hyperledger Composer provides a suite of tools for building blockchain business networks. These tools allow you to:

Model your business blockchain network
Generate REST APIs for interacting with your blockchain network
Generate a skeleton Angular application.

#### Explorer
Hyperledger Explorer is a tool for visualizing blockchain operations. It is the first ever blockchain explorer for permissioned ledgers, allowing anyone to explore the distributed ledger projects being created by Hyperledger's members from the inside, without compromising their privacy. The project was contributed by DTCC, Intel, and IBM.

Designed to create a user-friendly web application, Hyperledger Explorer can view, invoke, deploy, or query:

- Blocks
- Transactions and associated data
- Network information (name, status, list of nodes)
- Smart contracts (chain codes and transaction families)
- Other relevant information stored in the ledger.
___

# Chapter 3. The Promise of Business Blockchain Technologies
### Business Blockchain Technologies Overview
Blockchain is a new data structure with an automated way to enforce trust among participants. Consensus algorithms ensure that all participants agree on the data stored within the blockchain. Blockchain opens the door to disrupt any industry that relies on a central authority to confirm authenticity. It also allows independent, and even competing organizations, to share information to gain efficiencies across an industry.

In permissioned blockchains, a consortium of organizations are responsible for authenticating and controlling the participants in a blockchain. In public blockchains, no central authority or administration is required to exchange data. Blockchains can drive business innovation through controlled data-sharing networks for industry consortiums.

The promise of distributed ledger technologies (DLT) to simplify and automate key work functions has many industries taking notice. Businesses recognize the efficiency gains from transitioning from closed and proprietary solutions to standard open source capabilities, such as Hyperledger business blockchain technologies. Several common project features of blockchain applications are taking shape as the technology matures.

### When to use a Blockchain
There are certain factors to consider when evaluating blockchain distributed ledger technology for your business. How many participants are in your system? What is the geographical distribution of the participants? What sort of performance requirements do you have? Defining the rules, risks, and responsibilities of each party in your blockchain system is useful as you consider transferring a database to a decentralized environment such as one of the Hyperledger frameworks. Blockchain is best suited for business applications where one or more of the following conditions apply:

- There is a need for a shared common database
- The parties involved with the process have conflicting incentives, or do not have trust among participants
- There are multiple parties involved or writers to a database
- There are currently trusted third parties involved in the process that facilitate interactions between multiple parties who must trust the third party. This could include escrow services, data feed providers, licensing authorities, or a notary public
- Cryptography is currently being used or should be used. Cryptography facilitates data confidentiality, data integrity, authentication, and non-repudiation
- Data for a business process is being entered into many different databases along the lifecycle of the process. It is important that this data is consistent across all entities, and/or digitization of such a process is desired
- There are uniform rules governing participants in the system
- Decision making of the parties is transparent, rather than confidential
- There is a need for an objective, immutable history or log of facts for parties’ reference
- Transaction frequency does not exceed 10,000 transactions per second.

### When not to use Blockchain
Blockchain technology is a powerful tool, but it is not always the right tool for the job at hand. If you are contemplating using blockchain technology, be sure to evaluate the problem fully. The following conditions are not currently well suited to blockchain-based solutions:

- The process involves confidential data
- The process stores a lot of static data, or the data is quite large
- Rules of transactions change frequently
- The use of external services to gather/store data
___

# Chapter 4. Technical Requirements  

You have to have the following features installed on your computer: **cURL**, **Node.js**, **npm** package manager, **Go Language**, **Docker**, and **Docker Compose**, and, if you are a Windows user, VirtualBox.

Fast solution:
<div style="text-align: center">
[bash script](https://github.com/ccebrecos/hyperledger-dependencies)
</div>

___

# Chapter 5. Introduction to Hyperledger Iroha

<div style="text-align: center">
![](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/94f08731c2a2a792a7a20c298839aa38/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Iroha_3_sm.png)
</div>

Hyperledger Iroha is a blockchain framework, and one of the Hyperledger projects hosted by The Linux Foundation. Hyperledger Iroha is designed to be simple and easy to incorporate into infrastructure projects requiring distributed ledger technology. Hyperledger Iroha features a simple construction, modern, domain-driven C++ design, emphasis on mobile application development, and the YAC consensus algorithm.

### Goals
1. Provide an environment for C++ developers to contribute to Hyperledger.
2. Provide infrastructure for mobile and web application support.
3. Provide a framework to introduce APIs and a new consensus algorithm that can potentially be incorporated into other frameworks in the future.

### Architecture
<div style="text-align: center">
![iroha-arch](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/cb033d180ecb4eb288f2f0a489195e6c/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Iroha-architecture.png)
</div>

The components are:
- **Model** classes are system entities.
- **Torii** (gate) provides the input and output interfaces for clients. It is a single [gRPC](https://grpc.io/) server that is used by clients to interact with peers through the network. The client's RPC call is non-blocking, making Torii an asynchronous server. Both commands (transactions) and queries (read access) are performed through this interface.
- **Network** encompasses interaction with the network of peers.
- **Consensus** is in charge of peers agreeing on chain content in the network. The consensus mechanism used by Iroha is YAC (Yet Another Consensus), which is a practical byzantine fault-tolerant algorithm based on voting for block hash.
- **Simulator** generates a temporary snapshot of storage to validate transactions by executing them against this snapshot and forming a verified proposal, which consists only of valid transactions.
- **Validator** classes check business rules and validity (correct format) of transactions or queries. There are two distinct types of validation that occur in Hyperledger Iroha:
  - **Stateless validation** is a quicker form of validation, that performs schema and signature checks of the transaction.
  - **Stateful validation** is a slower form of validation, that checks the permissions and the current world state view, which is the latest and most actual state of the chain, to see if desired business rules and policies are possible. For example, does an account have enough funds to transfer?
- **Synchronizer** helps to synchronize new peers in the system or temporarily disconnected peers.
- **Ametsuchi** is the ledger block storage which consists of a block index (currently Redis), block store (currently flat files), and a world state view component (currently PostgreSQL).

### Participants
- **Clients** are able to:
  1. Query data that they have access/permission to
  2. Perform a state-changing action, 'transaction', which consists of atomic operations, called 'commands'. For example, in a single transaction, a user can transfer funds to three people (three separate commands). But, if he/she does not have enough funds to cover for all, the whole transaction will be rejected.
- **Peers** maintain the current state and their own copy of the shared ledger. A peer is a single entity in the network, and has an address, identity, and trust. Hyperledger Iroha is designed so that a single peer may be a single computer or scaled for a cluster, meaning different computers are used for ledger storage, indices, validation, and peer-to-peer logic.
- **Ordering** service orders transactions into a known order. There are a few options for the algorithm used by the ordering service. Kafka is considered a good candidate. It is important to mention that if Kafka, or any other distributed solution is used, that it be clustered; otherwise, this will result in a single point of failure.

### Transaction flow

**Step 1:** A client creates and sends a transaction to the Torii gate, which routes the transaction to a peer that is responsible for performing stateless validation.
<div style="text-align: center">
![Step 1 of Iroha Transaction Flow](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/31cba94d9a190c0a12ab6bac4c891e14/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Step_1_of_Iroha_Transaction_Flow.png)
</div>

**Step 2:** After the peer performs stateless validation, the transaction is first sent to the ordering gate, which is responsible for choosing the right strategy of connection to the ordering service.
<div style="text-align: center">
![Step 2 of Iroha Transaction Flow](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/21102f3a868cc94b8157d7871ca30192/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Step_2_of_Iroha_Transaction_Flow.png)
</div>

**Step 3:** The ordering service puts transactions into order and forwards them to peers in the consensus network in the form of proposals. A proposal is an unsigned block shared by the ordering service, that contains a batch of ordered transactions. Proposals are only forwarded when the ordering service has accumulated enough transactions, or a certain amount of time has elapsed since the last proposal. This prevents the ordering service from sending empty proposals.
<div style="text-align: center">
![Step 3 of Iroha Transaction Flow](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/dd7b06c38b34545769fb70f4e5a1a61a/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Step_3_of_Iroha_Transaction_Flow.png)
</div>

**Step 4:** Each peer verifies the proposal’s contents (stateful validation) in the Simulator and creates a block which consists only of verified transactions. This block is then sent to the consensus gate which performs YAC consensus logic.
<div style="text-align: center">
![Step 4 of Iroha transaction flow](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/91303543f6393c61426a9b216083bed8/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Step_4_of_Iroha_transaction_flow.png)
</div>

**Step 5:** An ordered list of peers is determined, and a leader is elected based on the YAC consensus logic. Each peer casts a vote by signing and sending their proposed block to the leader.
<div style="text-align: center">
![Step 5 of Iroha transaction flow](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/00da4d62048b9bdf0b331629946b3573/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Step_5_of_Iroha_transaction_flow.png)
</div>

**Step 6:** If the leader receives enough signed proposed blocks (i.e. more than two thirds of the peers), then it starts to send a commit message, indicating that this block should be applied to the chain of each peer participating in the consensus. Once the commit message has been sent, the proposed block becomes the next block in the chain of every peer via the synchronizer.
<div style="text-align: center">
![Step 6 of the Iroha transaction flow](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/118a771edf63220195e924a7154eaedd/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Step_6_of_Iroha_Transaction_flow.png)
</div>

### YAC - Steps to Successful Consensus
**Step 1:** The ordering service shares a proposal to all peers. A **proposal** is an unsigned block created and shared to peers in the network by the ordering service. It contains a batch of ordered transactions.

**Step 2:** Peers calculate the hash of a verified proposal and sign it. The resulting **< Hash, Signature>** tuple is called a **vote**.

**Step 3:** Based on the hashes created in the previous step, each peer computes an ordering list or order of peers. To do this, the ordering function will need to have knowledge of all the peers voting in the network, and is based on the hash of the proposed block. The first peer in the list is called the **leader**. The leader is responsible for collecting votes from other peers and sending the commit message.

**Step 4:** Each peer votes. The leader collects all the votes and determines the supermajority of votes for a certain hash. The leader sends a commit message that contains the votes of the committing block. This response is called a **commit**.

**Step 5:** After receiving the commit, the peers verify the commit and apply the block to the ledger. At this point, consensus is complete.


One of the main goals at Hyperledger in the future is to have less disjointed projects, and more libraries that can be used together as components. With that vision in mind, Hyperledger Iroha wants to eventually provide the following C++ components that can be used by other Hyperledger projects:

### Relationship to Hyperledger Fabric and Hyperledger Sawtooth
- YAC consensus library
- Ed25519 digital signature library
- SHA-3 hashing library
- Iroha transaction serialization library
- P2P communication library
- iOS library
- Android library
- JavaScript library
- Blockchain explorer/data visualization suite.
___

# Chapter 6. Introduction to Hyperledger Sawtooth
### Featured Hyperledger Sawtooth Elements

- **Transaction validators** validate transactions.

- **Transaction families** are smart contracts in Hyperledger Sawtooth. They define the operations that can be applied to transactions. Transaction families consist of both transaction processors (the server-side logic) and clients (for use from Web or mobile applications).

- **Transaction processor** is the server-side business logic of transaction families that acts upon network assets.

- **Transaction batches** are clusters of transactions that are either all committed to state or are all not committed to state.

- **The network layer** is responsible for communicating between validators in a Hyperledger Sawtooth network, including performing initial connectivity, peer discovery, and message handling.

- **Global state** contains the current state of the ledger and a chain of transaction invocations. The state for all transaction families is represented on each validator. The process of block validation on each validator ensures that the same transactions result in the same state transitions, and that the resulting data is the same for all participants in the network. The state is split into namespaces, which allow flexibility for transaction family authors to define, share, and reuse global state data between transaction processors.

### Architecture
#### Consensus
After a batch of many transactions is submitted to the network, the network’s consensus algorithm is run to choose a node to publish the transaction block. By default, the Proof of Elapsed Time consensus algorithm is used, and the transaction validator with the shortest wait time publishes the transaction block. The transaction block is then broadcast to the publishing nodes.

Each node within the network receives the transaction block, and validators verify whether the transaction is valid or not. If the transaction is validated, the global state is updated.

Hyperledger Sawtooth is unique because of its distributed state agreement, whereby every node in the system has the same understanding of information, and, as the supply chain matures, the data stored remains consistent across the network.

#### Transaction Batching
Hyperledger Sawtooth **transaction batches** are clusters of transactions that are either all committed to state together, or none of the transactions are committed at all. As a result, transaction batches are often described as an atomic unit of change, since a group of transactions are treated as one, and are committed to the state as one. Every single transaction in Hyperledger Sawtooth is submitted within a batch. Batches can contain as little as a single transaction.

When a transaction is created by a client, the batch is submitted to the validator (which we will cover more in depth in the next section). Transactions are organized into a batch in the order they are intended to be committed. The validator then, in turn, applies each transaction within the batch, leading to a change in the global state. The batch is committed to the state. If one transaction within the batch is invalid, then none of the transactions within that batch are committed.

In summary, transaction batching allows a group of transactions to be applied in a specific order, and if any are invalid, then none of the transactions are applied. This is a powerful tool that can be utilized by many enterprise solutions, as it provides greater efficiency and control for end users.

#### Validators
In any blockchain network, modifying the global state requires creating and applying a transaction. In Hyperledger Sawtooth, **validators** apply blocks that cause a change in the state. More specifically, validators validate transaction blocks, and ensure that transactions result in state changes that are consistent across all participants in the network.

To start, a user creates a transaction batch and submits it to a validator via a client and REST API. The validator then checks the transaction batch and applies it if it is considered valid, resulting in a change to the state. In terms of our demonstrated scenario, Sarah, the fisherman, creates a transaction batch to record information about a group of tuna catches. The validator would then apply the transactions, and the state would be updated if all appropriate attributes are present: a unique ID number, location and time of the catch, weight, and who caught the fish. If any of these elements are missing, the transactions within the batch would not be applied, and the state would not be updated.

<div style="text-align: center">
![validators-sawtooth](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/c7b3d5552070184b7b56fc25d316f585/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Sawtooth_validators.png)
</div>

#### Journal
In Hyperledger Sawtooth, the journal maintains and extends the blockchain for the validator. It is responsible for validating candidate blocks, evaluating valid blocks to determine if they are the correct chain head, and generating new blocks to extend the chain. Transaction batches arrive at the journal, where they are evaluated, validated, and added to the blockchain. Additionally, the journal resolves forks, which occur due to disagreements over who commits a block. Once blocks are completed, they are delivered to the ChainController for validation and fork resolution.

Consensus in Hyperledger Sawtooth is modular, meaning that the consensus algorithm can be easily modified. Hyperledger Sawtooth provides an abstract interface that supports both PBFT and Nakamoto-style algorithms. To implement a new consensus algorithm in Hyperledger Sawtooth, you must implement the distinct interface for: block publisher, block verifier, and fork resolution.

- **Block publisher:** Creates new candidate blocks to extend the chain.
- **Block verifier:** Verifies that candidate blocks are published in accordance with consensus rules.
- **Fork resolver:** Chooses which fork to use as the chain head for consensus algorithms that result in a fork.

<div style="text-align: center">
![](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/a6cfe922dbd88b452ce58d493273f9e4/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Consensus_interface.png)
</div>

#### Transaction families
As with any blockchain framework, transaction updates need to be approved and shared between many untrusted parties. As such, many blockchain frameworks have a mechanism for supporting distributed ledgers, as well as a method for changing the state of the shared ledger.

In Hyperledger Sawtooth, the data model that captures the state and the transaction language that changes the state are implemented using **transaction families**.

A transaction family consists of a group of operations or transaction types that are allowed on the shared ledgers. This allows for flexibility in the level of versatility and risk that exists on a network. Transaction families are often called 'safer' smart contracts, because they specify a predefined set of acceptable smart contract templates, as opposed to programming smart contracts from scratch.

Hyperledger Sawtooth’s transaction families can be written in many languages, including Javascript, Java, C++, Python, and Go, which allows flexibility for businesses to bring their own transaction families. Hyperledger Sawtooth allows the developers to specify the address/namespace of data, which provides flexibility in defining, sharing, and reusing data between different transaction families.

<div style="text-align: center">
![sawtooth-transaction-families](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/8f6a37e9af4a9e8117c7d1b779e0b405/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Transaction_families.png)
</div>

#### Transaction Processor
A **transaction processor** provides the server-side business logic that operates on assets within a network. Hyperledger Sawtooth supports pluggable transaction processors, that are customizable based on the specific application. Businesses are able to develop transaction processors that do exactly what their applications need. Additionally, transaction processors can be written in a variety of languages (Java, Python, C, C++, JavaScript, and Go), allowing for ease of use and simplicity when handling assets.

Each node within the Hyperledger Sawtooth network runs a transaction processor. This transaction processor processes incoming transactions submitted by authorized clients. In Hyperledger Sawtooth, the Sawtooth SDK allows programmers to focus on developing application logic, as opposed to building communication mechanisms between transaction processors.

#### Sawtooth Node
Hyperledger Sawtooth organizations run a node that interacts with the Hyperledger Sawtooth network. Each node runs at least three things:

- The main **validator** process
- The **REST service** listening for requests (could be transaction posts or state queries)
- One or more **transaction processors**

Each organization that enters the Hyperledger Sawtooth network runs at least one node, and receives transactions submitted by fellow nodes.

<div style="text-align: center">
![Sawtooth-node](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/274566f591da0f1ee0ea5035f5415a7e/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Sawtooth_node.png)
</div>

___

# Chapter 7. Introduction to Hyperledger Fabric
### Featured Hyperledger Fabric Elements

- **Channels** are data partitioning mechanisms that allow transaction visibility for stakeholders only. Each channel is an independent chain of transaction blocks containing only transactions for that particular channel.
- The **chaincode** (Smart Contracts) encapsulates both the asset definitions and the business logic (or transactions) for modifying those assets. Transaction invocations result in changes to the ledger.
- The **ledger** contains the current world state of the network and a chain of transaction invocations. A shared, permissioned ledger is an append-only system of records and serves as a single source of truth.
- The **network** is the collection of data processing peers that form a blockchain network. The network is responsible for maintaining a consistently replicated ledger.
- The **ordering service** is a collection of nodes that orders transactions into a block.
- The **world state** reflects the current data about all the assets in the network. This data is stored in a database for efficient access. Current supported databases are LevelDB and CouchDB.
- The **membership service provider** (MSP) manages identity and permissioned access for clients and peers.

### Architecture
#### Roles
There are three different types of roles within a Hyperledger Fabric network:

- **Clients**

  Clients are applications that act on behalf of a person to propose transactions on the network.
- **Peers**

  Peers maintain the state of the network and a copy of the ledger. There are two different types of peers: **endorsing** and **committing** peers. However, there is an overlap between endorsing and committing peers, in that endorsing peers are a special kind of committing peers. All peers commit blocks to the distributed ledger.
  - Endorsers simulate and endorse transactions
  - Committers verify endorsements and validate transaction results, prior to committing transactions to the blockchain.
- **Ordering Service**

  The ordering service accepts endorsed transactions, orders them into a block, and delivers the blocks to the committing peers.

#### Consensus
In Hyperledger Fabric, consensus is made up of three distinct steps:

- Transaction endorsement
- Ordering
- Validation and commitment.

These three steps ensure the policies of a network are upheld.

### Transaction Flow

**Step 1:** Within a Hyperledger Fabric network, transactions start out with client applications sending transaction proposals, or, in other words, proposing a transaction to endorsing peers.
<div style="text-align: center">
![Step 1 of Fabric transaction flow](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/21431955acd5b7888ca8d393c94deaf8/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Key_Components_-_Transaction_Proposal.png)
</div>

Client applications are commonly referred to as applications or clients, and allow people to communicate with the blockchain network.

**Step 2:** Each endorsing peer simulates the proposed transaction, without updating the ledger. The endorsing peers will capture the set of **R** ead and **W** ritten data, called **RW Sets**. These RW sets capture what was read from the current world state while simulating the transaction, as well as what would have been written to the world state had the transaction been executed. These RW sets are then signed by the endorsing peer, and returned to the client application to be used in future steps of the transaction flow.
<div style="text-align: center">
![Step 2 of Fabric transaction flow](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/13e5a6a80c0e150f46d45ec0634b86b8/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Transaction_flow_step_2.png)
</div>
Endorsing peers must hold smart contracts in order to simulate the transaction proposals.

**Step 3:** The application then submits the endorsed transaction and the RW sets to the ordering service. Ordering happens across the network, in parallel with endorsed transactions and RW sets submitted by other applications.
<div style="text-align: center">
![Step 3 of Fabric transaction flow](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/b6e7b13624d1cff4152e2c223538c355/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Transaction_flow_step_3.png)
</div>

**Step 4:** The ordering service takes the endorsed transactions and RW sets, orders this information into a block, and delivers the block to all committing peers.
<div style="text-align: center">
![Step 4 of Fabric transaction flow](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/eeb54ce57f8a6018443e22f34b3ebad9/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Transaction_Flow_Step_4.png)
</div>

The ordering service, which is made up of a cluster of orderers, does not process transactions, smart contracts, or maintains the shared ledger. The ordering service accepts the endorsed transactions and specifies the order in which those transactions will be committed to the ledger. The Fabric v1.0 architecture has been designed such that the specific implementation of 'ordering' (Solo, Kafka, BFT) becomes a pluggable component. The default ordering service for Hyperledger Fabric is Kafka. Therefore, the ordering service is a modular component of Hyperledger Fabric.

**Step 5:** The committing peer validates the transaction by checking to make sure that the RW sets still match the current world state. Specifically, that the Read data that existed when the endorsers simulated the transaction is identical to the current world state. When the committing peer validates the transaction, the transaction is written to the ledger, and the world state is updated with the Write data from the RW Set.
<div style="text-align: center">
![Step 5 of Fabric transaction flow](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/b05e5430900cf5e414e307d2f99de088/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Transaction_Flow_Step_5.png)
</div>

If the transaction fails, that is, if the committing peer finds that the RW set does not match the current world state, the transaction ordered into a block will still be included in that block, but it will be marked as invalid, and the world state will not be updated.

Committing peers are responsible for adding blocks of transactions to the shared ledger and updating the world state. They may hold smart contracts, but it is not a requirement.

**Step 6:** Lastly, the committing peers asynchronously notify the client application of the success or failure of the transaction. Applications will be notified by each committing peer.
<div style="text-align: center">
![Step 6 of Fabric transaction flow](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/ba380b73a55eff97c85da3abdc1d86e8/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Transaction_Flow_Step_6.png)
</div>

**Summary:**

Endorsing peers verify the client signature, and execute a chaincode function to simulate the transaction. The output is the chaincode results, a set of key/value versions that were read in the chaincode (Read set), and the set of keys/values that were written by the chaincode. The proposal response gets sent back to the client, along with an endorsement signature. These proposal responses are sent to the orderer to be ordered. The orderer then orders the transactions into a block, which it forwards to the endorsing and committing peers. The RW sets are used to verify that the transactions are still valid before the content of the ledger and world state is updated. Finally, the peers asynchronously notify the client application of the success or failure of the transaction.

#### Transaction Endorsement
A transaction endorsement is a signed response to the results of the simulated transaction. The method of transaction endorsements depends on the endorsement policy which is specified when the chaincode is deployed. An example of an endorsement policy would be "the majority of the endorsing peers must endorse the transaction". Since an endorsement policy is specified for a specific chaincode, different channels can have different endorsement policies.

#### Ordering
In a blockchain network, transactions have to be written to the shared ledger in a consistent order. The order of transactions has to be established to ensure that the updates to the world state are valid when they are committed to the network. Unlike the Bitcoin blockchain, where ordering occurs through the solving of a cryptographic puzzle, or mining, Hyperledger Fabric allows the organizations running the network to choose the ordering mechanism that best suits that network. This modularity and flexibility makes Hyperledger Fabric incredibly advantageous for enterprise applications.

Hyperledger Fabric provides three ordering mechanisms: SOLO, Kafka, and Simplified Byzantine Fault Tolerance (SBFT), the latter of which has not yet been implemented in Fabric v1.0.

- **SOLO** is the Hyperledger Fabric ordering mechanism most typically used by developers experimenting with Hyperledger Fabric networks. SOLO involves a single ordering node.
- **Kafka** is the Hyperledger Fabric ordering mechanism that is recommended for production use. This ordering mechanism utilizes Apache Kafka, an open source stream processing platform that provides a unified, high-throughput, low-latency platform for handling real-time data feeds. In this case, the data consists of endorsed transactions and RW sets. The Kafka mechanism provides a crash fault-tolerant solution to ordering.
- **SBFT** stands for Simplified Byzantine Fault Tolerance. This ordering mechanism is both crash fault-tolerant and byzantine fault-tolerant, meaning that it can reach agreement even in the presence of malicious or faulty nodes. The Hyperledger Fabric community has not yet implemented this mechanism, but it is on their roadmap.

#### Identity Verification
In addition to the multitude of endorsement, validity, and versioning checks that take place, there are also ongoing identity verifications happening during each step of the transaction flow. Access control lists are implemented on the hierarchical layers of the network (from the ordering service down to channels), and payloads are repeatedly signed, verified, and authenticated as a transaction proposal passes through the different architectural components.

## Channels
Channels allow organizations to utilize the same network, while maintaining separation between multiple blockchains. Only the members of the channel on which the transaction was performed can see the specifics of the transaction. In other words, channels partition the network in order to allow transaction visibility for stakeholders only. This mechanism works by delegating transactions to different ledgers. Only the members of the channel are involved in consensus, while other members of the network do not see the transactions on the channel.

![channels](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/b23a6aaaa627620a0ab161c556ff87b3/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Key_Components_Channels.png)

Peers can belong to multiple networks or channels. Peers that do participate in multiple channels simulate and commit transactions to different ledgers. The ordering service is the same across any network or channel.

A few things to remember:

- The network setup allows for the creation of channels.
- The same chaincode logic can be applied to multiple channels.
- A given user can participate in multiple channels.

## State Database

## Smart Contracts
Smart contracts are computer programs that contain logic to execute transactions and modify the state of the assets stored within the ledger. Hyperledger Fabric smart contracts are called chaincode and are written in Go. The chaincode serves as the business logic for a Hyperledger Fabric network, in that the chaincode directs how you manipulate assets within the network.

There are two ways to develop smart contracts with Hyperledger Fabric:

- Code individual contracts into standalone instances of chaincode
- (More efficient way) Use chaincode to create decentralized applications that manage the lifecycle of one or multiple types of business contracts, and let the end users instantiate instances of contracts within these applications.

### Chaincode
When creating a chaincode, there are two methods that you will need to implement:

- **Init**
  Called when a chaincode receives an instantiate or upgrade transaction. This is where you will initialize any application state.
- **Invoke**
  Called when the invoke transaction is received to process any transaction proposals.

As a developer, you must create both an Init and an Invoke method within your chaincode. The chaincode must be installed using the peer chaincode install command, and instantiated using the peer chaincode instantiate command before the chaincode can be invoked. Then, transactions can be created using the peer chaincode invoke or peer chaincode query commands.

## Application Flow Basics
<div style="text-align: center">
![App flow basics](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/a63eaf4dd007c3e65ee63955eccaf5b6/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/fabric-application-flowbasics.png)
</div>
