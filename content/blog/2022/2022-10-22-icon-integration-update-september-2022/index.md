---
title: ICON Integration Update – September 2022
date: 2022-10-21
description: Welcome to the Integration Update series. In September, the teams made progress on ICON Bridge integrations for Binance Smart Chain, NEAR and SNOW.
slug: icon-integration-update-september-2022
---

Welcome to the Integration Update series. In September, the teams made progress on ICON Bridge integrations for Binance Smart Chain, NEAR and SNOW.

Follow along for an itemized update of the work that has been done. 

## Binance Smart Chain:

The ICON Bridge integration with Binance Smart Chain has gone smoothly and the team has continued to patch recommended fixes and increase code testing coverage to 80%. Progress continued on building a usable centralized bridge for the BTP Relay System that can deliver digital assets between multiple chains. 

### Last 30 Days:
{{< table >}}
| Name | Development State | Notes | Source / location |
|-----|------------------|----|----------------| 
| Script to add/remove solidity owners | Released | Script to update SC owners| https://github.com/icon-project/icon-bridge/issues/395 |
| Script to add/remove javascore owners | Released | Script to update SC owners| https://github.com/icon-project/icon-bridge/issues/395 |
| Script to change javascore deployer | Released | Script to update SC owners| https://github.com/icon-project/icon-bridge/issues/395 |
| Local build script update| Released | missing dependencies need to be added | https://github.com/icon-project/icon-bridge/issues/426| 
| Upgrade(BTS SCORE) | Released on Testnet | upgrade script on bsc testnet for BTS Core. Investingating issue on Mainnet deployment | https://github.com/icon-project/icon-bridge/issues/467 | 
| Automate configuration on e2e | Released |  Configuration APIs added for e2e tests to run | https://github.com/icon-project/icon-bridge/issues/415 |
| Set truffle version in local build script | Released | Set truffle version to v5.5.5 | https://github.com/icon-project/icon-bridge/issues/435 |
| Alternative build process for local deployment | Released | Update local deployment scripts | https://github.com/icon-project/icon-bridge/issues/463 |
| Add bsc header and receipts verification | Released | Add block header and receipts verification logic to bsc verifier | https://github.com/icon-project/icon-bridge/issues/377 |
| Add script to generate e2e config during deployment | Released | Update script so necessary e2e config should be auto-generated by the deployment script itself | https://github.com/icon-project/icon-bridge/issues/494 |
| Notification pipeline | Released | List and update the most stable contract addresses | https://github.com/icon-project/icon-bridge/issues/37 |
| BSC block verification | Released | Relay to verify correctness of incoming messages the same way that the BMV does | https://github.com/icon-project/icon-bridge/issues/35 |
| Unit tests to bsc verifier | Released | Add unit tests to bsc verifier | https://github.com/icon-project/icon-bridge/issues/499 |
| Script to generate e2e config during deployment added | Released | Simplify the process of running e2etests after a successful build process | https://github.com/icon-project/icon-bridge/issues/525 |
| Setter getter tests for javascore BMC added | Released | Add unit test for all setter and getter methods in javascore BMC | https://github.com/icon-project/icon-bridge/issues/542 |
| NEAR integration suppoort | In Progress | Support NEAR integration team with integration and support | - |
| Security Audit | In Progress | Support Security Auditors | - |
{{< /table >}}

### Next 30 Days:
Next month the team will focus on auditing fixes, support activities, code testing coverage and general improvements to the codebase.

{{< table >}}
| Name | Development State | Notes |
|:-----|:------------------|:-----|
| Continue Improvement of code coverage for the code base |In Progress| The codecoverage of the repo is low. Work towards achieving the target of 80% coverage to improve the health of the overall codebase. |
| Assist with Security Audit | In Progress | The Security Audit has started. Any information needed to be provided or fixes needed based on security audit review will be provided adhoc.|
| Assist with Near release and integration | In Progress | Near is currently in Testnet. Mainnet deployment and Nexus integration is being planned September Release. Team to assist. |
| Strategize Xcall service for ICON<>BSC integration | Not Started |  |
{{< /table >}}

## NEAR Protocol:

In September, the team improved BMR Performance significantly, with up to 50x improvement in Block Monitoring. They also added Blacklisting and Transfer Restriction in BTS Contracts and began integration with Nexus.


### Last 30 Days:

{{< table >}}

| Module| Name | Development State | Notes | Source / location |
| ---- | --------- | ----------------- | ----- | ----------------- |
| E2E Testing Framework released | [E2E Test framework](https://github.com/icon-project/icon-bridge-planning/issues/47) | Alpha Released | Need to add test scripts  | [Github repo](https://github.com/icon-project/icon-bridge/tree/feat/402-create-chain-api-rpc-client-for-e2e-test/cmd/e2etest/chain/near) |
| BMR - Block Monitoring released | [Improvement in Block Monitoring](https://github.com/icon-project/icon-bridge/issues/387) | Released |  | [Pull Request](https://github.com/icon-project/icon-bridge/pull/401) |
| BTS - Transfer Restriction implemented  | [Implement Transfer Restriction](https://github.com/icon-project/icon-bridge/issues/152) | Released |  | [Pull Request](https://github.com/icon-project/icon-bridge/pull/549) |
| Blacklist implemented | [Implement Blacklist](https://github.com/icon-project/icon-bridge/issues/188) | Released |  | [Pull Request](https://github.com/icon-project/icon-bridge/pull/408) |


{{< /table >}}

### Next 30 Days:

NEAR is currently on testnet with ongoing testing and improvements planned for the month of October. The team is also developing a deployment plan for mainnet (more details to follow).


{{< table >}}
 | Name | Development State | Notes |
| ---- | ----------------- | ----- |
| Plan Mainnet Deployment | In Progress | |
| Complete Integration with Nexus Portal | In Progress | |
| Fix Reconnection Issue for BMR | Not Started | |
| Add Documentation for API Reference, Build, Deployment, Tests | In Progress | |
| Update NEAR SDK | Not Started | |
| Optimize smart contract storage | Not Started | |
| Add Code coverage | Alpha | |
| Add verifier for NEAR BMR | Not Started | |
| Fix Identified u128 serialization error | Not Started | |
{{< /table >}}

## SNOW Network:

SNOW's integration is in full flight with the goal of shipping to mainnet by the end of the month. Please note the current deployment will not include integration to Nexus. When live on mainnet, dapps will be abe to integrate what functions they want to use via their dapp itself.

### Last 30 Days:

{{< table >}}

| Name | Development State | Notes |
| ---- | ----------------- | ----- |
| Fix transaction fee calculation for SNOW chain | Released | |
| Create BMR unit test | In Progress | |
| Binance Smart Chain integration support | In Progress | |
| Refactored ICON relay receiver for readability  | Complete | |
| Add Code coverage | Alpha | |
| Add verifier for NEAR BMR | Not Started | |
| Fix Identified u128 serialization error | Not Started | |
| Improve BMR code unit tests coverage                                                | In Progress       |       | Epic https://github.com/icon-project/icon-bridge/issues/396 |
| Create BMR unit test for receiver functionality                                     | Released          |       | 1) https://github.com/icon-project/icon-bridge/issues/399   |
| Refactor the icon relay receiver to make it testable                                | Released          |       | 2) https://github.com/icon-project/icon-bridge/issues/614   |
| Integrate ICE/SNOW to the BTP                                                       | In Progress       |       | Epic https://github.com/icon-project/icon-bridge/issues/500 |

{{< /table >}}

### Next 30 Days:

{{< table >}}

| Name | Development State | Notes |
| ---- | ----------------- | ----- |
| Update NEAR SDK | Not Started | |
| Binance Smart Chain integration | Not Started | |
| Prepare SNOW Testnet Deployment | Not Started | |
| Extend deployment script functionality | Not Started | |
| Update SNOW configuration parameters | Not Started | |

{{< /table >}}

## Stay in the loop

If you would like to follow along daily with the team, a public roadmap is now available on [Github](https://github.com/orgs/icon-project/projects/4).

If you would like to learn more about ICON’s development process, be sure to [follow us on Twitter](https://twitter.com/helloiconworld) and [join us on Discord](https://discord.com/invite/7a75Hf3cFm)!


