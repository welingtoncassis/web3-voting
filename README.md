# Web3Voting Smart Contract

## Description
This repository contains a simple Ethereum smart contract written in Solidity for conducting voting using the Ethereum blockchain. 
The smart contract, named Web3Voting, allows users to create new voting sessions with two options, 
and participants can cast their votes during a specified time window.

## Smart Contract Overview
The smart contract consists of the following main components:
Voting Struct: Represents a voting session with two options, the number of votes for each option, and the maximum date until which the voting is open.
Vote Struct: Represents a vote, storing the choice made by a participant and the timestamp of the vote.
Web3Voting Contract: The main contract managing the voting process. It includes functions to start a new voting session, 
retrieve the current voting session details, and allow users to cast their votes.

Usage

1. Deploy the Smart Contract
Deploy the Web3Voting smart contract on the Ethereum blockchain.

2. Start a New Voting Session
Call the addVoting function to start a new voting session. Provide the two options and the duration of the voting period. Only the contract owner can initiate a new voting session.

```function addVoting(string memory option1, string memory option2, uint timeToVote) public;```

3. Retrieve Current Voting Session Details
Use the getCurrentVoting function to retrieve the details of the current voting session, including the options, vote counts, and the voting deadline.

```function getCurrentVoting() public view returns (Voting memory);```

4. Cast a Vote
Participants can cast their votes using the addVote function. Specify the choice (1 or 2) during the open voting period. Each participant can vote only once.

```function addVote(uint choice) public;```
