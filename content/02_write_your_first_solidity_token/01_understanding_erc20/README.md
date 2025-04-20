## Understanding the fundamentals of ERC20

If you've ever used a token on Ethereum — whether it's USDC, DAI, or LINK — chances are, you've interacted with an **ERC-20** token. The ERC-20 standard is the foundation for fungible tokens on Ethereum-compatible networks like **Pharos**, meaning every token of a type is interchangeable and holds the same value.

Think of it like this: just as every dollar in your wallet is worth the same, every ERC-20 token is equal in value and function. This standard makes tokens predictable, compatible, and easy to integrate across wallets, exchanges, DeFi apps, and beyond.

### Why Use ERC-20 on Pharos?

Pharos supports the Ethereum Virtual Machine (EVM), so anything built for Ethereum — including ERC-20 tokens — works seamlessly on Pharos. This is great for developers, because it means:

- You can use popular development tools like **Foundry**, **Hardhat**, or **Remix**.
- You get access to trusted open-source libraries like **OpenZeppelin**.
- Your token can plug directly into existing wallets, marketplaces, or even bridges between chains.

### The Big Ideas Behind ERC-20

At its core, the ERC-20 standard defines **a common set of rules** that all fungible tokens must follow. These rules govern how tokens are transferred, how balances are tracked, and how third parties (like smart contracts) can access or move someone’s tokens (with permission).

Every ERC-20 token follows the same pattern:

- You can **check your balance**.
- You can **send tokens** to someone else.
- You can **give permission** for another contract to spend your tokens.
- You can **track** when tokens move from one wallet to another.

This consistency makes ERC-20 tokens extremely reliable and easy to work with — which is exactly why it's the standard we’ll use in our token-building tutorial.

---

In the next section, we’ll show you how to implement this with OpenZeppelin’s smart contract library, and deploy your own ERC-20 token on Pharos using Foundry.

👉 Reference: [OpenZeppelin ERC-20 Standard Documentation](https://docs.openzeppelin.com/contracts/5.x/erc20)  
👉 Pharos Guide: [Write Your First Token](https://docs.pharosnetwork.xyz/developer-guides/foundry/write-your-first-token)

Let’s get started with writing and deploying your first token!