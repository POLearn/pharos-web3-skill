## Minting tokens from a Rust contract

Now that you’ve deployed both your contracts—the Solidity-based ERC-20 token and the Rust contract written with Stylus—it’s time to connect the dots and see them interact. This next step is all about demonstrating the real power of interoperability on Pharos.

In the previous section, we explored the `mint_erc20` function defined in the Rust contract. It’s designed to call the `mint` function on any ERC-20 token, as long as you provide the token’s address and the amount to mint. This works by encoding the function call using the Solidity ABI and sending it as an EVM call directly from the Rust contract.

### Quest - Call Execute Mint

Let’s put that into action. Using the same ERC-20 token you deployed earlier, try calling the `mint_erc20` method from your Rust contract. Pass in your token’s contract address and the desired token amount—for example, 1000 tokens (noting to multiply by 10^18 if using standard decimals).

Once the transaction goes through, check your wallet balance. If everything worked as expected, you should see the newly minted tokens. This shows just how powerful and flexible Stylus contracts can be when they interact with traditional Solidity contracts—all on the same network.

This hands-on exercise highlights how Rust-based smart contracts can complement existing EVM code, opening up new possibilities for building robust, modular dApps on Pharos.