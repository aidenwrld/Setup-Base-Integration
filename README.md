# Setup-Base-Integration
Setup &amp; Base Integration
Hardhat Config (Base setup)
require("@nomicfoundation/hardhat-toolbox");
require("dotenv").config();

module.exports = {
  solidity: "0.8.20",
  networks: {
    baseSepolia: {
      url: process.env.BASE_RPC,
      accounts: [process.env.PRIVATE_KEY],
    },
  },
};

ERC20 Test Token
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract BaseToken is ERC20 {
    constructor() ERC20("BaseToken", "BTK") {
        _mint(msg.sender, 1000000 * 10 ** decimals());
    }
}
