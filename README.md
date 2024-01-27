# Restaurant Review Smart Contract

## Overview

The Restaurant Review Smart Contract is a Solana program that manages restaurant reviews on the blockchain. This README provides an overview of the contract's purpose, functionalities, and instructions on how to deploy and interact with it.

## Contract Details

The contract is implemented in Rust using the Solana programming model. It consists of three main modules:

1. `lib.rs`: The main logic of the smart contract, including the entry point (`process_instruction`) and functions for adding and updating reviews.

2. `instruction.rs`: Defines the `ReviewInstruction` enum, which specifies the types of instructions that can be executed on the smart contract. It also includes the `ReviewPayload` struct for deserializing the instruction data.

3. `state.rs`: Defines the data structure (`AccountState`) representing the state of each restaurant review. It also includes the implementation of the `IsInitialized` trait for checking the initialization status and the `ReviewError` enum for custom error handling.

## Account State

### `AccountState`

The `AccountState` struct represents the state of each restaurant review and includes the following fields:

- `is_initialized`: A boolean indicating whether the account has been initialized.
- `rating`: A byte representing the rating given to the restaurant (1 to 10).
- `description`: A string containing a detailed description of the restaurant review.
- `title`: A string representing the title of the review.
- `location`: A string representing the location of the restaurant.

## Custom Errors

### `ReviewError`

The `ReviewError` enum defines custom errors for the smart contract, including:

- `UninitializedAccount`: Raised when attempting to interact with an uninitialized account.
- `InvalidPDA`: Raised when the derived PDA does not match the PDA passed in.
- `InvalidRating`: Raised when the provided rating is greater than 10 or less than 1.

## How to Deploy

Follow the deployment instructions provided in the [previous section](#how-to-deploy).

## How to Interact

After deploying the contract, you can interact with it using Solana's command-line tools or by integrating it into your Solana DApp. Refer to the [previous section](#how-to-interact) for examples.

## Bonus: Frontend Integration

To integrate the location field into your frontend code:

1. Update your UI components to capture and display the location field.
2. Adjust your queries to include the new location field when fetching or submitting reviews.

## Contribution

Feel free to contribute to the development of this project by submitting issues or pull requests. Contributions are welcomed to improve functionality and user experience.

Happy Reviewing! 🍽️🌟
