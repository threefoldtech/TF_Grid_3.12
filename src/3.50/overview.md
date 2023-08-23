<h1> TFGrid 3.50 Overview </h1>

<h2> Table of Contents </h2>

- [Introduction](#introduction)
- [Daily Minting on Chain](#daily-minting-on-chain)
- [More Income for Farmers](#more-income-for-farmers)
- [Farmers Information \& Reputation Management](#farmers-information--reputation-management)
- [Introduction of Staking on Validators and Farms:](#introduction-of-staking-on-validators-and-farms)
- [Features Removal](#features-removal)

***

## Introduction

The major goal of TFGrid 3.50 is to propose a major decentralization upgrade to ThreeFold.

***

## Daily Minting on Chain

* We implement the minting as a script which is run on (e.g.) 9 guardian nodes. It aims to achieve a consensus (log the minting in the chain). If the consensus is passed, then a multisignature account creates the tokens (from the 9 guardians). We also need to make sure double-spending is never possible.
***
## More Income for Farmers

TFGrid 3.50 leads to more income for Farmers.

* Those changes lead to a lot of extra income for farmers.
* Farmers can add extra reward for CU/SU (per node).
  1. Since a farm may have varying quality of CU/SU for different nodes, this parameter is set for each node.
* Farmers can add extra reward for Dedicated Nodes (per node).
  1. Same logic as above.
* Farmers can define prices for NU and IP Addresses (per farm).
  1. This is not an extra. The price is 100% defined by each farmer for their farm.
* Farmers make money on utilization
* Note: Default prices would be decided by the DAO.

***

## Farmers Information & Reputation Management

* Farmers can put a link in TFChain to describe their farm (e.g. leading to a website page or the like). This link is not the TFChain content itself, but a way for the farmers to present their farms.
 * Farmers can specify their bandwidth, if their farm is in a quality datacenter, and more, as structured info in TFChain. The Farmerbot could also check this information (bandwidth), as the TFChain can not immediately validate this information.
 * Stakers need to select the Farmers they want to support and help.
 * Farmers make money on staking support from their own communities or their own TFT.
   1. More information below. Staking on farms has 10% for utilization and 20% of this 10% goes to the Farmer (i.e. 2%).
***
## Introduction of Staking on Validators and Farms:
  
* Use Staking for TF Farms and TF Validators to define voting power, as well as distribute rewards for the community that is showing support for ThreeFold.
  1. This means that current voting power based on farm size is removed. Farmed tokens for farms are staked automatically. A farmer needs to un-stake to get the tokens. This might only happen after the lock.
***
## Features Removal

We remove features which cause complications and confusion:

* The solution provider & sales channel features will be removed.
* The certified farmer concept is no longer needed, because farmers can define their own additional reward income. This includes gold certified farming.
  1. Farmers can advertise their uptimes on their website. Uptime is also available on the TF Dashboard. High uptime farms would be seen as more reliable (e.g. the 99.8% required previously for certified farms).
  2. To discuss: add a feature in the TF Dashboard for users to see different uptime levels (e.g. past month, past 3 months, past 12 months, since the start of the farm, etc.).