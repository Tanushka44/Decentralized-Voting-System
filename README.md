# Decentralized Voting System

## Project Description
A secure and transparent decentralized voting system built on Ethereum using Solidity. The system allows participants to vote on proposals within a fixed time period. Each wallet is allowed one vote, and the results are publicly verifiable on the blockchain.

## Project Vision
To empower communities and DAOs to make fair, tamper-proof decisions without relying on centralized intermediaries. By leveraging blockchain, we eliminate the risk of vote manipulation, ensure transparency, and preserve voter integrity.

## Key Features
- ✅ One-person, one-vote mechanism (per wallet)
- ⏰ Time-boxed voting session (defined at contract creation)
- 📊 Real-time leader tracking
- 🗳 Chairperson can add proposals before voting closes
- 🔍 On-chain result verification
- 📤 Emits events for off-chain indexing (e.g., Graph, Etherscan)

## How It Works
1. **Deploy** the contract with a list of proposal names and voting duration (in seconds).
2. **Participants vote** by calling `vote(proposalId)` before the deadline.
3. **Winner** can be revealed after voting ends by calling `winner()`.

## Future Scope
- 🧠 Token-weighted voting support (ERC-20 or NFT-based)
- 🔗 Chainlink/Oracle integration for off-chain voting triggers
- 📈 Front-end dApp using React and Web3.js or Ethers.js
- 📂 IPFS support for rich proposal metadata
- 🛡️ zkSNARKs or zero-knowledge rollups for private voting
- 👥 DAO integration using OpenZeppelin’s Governor or Compound Governance modules

## Example
```solidity
string[] memory proposals = ["Alice", "Bob", "Charlie"];
DecentralizedVoting vote = new DecentralizedVoting(proposals, 600); // Voting lasts 10 minutes

![image](https://github.com/user-attachments/assets/0ab7a3d8-ea84-4726-a4e9-baf0ef2ae169)

