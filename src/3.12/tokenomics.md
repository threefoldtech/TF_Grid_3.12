## TOKENOMICS 3.12

The TFGrid will be compatible with two tokenomics policies. The new tokenomics policy will be 100% backward compatible with the currently used farming reward model. This means that farmers would keep on earning the exact same amount of tokens if they choose not to upgrade to the variable model.

#### FIXED FARMING POLICY

##### Farming

* For all existing farms, the rewards are the same as today. We call this the Fixed Farming reward.
* For every node in the farm, we calculate the amount of CU and SU.
* We also check the amount of NU (public network traffic) and IP (public IPv4) used on the nodes by workloads.
* The uptime over the period is calculated based on the uptime reports in the chain.
* The farming parameters get fetched from the chain. These parameters depend on the certification of the node (certified or not) and the certification of the farm (gold or regular), and are then used to calculate the total maximum payout for the period.
* If the farm is a gold certified farm, the node gets tokens from minting if it has at least 99.80% uptime in the period. For non gold certified farms, the payout is scaled proportional to the node uptime percentage (e.g. 50% uptime -> 50% of the total payout).

##### Utilization CU/SU

* 10% goes to the stakers on validators.
* 40% goes to the TF treasury.
* 50% goes to burning. This is more than in version 3.11 and it should largely compensate for minting.

##### Utilization Extras

* Utilization extras will not be possible.

#### VARIABLE POLICY (NEW)

Farms can decide to upgrade to Variable Policy, we highly recommend farmers do so.

##### Farming

* New tokens (TFT or CHI for v4.0) are only the result of CU/SU farming.
* Rewards are always variable in line to parameters as specified on TFChain.
* Rewards are automatically staked on the 3Node.
* There is a Farmer Staking lockup period of 1 year or 30% utilization, whichever comes first.

##### Utilization CU/SU

* 20% goes to farmers for SU/CU utilization.
* 10% goes to the stakers on validators.
* 10% goes to the stakers on farms (for utilization of that farm).
* 10% goes to the TF treasury.
* 50% goes to burning. This is more than in 3.11 and should largely compensate for minting.

##### Utilization Extras

As can be defined by the farmers, this represents an extra source of income:

* 70% goes to the farmer for the utilization extras
  * Extra rewards for CU/SU (per node)
  * Extra rewards for Dedicated Nodes (per node)
  * Define prices for NU and IP Addresses (per farm)
* 10% goes to stakers on validators.
* 10% goes to stakers on farms (for utilization of that farm).
* 10% goes to the TF treasury.