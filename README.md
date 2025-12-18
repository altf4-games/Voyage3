# Voyage

A decentralized travel and hospitality platform that revolutionizes the travel industry by combining blockchain smart contracts, AI agents, and community-driven features. Users can book hotels and tickets, earn loyalty rewards as NFTs, participate in community governance, and access a decentralized marketplace.

## Overview

Voyage eliminates traditional intermediaries in the travel industry by leveraging blockchain technology for transparent, secure bookings and payments. The platform integrates AI agents for enhanced user experience and uses smart contracts to manage hotel reservations, ticket purchases, and community interactions.

## Project Structure

```
Frontend/          - React-based web application with 3D globe visualization
onchainAiAgents/   - Python AI agent services for onchain interactions
voyage-contracts/  - Solidity smart contracts for core platform logic
```

## Key Features

### Booking System

- NFT-based hotel bookings with check-in/check-out verification
- Ticket purchase and management system
- Automated loyalty points distribution
- Secure payment handling with smart contracts

### Community Features

- Decentralized community governance
- User profiles with booking history
- Community-driven marketplace for travel services
- Testimonials and reviews system

### Rewards Program

- Loyalty points earned through bookings
- NFT-based reward system
- Point redemption mechanism
- Gamified travel experience

### User Experience

- Interactive 3D globe for destination browsing
- Real-time booking availability
- File upload for travel documents
- Responsive design with TailwindCSS

## Tech Stack

**Frontend**

- React 18 with Vite for fast development
- React Router for navigation
- TailwindCSS for styling
- Three.js & React Three Fiber for 3D visualizations
- Framer Motion for animations
- ThirdWeb SDK for Web3 integration
- Ethers.js for blockchain interactions
- React Dropzone for file uploads
- Axios for API requests

**Blockchain**

- Solidity ^0.8.0
- Hardhat development framework
- OpenZeppelin contracts (ERC721, Ownable, ReentrancyGuard)
- NFT standards (ERC721URIStorage)

**AI Agents**

- Python-based onchain AI services
- Video processing capabilities
- Smart contract interaction automation

## Setup

### Frontend

```bash
cd Frontend
npm install
npm run dev
```

### Smart Contracts

```bash
cd voyage-contracts
npm install
npx hardhat compile
```

### AI Agents

```bash
cd onchainAiAgents
pip install -r requirements.txt
python main.py
```

## Development

The frontend runs on Vite's development server with hot module replacement. Smart contracts can be deployed to local Hardhat network or testnets. The AI agents interact with deployed contracts for automated onchain operations.

### Smart Contract Deployment

```bash
cd voyage-contracts
npx hardhat run scripts/deploy.js --network <network-name>
```

### Testing

```bash
cd voyage-contracts
npx hardhat test
```

## Architecture

The platform uses a three-tier architecture:

1. **Frontend Layer**: React application handling user interactions and Web3 wallet connections
2. **Blockchain Layer**: Smart contracts managing bookings, payments, and NFT issuance
3. **AI Layer**: Python agents for automated operations and enhanced user experience

All booking and transaction data is stored on-chain for transparency and immutability. The frontend communicates with smart contracts via Ethers.js and ThirdWeb SDK.

## Smart Contracts

### Hotel.sol

- ERC721-based NFT hotel bookings
- Check-in/check-out time management
- Room number assignment
- Loyalty points system per booking
- Price management and payment handling
- User booking history tracking
- Reentrancy protection for secure transactions

### Ticket.sol

- Ticket issuance and verification
- Digital ticket ownership
- Transfer and resale capabilities

### Community_Contract.sol

- Community governance mechanisms
- Member management
- Voting and proposal systems
- Community treasury management

## Application Routes

- `/` - Landing page with hero, features, testimonials, and FAQs
- `/dashboard` - User dashboard overview
- `/profile` - User profile with booking history
- `/booking` - Hotel and ticket booking interface
- `/marketplace` - Decentralized travel marketplace
- `/community` - Community hub and governance
- `/rewards` - Loyalty rewards management

## License

MIT
