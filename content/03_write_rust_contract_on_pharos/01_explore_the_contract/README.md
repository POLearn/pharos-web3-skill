## Exploring the `call-evm-from-wasm` Example from Pharos

Now that you've had an introduction to Stylus and how it works with Rust on the Pharos network, it’s time to dive deeper. One of the most exciting capabilities Stylus offers is the ability to interact directly with EVM-based Solidity contracts using Rust. To see this in action, we’ll explore an official example provided by the Pharos team.

You can find the contract on the Pharos GitHub repository:

```bash
https://github.com/PharosNetwork/examples/tree/main/interoperability/call-evm-from-wasm
```

To get hands-on without needing to set up anything locally, you can open the project directly in **Stylide**, the browser-based Stylus IDE:

```bash
https://stylus.polearn.xyz/?url=https://github.com/PharosNetwork/examples/tree/main/interoperability/call-evm-from-wasm
```

This contract is a great demonstration of Stylus’s real power—it allows a Rust smart contract to **call functions in a Solidity-based contract**. Specifically, it shows how a Stylus contract can mint tokens from an existing ERC-20 contract deployed on Pharos.

Let’s take a look at the key function in the `lib.rs` file:

```rust
pub fn mint_erc20(&self, erc20: Address, value: U256) -> Bytes {
    self.execute(erc20, Bytes(IErc20::mintCall {
        value,
    }.abi_encode()))
}
```

At first glance, this function might look simple, but it does something very powerful: it calls a Solidity contract’s `mint` function—directly from Rust.

Here's what’s happening step-by-step:

- `erc20: Address` is the address of the deployed ERC-20 Solidity contract we want to interact with.
- `value: U256` is the amount of tokens we want to mint. It uses `U256`, the 256-bit unsigned integer type standard in EVM blockchains.
- `IErc20::mintCall { value }.abi_encode()` builds the call to the Solidity `mint(uint256)` function using a Rust version of the Solidity interface. This is made possible using `sol!`, a macro provided by Alloy that allows defining Solidity interfaces in Rust and generating their ABI encoding automatically.
- `self.execute(...)` is a helper function that sends the encoded call to the specified contract using Stylus’s low-level `vm().call(...)` functionality.

So with just a few lines, we’re crafting and sending a contract call from Rust to Solidity. This is a perfect example of **Rust–Solidity interoperability** in action.

Why is this important?

Stylus makes it possible to build hybrid applications where the performance-critical or logic-heavy parts are written in Rust, while still leveraging existing and widely adopted Solidity infrastructure—like OpenZeppelin-based tokens or DeFi protocols. You’re not forced to pick one language or ecosystem over the other. Instead, you get the best of both worlds.

This is particularly valuable for projects that:

- Want to reuse trusted Solidity contracts but extend them with custom logic in Rust.
- Need Rust’s performance and memory safety for complex computations.
- Prefer Rust’s tooling, safety, or language features but still need to interact with EVM standards.

In the next part of this course, we’ll guide you through compiling and deploying this Stylus contract to Pharos. Once deployed, you’ll use it to call your existing Solidity-based ERC-20 token—right from your Rust contract. This unlocks a powerful pattern for designing modern, modular, and multi-language smart contract systems.