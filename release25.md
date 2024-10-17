# v25 release changes


## Bootloader

* increase max_pubdata price and max_l2_price from 1M to 2^64 
    * This is for chains with custom base tokens with low unit value.

* removed upgradesystemcontext method
    * It was a temporary method, used in one of the past upgrades.

## Contracts

* Moved to **custom errors** from string based ones
* small gas optimisations
* l2-contracts moved to 1.5.0 compiler and solidity 0.8.24
* verifier_contract - mention vk_hash in the source code comments

## Scripts

* workflows - **switching to forge & foundry from hardhat**
* script for new chain registration
* moved from zksync-web3 to zksync-ethers
* improvements to deploy scripts - comare diamond hash
* improved compilation caching in scripts (don't recompile if not needed)


## Testing
* more bridgehub tests
* adopting tests to custom errors
* more mailbox tests


## Docs & comments

* naming - changing from zkSync to ZKsync
* additional documentation in solidity files
* better documentation for some methods & arguments
* changed wording from 'ergs' to 'gas'
* added missing licenses to YUL files


## Dependencies


* hardhat updated to 2.22 and chai matchers to 0.2.0
* lower restriction on solidity versions for interfaces (from 0.8.24 to ^0.8.21)
* explicit dependency on openzeppelin-v4 (to allow users to include other OZ versions)
* updated forge-sdk & murky
