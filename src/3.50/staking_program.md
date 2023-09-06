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
- [Rewards Distribution Examples](#rewards-distribution-examples)
  - [Remark on Staking and Grid Revenues](#remark-on-staking-and-grid-revenues)
  - [Validator Staking](#validator-staking)
  - [Farmer Staking](#farmer-staking)
  - [Delegator Staking](#delegator-staking)
- [Parameters to Consider](#parameters-to-consider)
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
    * compute, storage, network units to the grid

## Rewards

The are two main type of rewards on the TFGrid.

* Proof-of-capacity rewards
    * based on basic 3Node specs
* Proof-of-utilization rewards
    * based on workloads deployed on 3Node

## Importance of Staking

Staking is an important part of the overall ThreeFold ecosystem for the following reasons:

* Farming nodes provide the basic resources on the grid
  * 3Nodes offering compute, storage and network units managed by farmers (farm operators)
* Validator nodes secure the transaction on the grid 
  * Validator workloads deployed on TFGrid managed by validators
* Staking enables voting power in the TF DAO to improve and manage the grid
* Staking enables staking rewards based on the proportional TFT staked

## Staking Principles

The Staking program consists of 200,000,000 TFT being used in Proof-of-stake to validate transactions on the TFGrid. 100,000,000 comes from validator staking and 100,000,000 comes from the staking pool. 

The staking pool contributes equally to validator staking and is distributed equally to each validator node based proportionally on validator staking TFT amount. The staking pool consists of 50,000,000 TFT staked from farm staking/node collateral and 50,000,000 TFT staked from delegator staking.

## Staking Rewards Distribution

Staking rewards consistutes the 20% of Proof-of-utilization revenues from the TFGrid. Staking rewards are proportional to the amount of TFT staked. They follow the rules:

* 2% goes to validator staking
* 2% goes to farm staking
* 16% goes to all stakers (validators, farmers and delegators)

We note that before the staking pool reaches 100 millions TFT, the validators will earn most of the 16% PoU revenues (proportional to TFT staked). This compensates for the delay in validator staking.

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

* Individual-staked TFT (istft) = TFT staked per individual staker

* Group-staked TFT (gstft)= TFT staked by all the group
  * validator staking (gtf = 100,000,000)
  * farmer staking (gtf = 50,000,000)
  * all staking = validator+farmer+delegator (gtf = 200,000,000)

* TFT staked ratio (rtft) =  itft / gtft
  * validator (vsrtft)
    * itft / 100,000,000
  * farmer (fsrtft)
    * itft / 50,000,000
  * all-staking (asrtft)
    * itft / 200,000,000

We propose the following staking rewards distribution:

* Rewards distribution per staker types
  * Validator operators
    * Validator staking rewards
      * validator staking staked ratio * 2% * PoU revenues
    * Delegated Staking rewards
      * all-staking staked ratio * 16% * PoU revenues
  * Farm operators
    * Farmer staking rewards
      * farmer staked ratio * 2% * PoU revenues
    * Delegated Staking rewards
      * all-staking staked ratio * 16% * PoU revenues
  * Non-operator stakers
    * Delegated Staking rewards
      * all-staking staked ratio * 16% * PoU revenues

The equations for the monthly staking rewards are thus the following:

* monthly staking rewards
  * validator monthly staking rewards = TFT validator staked ratio * 2% * PoU monthly revenues + TFT all-staking staked ratio * 16% * PoU monthtly revenues
  * farmer monthly staking rewards = TFT farmer staked ratio * 2% * PoU monthly revenues + TFT all-staking staked ratio * 16% * PoU monthtly revenues 
  * delegator monthly staking rewards = TFT all-staking staked ratio * 16% * PoU monthtly revenues

## Voting Power

* The three types of stakers (validators, farmers and delegators) get voting power on the TFChain DAO based on the amount of staked tokens
* Since 50% of the TFT staked is within the validator staking and 50% of the TFT staked is within the staking pool staking (farmer staking and delegator staking)
  * The staking program provides a balance between the validator staking and staking pool staking

## Slashing

* A form of punishment (i.e. validator-only slashing) will be implemented in the cases where the validators misbehaves. 
* The incites validators to be constantly effective and will allow stakers to support trusted parties (e.g. validators with few or no failures)
* Potential slashing events:
  * Failure to participate promptly in minting.
  * Normal PoS slashing events.

## Node Collateral Program: Concept and Examples

We present the overall concept of node collateral.

To farm TFT, a farmer connects a 3Node to the ThreeFold Grid. Each 3Node needs collateral, we call this node collateral. The node collateral amount in TFT is used for delegated staking to the staking pool. The staking pool distributes equally the TFT to the validator nodes in the form of delegated staking. In return, farmers share part of the PoU revenues and voting power for the DAO.

### Terminology

To efficiently and quickly discuss the node collateral program, we define some terms.

* Resource units
  * compute unit (cru) = vcores
  * memory unit(mru) = GB of RAM
  * storage unit (sru) = GB of SSD or HDD
  * farming unit (fru) = min(cru,mru/8,sru/100)
* Total TFT to stake (sTFT)
* Total farming units on the grid (tfru)
* Collateral ratio (cr) = sTFT / tfru
* Server farming unit (sfru) =  total farming units of one node
* Minimum collateral amount (mca) = cr * sfru
* Staking average percentage return (sAPR)

### Node Collateral Calculations

In this model, there is a total of 50 millions TFT staked as node collaterals.

We show a simple example with 50 millions TFT and a typical server of 32 vcores, 256 GB of RAM and 4 TB of SSD. This server has thus 32 farming units (sfru).

The collateral ratio is obtained by dividing the total TFT to stake by the total farming units on the grid currently.

| Whole Network                             | Quantities | Typical Server (TS)                        | Quantities |
| ----------------------------------------- | ---------- | ------------------------------------------ | ---------- |
| Total TFT to stake (sTFT)                 | 50000000   | cru                                        | 32         |
| total cru                                 | 62419      | mru                                        | 256        |
| total mru                                 | 402100     | sru                                        | 4000       |
| total sru                                 | 9445009    |                                            |            |
| total fru (tfru) = min(cru,mru/8,sru/100) | 50262.5    | server fru (sfru) = min(cru,mru/8,sru/100) | 32         |
| collateral ratio (cr=sTFT/tfru)           | 994.8      | min collateral amount (mca)                | 31832.9    |

In this example, each farming unit (fru) would need around 995 TFT staked. If a farmer doesn't want to put staking as collateral, the TFT farmed is locked until it achieves the minimum staking as collateral amount, or until the 3Node farms 2 years or until the 3Node has 30% utilization for a given period of time.

| TS Parameters                               | Quantities |
| ------------------------------------------- | ---------- |
| TS monthly farming rewards (mfr)            | 1912.5     |
| TS minimum collateral amount (mca=cr\*sfru) | 31832.9    |
| Staking APR (sAPR = mca/mfr)                | 16.6       |

With the above example, the TFT to stake as collateral for the proposed typical server would be around 32,000 TFT. The staking return on investment (APR) would be around 17 months. So for example, if the farmer doesn't provide collateral at the start, it will take 17 months to the 3Node to generate the minimum collateral amount.

## Rewards Distribution Examples

We present here some simulators on validator staking. 

### Remark on Staking and Grid Revenues

As we will see with the following examples, staking APR increases as the TFGrid utilization revenues increase. This is by design with the staking program.

The whole idea behind this is that every staker in the TF Ecosystem will benefit when utilization increases on the TFGrid. This will have the effect of uniting every ThreeFolders with the common goal of expanding the TFGrid in utilization.

### Validator Staking

| Table 1: Validator staking    |            |            |            |            |
| ----------------------------- | ---------- | ---------- | ---------- | ---------- |
| TFT Staked Validators         | 100000000  | 100000000  | 100000000  | 100000000  |
| TFT Staked Staking Pool       | 100000000  | 0          | 100000000  | 0          |
| Total TFT staked (stft)       | 200000000  | 100000000  | 200000000  | 100000000  |
| Individual TFT staked (itft)  | 2000000    | 2000000    | 2000000    | 2000000    |
| Grid monthly revenues (USD)   | 8000       | 8000       | 16000      | 16000      |
| Grid monthly revenues (TFT)   | 1230769.23 | 1230769.23 | 2461538.46 | 2461538.46 |
| Monthly rewards validators    | 492.31     | 492.31     | 984.62     | 984.62     |
| Monthly rewards all stakers   | 1969.23    | 3938.46    | 3938.46    | 7876.92    |
| Total monthly rewards         | 2461.54    | 4430.77    | 4923.08    | 8861.54    |
| Total yearly rewards          | 29538.46   | 53169.23   | 59076.92   | 106338.46  |
| Staking yearly APR in TFT (%) | 1.48       | 2.66       | 2.95       | 5.32       |

### Farmer Staking

| Table 2: Farmer staking        |            |            |
| ------------------------------ | ---------- | ---------- |
| TFT Staked Farmers             | 50000000   | 50000000   |
| TFT Staked Staking Pool        | 100000000  | 100000000  |
| Total TFT staked (stft)        | 200000000  | 200000000  |
| Individual TFT staked (itft)   | 31832.9    | 31832.9    |
| Grid monthly revenues (USD)    | 8000       | 16000      |
| Grid monthly revenues (TFT)    | 1230769.23 | 2461538.46 |
| Monthly rewards (from the 2%)  | 15.67      | 31.34      |
| Monthly rewards (from the 16%) | 31.34      | 62.69      |
| Total monthly rewards          | 47.01      | 94.03      |
| Total yearly rewards           | 564.18     | 1128.35    |
| Staking yearly APR in TFT (%)  | 1.77231    | 3.54462    |

### Delegator Staking

| Table 3: Delegator staking     |            |            |
| ------------------------------ | ---------- | ---------- |
| Total TFT staked (stft)        | 200000000  | 200000000  |
| Individual TFT staked (itft)   | 50000      | 50000      |
| Grid monthly revenues (USD)    | 8000       | 16000      |
| Grid monthly revenues (TFT)    | 1230769.23 | 2461538.46 |
| Monthly rewards (from the 16%) | 49.23      | 98.46      |
| Total yearly rewards           | 590.77     | 1181.54    |
| Staking yearly APR in TFT (%)  | 1.18154    | 2.36308    |

## Parameters to Consider

There are some parameters to consider when discussing this staking program. 

One important parameter is the collateral ratio. In this example, we used 995 TFT per farming unit as a collateral ratio. This number could be decided by the TFDAO based on the situation of the TFGrid, the grid utilization, the TFT price (see below) and other evolving factors.

There are currently 3 distinct prices related to TFT:

1. TFT market price: 0.0066$USD
2. TFT TFChain price: 0.01$USD
3. TFT farming rewards price: 0.08$USD

(Reference: As of 06-09-23)

This should be taken into account when considering the collateral ratio.

At the current market price, it would cost a farmer around 210$USD to pay for the minimum collateral amount of the server stated as an example (32vcores, 256gb ram, 3.2TB SSD).
If the price of TFT goes back to 8 cents, it would cost 3200$ of collateral for the same server. That being said, it would still be around 17 months to farm it, as the TFT farming rewards is set to 8 cents in both cases.

We thus propose that the TFDAO vote for a change in the collateral ratio when the TFT market price goes beyond 8 cents and the TFT farming rewards price of 8 cents is updated in line with Proof-of-capacity rewards.

Until then, it will incite farmers to acquire the minimum collateral amount for their farm at a good price, while providing them PoU staking rewards and voting power to the TFDAO.

## Questions and Feedback

We do welcome greatly feedback on this proposition. It is not an official ThreeFold position, but an invitation to discuss parameters and concepts for the future 3.50 TFGrid release and the associated staking program.