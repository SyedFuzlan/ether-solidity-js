# Explore Simple Storage

A minimal Solidity + JavaScript workshop demonstrating how to:
- Write, compile, and deploy a simple smart contract
- Interact with Ethereum using [ethers.js v6](https://docs.ethers.org/v6/)
- Securely manage private keys

## Contents

- `SimpleStorage.sol` — Solidity contract for storing and retrieving a number, and mapping names to numbers.
- `deploy.js` — Script to deploy and interact with the contract using ethers.js v6.
- `encryptKey.js` — Script to encrypt your private key for safer storage.
- `.env` — Environment variables (never commit secrets to public repos!).
- `.encryptedKey.json` — Encrypted private key output (do not share).

## Prerequisites

- Node.js (v16+ recommended)
- [Yarn](https://yarnpkg.com/) or npm
- [solcjs](https://www.npmjs.com/package/solc) for Solidity compilation
- An Ethereum RPC endpoint (e.g., [Alchemy](https://alchemy.com/), [Infura](https://infura.io/))
- A funded testnet account (e.g., Sepolia)

## Setup

1. **Install dependencies:**
   ```bash
   yarn install
   # or
   npm install
   ```

2. **Compile the contract:**
   ```bash
   yarn solcjs --bin --abi --include-path node_modules/ --base-path . -o . SimpleStorage.sol
   ```

3. **Configure environment variables:**
   Create a `.env` file:
   ```
   PRIVATE_KEY=your_private_key
   RPC_URL=https://your-ethereum-node
   PRIVATE_KEY_PASSWORD=your_password
   ```

4. **Encrypt your private key (optional but recommended):**
   ```bash
   node encryptKey.js
   ```

## Deploy & Interact

Deploy the contract and interact with it:

```bash
node deploy.js
```

## Security

- **Never commit your real `.env` or unencrypted private keys to public repositories.**
- Use `.gitignore` to exclude sensitive files.

## License

MIT

---
*Workshop by [Your Name or Organization]*
