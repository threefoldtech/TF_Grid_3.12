<h1> Validators and Staking </h1>

<h2> Table of Contents </h2>

- [Introduction](#introduction)
- [Basics of Staking](#basics-of-staking)
- [Staking Principles](#staking-principles)
- [Staking Rewards](#staking-rewards)
- [Simplified Staking Proposition](#simplified-staking-proposition)
- [Node Staking and TFT as Collateral](#node-staking-and-tft-as-collateral)

***

## Introduction

We want to roll out and improve our validator and staking strategy.
***
## Basics of Staking

Staking can happen on

* ThreeFold Guardian Validators
* ThreeFold Farms

Staking is important for the following reasons:

* You show your support for a farmer or a guardian, because you give them your vote of confidence.
* You show your support for the TFGrid by locking in value and receiving rewards for doing so.
***
## Staking Principles

* 9 to 33 validators are operated by ThreeFold Guardians. We call them Guardian Validators.
  * As block creators are elected based on staking, it is not possible to enforce a lower bound. These numbers (9 to 33) would need to be discussed and approved.
* Every TFT token holder can stake their tokens on Guardian Validator(s) or on the Farm(s) of their choice.
* The minimum number of TFT per validator is 2,000,000 TFT.
* The Guardians and Farmers get votes on the TFChain DAO in relation to the weight of the amount of staked tokens on their Validator or Farm.
* A form of punishment (e.g. slashing) should be implemented in the cases where the authority misbehaves. The incites validators to be constantly effective and will allow stakers to support trusted parties (e.g. validators with few or no failures)
  * Potential slashing events:
    * Failure to participate promptly in minting.
    * Normal PoS slashing events.

***

## Staking Rewards

The initial rewards for the staking tokens on a Guardian Validator are

* 10% of TFT that is used for utilization of the grid.
* A commission of 20% on above 10% goes to the Validator Operator = The Guardian.

The initial rewards for the staking tokens on a ThreeFold Farm are the following:

* 10% of TFT is used for utilization of the grid.
* A commission of 20% of the 10% (i.e. 2%) goes to the 3Nodes Operator, i.e. the Farmer.
This is only for the tokens that are staked, the farmer gets other rewards in relation to utilization.

## Simplified Staking Proposition

We propose a simplified staking model for the TFGrid 3.12. 

In this proposition, there would only be one kind of staking on the TFGrid: validator staking. In essence, node staking and farm staking would simply be delegated staking to the validator staking model.

We also propose that each 3Node on the grid would require a given amount of TFT collateral. This TFT collateral would be used as deletaged staking. In this scenario, farmers would have their collateral/staking TFTs delegated to validators. 

Furthermore, the weigth of a given DAO vote would be based on the current shares in validator staking. Since every farmer would have TFT collateral directed as delegated validator staking, every farmer would have a weight on DAO voting.

Since validators get revenues from utilization on the TFGrid, this overall staking model would give a great emphasis and importance on utilization. It would incite members of the whole ecosystem to increase grid utilization.

## Node Staking and TFT as Collateral

When it comes to node staking, we propose the following model with two node staking options: having TFT as collateral and liquid farming rewards, or having locked TFT (non-liquid) until you achive the collateral amount. 

Each 3Node requires a minimum amount of collateral based on their 3Node resources. 

If the farmer stakes the minimum TFT collateral amount for their 3Node, the TFT farming rewards are liquid and thus the amount of TFT they farm at everyone minting period is directly available to them.

If the farmer doesn't stake the minimum TFT collateral amount for their 3Node, the TFT farming rewards are non-liquid and thus the amount of TFT they farm at every minting period is locked until they stake the minimum collateral amount.

* Farming model with 2 options
  * (1) A farmer stakes the minimum TFT for their given 3Node as collateral
    * Monthly farming rewards become liquid (unlocked)
  * (2) A farmer doesn't stake the minimum TFT for their given 3Node as collateral
    * Monthly farming rewards are non-liquid (unlocked) and added to the validator staking pool
      * When the total staked TFT reaches the minimum TFT for their given 3Node as collateral
        * the additional TFT becomes liquid
        * In short, it goes back to option (1).

As a concrete example, say a farmer has a 3Node with XYZ resources and this 3Node requires 10 000 TFT of collateral. The farmer can decide to stake 10 000 TFT as delegated staking to a validator. This 10 000 TFT acts as a collateral for their 3Node. This way, after each minting period, the farmer receives unlocked TFT rewards.

If the farmer doesn't have any TFT or simply doesn't want to stake the 10 000 TFT as collateral, the TFT farming rewards they receive at each minting period would directly go to a delegated staking of a validator. The 3Node would then farm TFT at every minting period and when the 10 000 TFT are staked, any TFT minted after this point would be liquid and unlocked to the farmer.

