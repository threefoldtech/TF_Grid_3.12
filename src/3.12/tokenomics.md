<h1> Tokenomics 3.12 </h1> 

<h2> Table of Contents </h2>

- [Introduction](#introduction)
- [Fixed Farming Policy](#fixed-farming-policy)
  - [Farming](#farming)
  - [Utilization CU/SU](#utilization-cusu)
  - [Utilization Extras](#utilization-extras)
- [Variable Farming Policy (NEW)](#variable-farming-policy-new)
  - [Farming](#farming-1)
  - [Utilization CU/SU](#utilization-cusu-1)
  - [Utilization Extras](#utilization-extras-1)
- [Certified Nodes and Gold Farming](#certified-nodes-and-gold-farming)
  - [Certified Parameters](#certified-parameters)
- [Certified Boot Loaders](#certified-boot-loaders)
  - [Hardware Failures](#hardware-failures)
    - [Hardware Failures Workarounds](#hardware-failures-workarounds)
  - [Proof-of-Capacity and Proof-of-Utilization](#proof-of-capacity-and-proof-of-utilization)

***

## Introduction

The TFGrid will be compatible with two tokenomics policies. The new tokenomics policy will be 100% backward compatible with the currently used farming reward model. This means that farmers would keep on earning the exact same amount of tokens if they choose not to upgrade to the variable model.
***
## Fixed Farming Policy

### Farming

* For all existing farms, the rewards are the same as today. We call this the Fixed Farming reward.
* For every node in the farm, we calculate the amount of CU and SU.
* We also check the amount of NU (public network traffic) and IP (public IPv4) used on the nodes by workloads.
* The uptime over the period is calculated based on the uptime reports in the chain.
* The farming parameters get fetched from the chain. These parameters depend on the certification of the node (certified or not) and the certification of the farm (gold or regular), and are then used to calculate the total maximum payout for the period.
* If the farm is a gold certified farm, the node gets tokens from minting if it has at least 99.80% uptime in the period. For non gold certified farms, the payout is scaled proportional to the node uptime percentage (e.g. 50% uptime -> 50% of the total payout).

### Utilization CU/SU

* 10% goes to the stakers on validators.
* 40% goes to the TF treasury.
* 50% goes to burning. This is more than in version 3.11 and it should largely compensate for minting.

### Utilization Extras

* Utilization extras will not be possible.
***
## Variable Farming Policy (NEW)

Farms can decide to upgrade to Variable Policy, we highly recommend farmers do so.

### Farming

* New tokens (TFT or CHI for v4.0) are only the result of CU/SU farming.
* Rewards are always variable in line to parameters as specified on TFChain.
* Rewards are automatically staked on the 3Node.
* There is a Farmer Staking lockup period of 1 year or 30% utilization, whichever comes first.

### Utilization CU/SU

* 20% goes to farmers for SU/CU utilization.
* 10% goes to the stakers on validators.
* 10% goes to the stakers on farms (for utilization of that farm).
* 10% goes to the TF treasury.
* 50% goes to burning. This is more than in 3.11 and should largely compensate for minting.

### Utilization Extras

As can be defined by the farmers, this represents an extra source of income:

* 70% goes to the farmer for the utilization extras
  * Extra rewards for CU/SU (per node)
  * Extra rewards for Dedicated Nodes (per node)
  * Define prices for NU and IP Addresses (per farm)
* 10% goes to stakers on validators.
* 10% goes to stakers on farms (for utilization of that farm).
* 10% goes to the TF treasury.

## Certified Nodes and Gold Farming

We propose to keep the certified nodes and gold farming programs as they are currently for TFGrid 3.12 while we prepare the following.

In the future, the certified nodes and gold farming programs would be controlled by the DAO. The principle would be that the DAO votes for strict parameters to be eligible for either certified nodes farming and/or gold farming.

The parameters would be as objective as possible and would be testable by benchmarks and metrics.

### Certified Parameters

The following parameters could be tested periodically to ensure that farmers have eligible nodes or farms to get the certified nodes and/or gold farming certifications:

* CPU speed
* RAM speed
* SSD speed
* Total uptime
  * per month
  * per year
* Total bandwidth

For example, we already measure the total uptime per minting period. We could then build an interface, most certainly on the ThreeFold Dashboard, where users could see the total uptimes (based on different periods, e.g. per week, per monht, per year, etc.), to see how the nodes have performed in the past.

What we propose is that nodes could be certified for different parameters individually. This could be more resilient and versatile. As a simple example, say a user needs a node that has high uptime to keep their Telegram bot alive. In this case, this type of workload doesn't require lots of compute power nor high bandwidth. So the user could choose a node with certified uptime, which means very high availability. This would ensure an efficient workload for their specific needs.

When a node unlocks a given certified parameter, they would earn more TFT by a given factor, chosen by the DAO. For example, having a certified high CPU speed would give 5% more TFT rewards at the proof-of-capacity stage. Those additional rewards based on given certified parameters would thus be decided by the DAO.

The main advantage of this method is that it would be mainly automated once the DAO decides the bonus factor. Farmers would have their 3Nodes checked and get additional rewards at PoC stage if their 3Nodes perform well in given certified parameters categories.

To implement these automated certified parameters testing, we need both the testing mechanism and the public interface to present those results to the users.

## Certified Boot Loaders

Certified nodes would need certified boot loaders. This ensures that the Zero-OS running on the 3Node is the same as the Zero-OS on the ThreeFold Hub. The question is: who would offer such boot loaders?

We propose that Guardians could distribute certified boot loaders to farmers. Two parts would be signed: (1) the secure boot keys that get loaded in the BIOS, and (2) the signed boot loader. We note that there would be one signed boot loader per farm.

Currently the fees are per farm. Ideally, we would have certified node on chain and make those fees and certification per node. 

This certified boot loader could be done with multi-signature threshold signing by the guardians. For example, a minimum of 10 guardians would be needed to certified a node (or a farm) enabling the farming to get a certified boot loader.

### Hardware Failures

The current situation already takes into account hardware failures and ways to incite farmers to avoid such situations. In the current scenario, if hardware fails while the 3Node has some workloads, the farmers lose the rewards for the whole month. This incite farmers to use high-quality hardware that will not fail during deployment. This is written in the minting code.

#### Hardware Failures Workarounds

There can be many ways to work around hardware failures depending on the situation. While all potential issues and situations are not yet covered and fixed, we can develop on the current situation.

Currently, if the SSD of a 3Node fails, the user loses the data. Depending on the type of workload, a user could simply decide to deploy on another node. Users could also have backups available in order to avoid losing the data.

Some workloads can be self-healing by design. For example, if a user runs a Jitsi instance and the 3Node fails, the user could simply redeploy on another 3Node and the workload would more or less be as effective. As another example, if a user deploys a Nextcoud instance and enabled a redundant backup on another 3Node, they could simply redeploy on functioning 3Node and transfer the data to this new 3Node.

This type of thinking is to show that there are ways to circumvent or deal with hardware failures with deployments themselves.

### Proof-of-Capacity and Proof-of-Utilization

As a general observation, proof-of-capacity (PoC) is related to the offer phase of the market, where farmers get rewarded simply by offering compute, storage and network units on the ThreeFold Grid, while proof-of-utilization (PoU) is related to the demand phase of the market, where farmers get rewarded when users use their 3Nodes to deploy workloads.

It can be noted that, in this case, PoC is a passive rewards system while PoU is an active rewards system. In the new tokenomics variable farming policy, farmers can actively decide to get more TFT during the PoU/demand phase.

Considering certified nodes and certified indivual parameters, farmers would get more TFT rewards at the PoC/offer phase by having bonus rewards for their certification without needing any workloads to be deployed on their 3Nodes. This is why we call this passive rewards.

When farmers get utilization on their nodes, with the variable farming policy, they can ask more rewards if they think their 3Nodes parameters are worth more, in this case, the certified parameters.
