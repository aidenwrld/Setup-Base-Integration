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

