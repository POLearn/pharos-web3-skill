## Deploying Your Token to Pharos

Now that you’ve learned how the ERC-20 standard works and understand how Pharos operates, it’s time to put that knowledge into action by deploying your own token to the Pharos Devnet. We'll use the `Token.sol` contract, which is already set up and ready for deployment through the Solide IDE. Simply load the contract, and make sure to compile it using the Solidity version `0.8.26`.

Before deploying, make sure your MetaMask wallet is connected to the Pharos Devnet. If you haven’t configured it yet, refer back to the `05_connect_to_pharos` section for the network setup instructions.

### Quest - Deploy Token

Let’s personalize your token. Update the token’s name and symbol in the contract to represent your project. For this exercise, rename it to `"Proof of Token"` with the symbol `"POT"`. When deploying the contract, you’ll be asked to provide constructor parameters. Input the following:

- Name: `Proof of Token`  
- Symbol: `POT`

After deployment, you’ll receive a contract address. You can verify and explore your token by pasting this address into [pharosscan.xyz](https://pharosscan.xyz).

Congratulations—your first token contract is now live on Pharos! This is a major milestone in your journey. Be sure to keep your transaction hash safe, as you’ll need it to complete your quest and prove your achievement. 🎉