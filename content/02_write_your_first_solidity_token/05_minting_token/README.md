## Minting Tokens with Solidity Contract

With your token successfully deployed to the Pharos Devnet, the next step is to mint additional tokens. Minting refers to the creation of new tokens and assigning them to a specified address. In our `Token.sol` contract, this is handled by the `_mint` function inherited from OpenZeppelin’s ERC20 implementation.

Since the contract is designed to mint tokens only once during deployment (via the constructor), if you want to mint more tokens after deployment, you’ll need to modify the contract slightly to add a public `mint` function—or redeploy a version that includes this.

For now, let’s walk through how to do this using a version of the contract that has minting functionality exposed. First, update your contract in the Solide IDE by adding the following function inside the `Token` contract:

```solidity
function mint(address to, uint256 amount) public {
    _mint(to, amount);
}
```

### Quest - Mint X Tokens

With this addition, you can now mint tokens to any address of your choice. Recompile and redeploy the contract, making sure you’re still connected to the Pharos Devnet in MetaMask.

Once deployed, head to the "Write Contract" tab in Solide or any connected interface, and call the `mint` function. You’ll need to provide two inputs:
- `to`: the wallet address you want to send the new tokens to
- `amount`: how many tokens you’d like to mint (remember ERC-20 tokens often use 18 decimals, so minting “100” tokens would require inputting `100000000000000000000`)

After submitting the transaction, you can check your minted balance by calling the `balanceOf` function or viewing your address on [pharosscan.xyz](https://pharosscan.xyz).

Minting is a key part of many token ecosystems, especially those involving rewards, governance, or inflationary models. You’ve just taken another step closer to mastering token development on Pharos!