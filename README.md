# VIP Token Contract

This contract, written in Solidity, implements the functionality of a custom ERC20 token named "VIP Token" with the symbol "VP". The contract provides basic token operations such as minting, burning, and transferring tokens. Additionally, it includes a modifier to restrict certain functions to be callable only by a specified address.

## Overview

- **Token Name**: VIP Token
- **Token Symbol**: VP
- **Total Supply**: Initially set to 0, tokens can be minted by the claimer.
- **Claimer**: The address that deploys the contract is set as the initial claimer. Only the claimer can mint tokens.

## Functionality

### Constructor

- Initializes the contract with the token name, symbol, and assigns the deploying address as the claimer.
- Mints 0 tokens initially to the claimer.
- Sets the contract status to active.

### `MintTokens`

- **Access**: Only callable by the claimer.
- Allows the claimer to mint a specified amount of tokens and assign them to a target address.

### `burnTokens`

- **Access**: Available to any token holder.
- Allows a token holder to burn a specified amount of their own tokens.

### `transferTokens`

- **Access**: Available to any token holder.
- Allows a token holder to transfer a specified amount of tokens to another address.

### `onlyClaimer` Modifier

- Restricts access to functions marked with this modifier to only the claimer address.

## Usage

1. Deploy the contract to the Ethereum network.
2. After deployment, the deploying address becomes the claimer.
3. The claimer can mint tokens for specific addresses using the `MintTokens` function.
4. Token holders can burn their tokens using the `burnTokens` function.
5. Token holders can transfer tokens to other addresses using the `transferTokens` function.

## Development Environment

- **Solidity Version**: ^0.8.17
- **Dependencies**: OpenZeppelin ERC20.sol
- **License**: MIT

## Contact

renukapushpa6@gmail.com
