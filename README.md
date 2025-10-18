# 🧮 Counter Smart Contract

A simple Ethereum smart contract written in Solidity that keeps track of a count and increases it when called.

## 📄 Contract Code

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Counter {
    uint256 public count = 0;

    event CountIncreased(uint256 newCount);

    function increment() public {
        count += 1;
        emit CountIncreased(count);
    }

    function getCount() public view returns (uint256) {
        return count;
    }
}
