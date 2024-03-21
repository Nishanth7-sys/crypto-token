# Item Redeem Token Contract

## Overview
This Solidity smart contract, named ItemRedeemToken, facilitates the redemption of cryptocurrencies in exchange for tokens. It allows users to redeem cryptocurrencies like Bitcoin and Solana by spending a certain amount of tokens. The contract is implemented with OpenZeppelin libraries for ERC20 token functionality, access control, and burning capabilities.

## Contract Features
- **ERC20 Token**: The contract extends the ERC20 token standard, allowing for the creation, transfer, and management of tokens.
- **Access Control**: The contract utilizes the Ownable pattern from OpenZeppelin, providing ownership control over contract management functions.
- **Burning Functionality**: Users can burn their tokens using the `burnTokens` function.
- **Token Minting**: The owner can mint new tokens to a specified address using the `mint` function.
- **Token Transfer**: Users can transfer tokens to other addresses using the `transferTokens` function.
- **Redeeming Cryptocurrencies**: Users can redeem cryptocurrencies by spending tokens. The contract supports redemption for Bitcoin and Solana, with configurable redemption rates.

## Deployment
The contract is deployed with the following parameters:
- Token Symbol: "DGN"
- Token Name: "DEGEN"
- Initial owner: Deployer's address
- Initial supply: 0 (tokens are minted as needed)
- Redemption costs and quantities for Bitcoin and Solana are configured during deployment.

## Functions
1. **setCrypto**: Internal function used by the owner to set the redemption details for supported cryptocurrencies.
2. **mint**: Owner-only function to mint new tokens to a specified address.
3. **transferTokens**: Allows users to transfer tokens to other addresses.
4. **redeemCrypto**: Allows users to redeem cryptocurrencies by spending tokens.
5. **burnTokens**: Allows users to burn their tokens.

## Events
- **LogMessage**: Emits a general log message.
- **CryptoRedeemed**: Emits an event when a user redeems cryptocurrency tokens.

## Storage
- **cryptos**: A mapping storing redemption details for supported cryptocurrencies.
- **redeemedQuantities**: A mapping storing the quantities of each redeemed cryptocurrency for each user.
- **redeemed**: A mapping storing the last redeemed cryptocurrency for each user.

## License
This code is released under the MIT License. See the SPDX-License-Identifier in the contract file.

#
