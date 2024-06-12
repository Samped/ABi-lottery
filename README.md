
# ABI-Lottery Smart Contract

## Overview
This Solidity smart contract implements a lottery system where participants can enter by sending a minimum amount of Ether. The winner is determined randomly using Chainlink's Verifiable Random Function (VRF), ensuring fairness and transparency.

## Features
- Allows participants to enter the lottery by sending Ether.
- Determines the winner randomly using Chainlink's VRF.
- Provides a transparent and decentralized method for selecting winners.
- Implements access control to start and end lotteries, with the owner having exclusive control.

## Dependencies
- [Chainlink VRFConsumerBase](https://docs.chain.link/docs/vrf-contracts/) - Interface for interacting with Chainlink's VRF.
- [OpenZeppelin Ownable](https://docs.openzeppelin.com/contracts/3.x/access-control#ownable) - Provides basic access control functions.

## Usage
1. **Setup**: Deploy the contract with the necessary constructor parameters, including the address of the ETH/USD price feed, VRF coordinator, LINK token address, fee, and keyhash.
2. **Starting a Lottery**: Only the owner can start a new lottery using the `startLottery()` function.
3. **Entering the Lottery**: Participants can enter the lottery by sending the required amount of Ether using the `enter()` function.
4. **Ending the Lottery**: After participants have entered, the owner can end the lottery and determine the winner using the `endLottery()` function.
5. **Winner Determination**: The winner is randomly selected using Chainlink's VRF and announced by the contract.
6. **Claiming Winnings**: The winner can claim their winnings by withdrawing them from the contract.




