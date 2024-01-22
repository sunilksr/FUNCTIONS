# MyToken 

## Overview

This Solidity smart contract, named `MyToken`, is an ERC-20 token that extends the functionality provided by the OpenZeppelin library. The contract allows for the creation, minting, burning, and transferring of tokens. The owner of the contract (inheritor) has exclusive privileges to perform certain actions.

## Smart Contract Details

### Token Details

- **Name:** MyToken
- **Symbol:** MYT

### Owner

The contract owner, referred to as the inheritor, is the address that deploys the contract. This address is granted special permissions to mint new tokens and execute other privileged functions.

### Events

The contract emits three events to notify external entities about important transactions:

1. **TokensMinted:** Triggered when new tokens are minted. It includes the inheritor's address and the number of tokens minted.

2. **TokensBurned:** Fired when tokens are burned. It includes the burner's address and the number of tokens burned.

3. **TokensTransferred:** Emits when tokens are transferred between addresses. It includes the sender's address, the inheritor's address, and the number of tokens transferred.

### Functions

1. **Constructor:**
   - Initializes the contract with a given name and symbol.
   - Mints an initial supply of 1000 tokens to the inheritor.

2. **mintTokens:**
   - Allows the inheritor to mint new tokens and assign them to a specified address.
   - Only the inheritor can call this function.
   - Requires a valid inheritor address and a positive token count.

3. **burnTokens:**
   - Allows any address to burn a specified amount of their own tokens.
   - Requires a positive token count.
   - Emits a `TokensBurned` event.

4. **transferTokens:**
   - Enables the transfer of tokens from the sender to a specified inheritor.
   - Requires a valid inheritor address and a positive token count.
   - Emits a `TokensTransferred` event.

## Usage

1. **Deploying the Contract:**
   - Deploy the contract using a compatible Ethereum development environment or platform.

2. **Minting Tokens:**
   - Call the `mintTokens` function to mint new tokens and assign them to a specified address.

3. **Burning Tokens:**
   - Use the `burnTokens` function to burn a specified amount of your own tokens.

4. **Transferring Tokens:**
   - Execute the `transferTokens` function to transfer tokens from the sender's address to a specified inheritor.

## Author

Sunil kS
