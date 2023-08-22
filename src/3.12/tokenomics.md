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
- [Gold Farming, Certified Vendors and Nodes](#gold-farming-certified-vendors-and-nodes)
  - [Certified Parameters](#certified-parameters)
    - [Hardware and Availability Parameters](#hardware-and-availability-parameters)
  - [Certified Boot Loaders](#certified-boot-loaders)
  - [Proof-of-Capacity and Proof-of-Utilization Distinctions](#proof-of-capacity-and-proof-of-utilization-distinctions)

***

# Introduction

The TFGrid will be compatible with two tokenomics policies. The new tokenomics policy will be 100% backward compatible with the currently used farming reward model. This means that farmers would keep on earning the exact same amount of tokens if they choose not to upgrade to the variable model.
***
# Fixed Farming Policy

## Farming

* For all existing farms, the rewards are the same as today. We call this the Fixed Farming reward.
* For every node in the farm, we calculate the amount of CU and SU.
* We also check the amount of NU (public network traffic) and IP (public IPv4) used on the nodes by workloads.
* The uptime over the period is calculated based on the uptime reports in the chain.
* The farming parameters get fetched from the chain. These parameters depend on the certification of the node (certified or not) and the certification of the farm (gold or regular), and are then used to calculate the total maximum payout for the period.
* If the farm is a gold certified farm, the node gets tokens from minting if it has at least 99.80% uptime in the period. For non gold certified farms, the payout is scaled proportional to the node uptime percentage (e.g. 50% uptime -> 50% of the total payout).

## Utilization CU/SU

* 10% goes to the stakers on validators.
* 40% goes to the TF treasury.
* 50% goes to burning. This is more than in version 3.11 and it should largely compensate for minting.

## Utilization Extras

* Utilization extras will not be possible.
***
# Variable Farming Policy (NEW)

Farms can decide to upgrade to Variable Policy, we highly recommend farmers do so.

## Farming

* New tokens (TFT or CHI for v4.0) are only the result of CU/SU farming.
* Rewards are always variable in line to parameters as specified on TFChain.
* Rewards are automatically staked on the 3Node.
* There is a Farmer Staking lockup period of 1 year or 30% utilization, whichever comes first.

## Utilization CU/SU

* 20% goes to farmers for SU/CU utilization.
* 10% goes to the stakers on validators.
* 10% goes to the stakers on farms (for utilization of that farm).
* 10% goes to the TF treasury.
* 50% goes to burning. This is more than in 3.11 and should largely compensate for minting.

## Utilization Extras

As can be defined by the farmers, this represents an extra source of income:

* 70% goes to the farmer for the utilization extras
  * Extra rewards for CU/SU (per node)
  * Extra rewards for Dedicated Nodes (per node)
  * Define prices for NU and IP Addresses (per farm)
* 10% goes to stakers on validators.
* 10% goes to stakers on farms (for utilization of that farm).
* 10% goes to the TF treasury.

# Gold Farming, Certified Vendors and Nodes

We propose to keep the certified vendors and nodes as well as gold farming programs as they are currently for TFGrid 3.12 while we prepare the following.

In the future, the certified nodes and gold farming programs would be controlled by the DAO. The principle would be that the DAO votes for strict parameters to be eligible for either certified nodes farming and/or gold farming.

The parameters would be as objective as possible and would be testable by benchmarks and metrics.

A 3Node with all certified hardware parameters would be a complete certified hardware 3Nodes. They can be either built by DIY farmers, or bought by certified vendors. The certified vendors would be elected by the DAO and be able to distribute certified boot loaders. Certified vendors could sell 3Nodes with complete certified hardware or partial certified hardware: it would be up to them to decide which product they offer and this could diverse their service offer as well as propose different entry level certified 3Nodes for potential farmers.

To get the status of a gold farm, it would thus be needed to have both certified hardware parameters (e.g. SSD, RAM, CPU, etc.) as well as certified availability parameters (e.g. uptime, bandwidth).


## Certified Parameters

The following parameters could be tested periodically to ensure that farmers have eligible nodes or farms to get the certified nodes and/or gold farming certifications:

* Hardware parameters
  * CPU speed
  * RAM speed
  * SSD speed
* Availability parameters
  * Uptime
  * Bandwidth

For example, we already measure the total uptime per minting period. We could then build an interface, most certainly on the ThreeFold Dashboard, where users could see the total uptimes (based on different periods, e.g. per week, per month, per year, etc.), to see how the nodes have performed in the past.

What we propose is that nodes could be certified individually for different parameters. This could be more versatile. As a simple example, say a user needs a node that has high uptime to keep their Telegram bot alive. In this case, this type of workload doesn't require lots of compute power nor high bandwidth. So the user could choose a node with certified uptime, which means very high availability. This would ensure an efficient workload for their specific needs.

When a node unlocks a given certified parameter, they would earn more TFT by a given factor, chosen by the DAO. For example, having a certified high CPU speed would give 5% more TFT rewards at the proof-of-capacity stage. Those additional rewards based on given certified parameters would be decided by the DAO.

The main advantage of this method is that it would be mainly automated once the DAO decides the different bonus factors for the different certified parameters. Farmers would have their 3Nodes checked and get additional rewards at the PoC stage if their 3Nodes perform well in given certified parameters categories.

To implement these automated certified parameters testing, we need both the testing mechanism and the public interface to present those results to the users.

### Hardware and Availability Parameters

Considering hardware and availability parameters, there could be different levels. A simple example can be found in the [Uptime and Farming Rewards](../3.12/uptime_farming.md) page. Bandwidth could also have different levels and respective farming rewards.

As discussed, regions where Internet bandwidth and/or electricity are scare or less optimal could be organized and parametrized by regional Internets. This would thus be develop at a later stage of the TFGrid, potentially in TFGrid 4.0.

The parameters levels would be decided by the DAO.

## Certified Boot Loaders

Certified nodes would need certified boot loaders. This ensures that the Zero-OS running on the 3Node is the same as the Zero-OS on the ThreeFold Hub. The question is: who would offer such boot loaders?

We propose that Guardians could distribute certified boot loaders to farmers. Two parts would be signed: (1) the secure boot keys that get loaded in the BIOS, and (2) the signed boot loader. We note that there would be one signed boot loader per farm.

Currently the fees are per farm. Ideally, we would have certified nodes on chain and make those fees and certification per node instead of per farm. This would give more versatility and resilience to the system.

This certified boot loader could be done with multi-signature threshold signing by the guardians. For example, a minimum of 10 Guardians could be needed to certify a node (or a farm) enabling the farmer to get a certified boot loader.

## Proof-of-Capacity and Proof-of-Utilization Distinctions

As a general observation, proof-of-capacity (PoC) is related to the offer phase of the market, where farmers get rewarded simply by offering compute, storage and network units on the ThreeFold Grid, while proof-of-utilization (PoU) is related to the demand phase of the market, where farmers get rewarded when users use their 3Nodes to deploy workloads.

It can be noted that, in this case, PoC is a passive rewards system while PoU is an active rewards system. In the new tokenomics variable farming policy, farmers can actively decide to get more TFT during the PoU/demand phase.

Considering certified nodes and certified indivual parameters, farmers would get more TFT rewards at the PoC/offer phase by having bonus rewards for their certification without needing any workloads to be deployed on their 3Nodes. This is why we call this passive rewards.

When farmers get utilization on their nodes, with the variable farming policy, they can ask more rewards if they think their 3Nodes parameters are worth more. This is why we call this active rewards, as you get more rewards when there is active utilization on the grid.
