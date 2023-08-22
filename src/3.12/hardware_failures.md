# Hardware Failures

The current situation already takes into account hardware failures and ways to incite farmers to avoid such situations. In the current scenario, if hardware fails while the 3Node has some workloads, the farmers lose the rewards for the whole month. This incite farmers to use high-quality hardware that will not fail during deployment. This is written in the minting code.

#### Hardware Failures Workarounds

There can be many ways to work around hardware failures depending on the situation. While all potential issues and situations are not yet covered and fixed, we can develop on the current situation.

Currently, if the SSD of a 3Node fails, the user loses the data. Depending on the type of workload, a user could simply decide to deploy on another node. Users could also have backups available in order to avoid losing the data.

Some workloads can be self-healing by design. For example, if a user runs a Jitsi instance and the 3Node fails, the user could simply redeploy on another 3Node and the workload would more or less be as effective. As another example, if a user deploys a Nextcoud instance and enabled a redundant backup on another 3Node, they could simply redeploy on functioning 3Node and transfer the data to this new 3Node.

This type of thinking is to show that there are ways to circumvent or deal with hardware failures with deployments themselves.