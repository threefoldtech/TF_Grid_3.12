<h1> Staking Program </h1>

<h2> Table of Contents </h2>

- [Introduction](#introduction)
- [3 Types of Staking](#3-types-of-staking)
- [Operators](#operators)
- [Rewards](#rewards)
- [Importance of Staking](#importance-of-staking)
- [Staking Principles](#staking-principles)
- [Staking Rewards Distribution](#staking-rewards-distribution)
- [Attributes of Stakers](#attributes-of-stakers)
- [Validator Staking and Staking Pool](#validator-staking-and-staking-pool)
- [PoU Rewards Staking Program](#pou-rewards-staking-program)
- [Rewards Distribution per Staker Types](#rewards-distribution-per-staker-types)
- [Voting Power](#voting-power)
- [Slashing](#slashing)
- [Node Collateral Program: Concept and Examples](#node-collateral-program-concept-and-examples)
  - [Terminology](#terminology)
  - [Node Collateral Calculations](#node-collateral-calculations)
- [Questions and Feedback](#questions-and-feedback)

***

## Introduction

Here is a staking program proposition for the TFGrid 3.50.

***

## 3 Types of Staking

* 3 types of staking
  * (1) validator staking
    * made by validator operator (validator)
  * (2) farmer staking 
    * made by farm operator (farmer)
  * (3) delegator staking 
    * made by non-operator (delegator)
    
* Bicameral chamber staking
  * The total staking program, and thus staking rewards and voting power, is divided in two:
    * validator staking
    * staking pool staking (delegated staking to validator staking)
      * farm staking
      * delegator staking

## Operators

* Validator operators  
  * operate validator nodes that process transactions on the grid

* Farm operators
  * farmers offer 3Nodes resources on the TFGrid
    * compute, storage, network units to the ThreeFold Grid

## Rewards

The are two main type of rewards on the TFGrid.

* Proof-of-capacity rewards
    * based on basic 3Node specs
* Proof-of-utilization rewards
    * based on workloads deployed on 3Node

## Importance of Staking

Staking is an important part of the overall ThreeFold ecosystem for the following reasons:

* Farming nodes provide the basic resources on the grid
  * 3Nodes offering compute, storage and network units managed by farmers (farm operator)
* Validator nodes secure the transaction on the grid 
  * Validator workloads deployed on TFGrid managed by validators
* Staking enables voting power in the TF DAO to improve and manage the grid
* Staking enables staking rewards based on the proportional TFT staked

## Staking Principles

The Staking program consists of 200,000,000 TFT being used in Proof-of-stake to validate transactions on the tfgrid. 100,000,000 comes from validator staking and 100,000,000 comes from the staking pool. 

The staking pool contributes equally to validator staking and is distributed equally to each validator node based proportionally on validator staking TFT amount. The staking pool consists of 50,000,000 TFT staked from farm staking/node collateral and 50,000,000 TFT staked from delegator staking.

## Staking Rewards Distribution

Staking rewards consistutes the 20% of Proof-of-utilization revenues from the TF Grid. Staking rewards are proportional to the amount of TFT staked. They follow the rules:

* 2% goes to validator staking
* 2% goes to farm staking
* 16% goes to all stakers (validators, farmers and delegators)

## Attributes of Stakers

* Validator staking
  * each validator stakes 2,000,000 tft
  * validator nodes proceed transactions on the TFGrid
  * there is individual slashing to validator node rewards when a node misbehave (doesn't affect staking pool rewards)
* Farmer staking
  * Every farmer must stake a minimum collateral TFT amount for each node to the staking pool
    * the farming rewards are locked (illiquid) until the minimum collateral amount is achieved
    * OR the 3Node farms for 2 years
    * OR the 3Node has more than 30% utilization for a given period of time
* Delegator staking
  * Any TFT token holder can become a delegator and stake their tokens to the staking pool

## Validator Staking and Staking Pool

Validators operates a validator node and stake 2,000,000 each. In total, 100,000,000 TFT is staked to validator staking.

The staking pool consists of 100,000,000 TFT delegated to validator staking. The staking pool distributes staking power equally to all validator nodes. 

* The total TFT staked is 200,000,000
  * Validator staking (100,000,000 TFT)
    * 50 validators stake each 2,000,000 to validator staking
  * Staking pool (100,000,000 TFT)
    * Farmer staking
      * farmers stake in total 50,000,000 TFT to the staking pool
    * Delegator staking
      * delegators stake in total 50,000,000 TFT to the staking pool



## PoU Rewards Staking Program

* 20% of the Proof-of-Utilization (PoU) rewards of the grid goes to the staking program
  * 2% of PoU rewards
    * distributed to all validators proportional to staked TFT (validator node)
  * 2% of PoU rewards
    * distributed to all farmers proportional to staked TFT (node collateral)
  * 16% of PoU rewards
    * distributed to all stakers (validators, farmers, delegators) proportional to staked TFT

## Rewards Distribution per Staker Types

We first define some terms:

* Total stakers = farm operators + validator operators + non-operators stakers

* individual staked ratio = TFT staked per individual staker / TFT staked total  

We propose the following staking rewards distribution:

* Rewards distribution per staker types
  * Validator operators
    * Validator staking rewards
      * individual staked ratio * 2% * PoU rewards
    * Delegated Staking rewards
      * individual staked ratio * 16% * PoU rewards
  * Farm operators
    * Farmer staking rewards
      * individual staked ratio * 2% * PoU rewards
    * Delegated Staking rewards
      * individual staked ratio * 16% * PoU rewards
  * Non-operator stakers
    * Delegated Staking rewards
      * individual staked ratio * 16% * PoU rewards

## Voting Power

* The three types of stakers (validators, farmers and delegators) get vote power on the TFChain DAO in relation to the weight of the amount of staked tokens.

## Slashing

* A form of punishment (e.g. validator-only slashing) will be implemented in the cases where the validators misbehaves. The incites validators to be constantly effective and will allow stakers to support trusted parties (e.g. validators with few or no failures)
  * Potential slashing events:
    * Failure to participate promptly in minting.
    * Normal PoS slashing events.

## Node Collateral Program: Concept and Examples

We present the overall concept of node collateral.

To farm TFT, a farmer connects a 3Node to the ThreeFold Grid. Each 3Node needs collateral, we call this node collateral. The node collateral amount in TFT is used for delegated staking to the staking pool. The staking pool distributes equally the TFT to the validator nodes in the form of delegated staking. In return, farmers share part of the PoU revenues and voting power for the DAO.

### Terminology

To efficiently and quickly discuss the node collateral program, we define some terms.

* Minimum collateral amount (MCA) = collateral ratio * farming unit (per node)
* Collateral ratio (CR) = TFT to staked / farming unit (per node)
* Server farming unit (sfru) =  \# farming unit per node
* Resource units
  * compute unit (cru) = vcores
  * memory unit(mru) = GB of RAM
  * storage unit (sru) = GB of SSD or HDD
  * farming unit (fru) = min(cru,mru/8,sru/100)

### Node Collateral Calculations

In this model, there is a total of 50 millions TFT staked as node collaterals.

Let us call farming unit (fru) the mininum of the ratio 8GB of RAM/1 vcore/100 GB of SSD.

We show a simple example with 50 millions TFT and a typical server of 32 vcores, 256 GB of RAM and 4 TB of SSD.

| **Whole Network**                                       | **Quantities** | **Typical Server (TS)**                    | **Quantities** |
| ------------------------------------------------------- | -------------- | ------------------------------------------ | -------------- |
| Total TFT to stake (sTFT)                               | 50000000       | cru                                        | 32             |
| total cru                                               | 62419          | mru                                        | 256            |
| total mru                                               | 402100         | sru                                        | 4000           |
| total sru                                               | 9445009        |                                            |                |
| total fru (tfru) = min(cru,mru/8,sru/100)               | 50262.5        | server fru (sfru) = min(cru,mru/8,sru/100) | 31.88          |
| collateral ratio (CR) (Staking TFT per fru (sTFT/tfru)) | 994.78         | min collateral amount                      | 31713.5864     |                   |            |

In this example, each farming unit (fru) would need around 995 TFT staked. If a farmer doesn't want to put staking as collateral, the TFT farmed is locked until it achieves the minimum staking as collateral amount, or until the 3Node farms 2 years or until 30% utilization for a given period of time.

| TS Parameters             | Quantities |
| ------------------------- | ---------- |
| TS monthly farming rewards (mfr)     | 1912.5     |
| TS Minimum Collateral amount (CR*sfru)      | 31708.53   |
| Staking ROI (SROI = MCA/mfr) | 16.58      |

With the above example, the TFT to stake as collateral for the proposed typical server would be around 32,000 TFT. The staking return on investment (SROI) would be around 17 months. So for example, if the farmer doesn't provide collateral at the start, it will take 17 months to the 3Node to generate the minimum collateral amount.

## Questions and Feedback

We do welcome greatly feedback on this proposition. It is not an official ThreeFold position, but an invitation to discuss parameters and concepts for the future 3.50 TFGrid release.