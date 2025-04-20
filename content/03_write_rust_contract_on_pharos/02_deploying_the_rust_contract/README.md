## Deploying a Stylus contract to Pharos

Deploying a Stylus contract to Pharos is a straightforward but exciting step in your developer journey. Once you've written your Rust-based smart contract using Stylus, you'll want to see it live and functioning on-chain. In this section, we’ll walk you through the process of compiling, deploying, and verifying your contract on the Pharos Devnet.

First, make sure your development environment is properly set up. You’ll need Rust installed, along with the `cargo stylus` plugin which helps compile Stylus contracts into WASM (WebAssembly). If you haven’t already installed it, you can follow the guide in the [Pharos docs](https://docs.pharosnetwork.xyz/developer-guides/rust/setup-environment).

Once your tools are ready, navigate to the directory containing your Rust contract and run the build command:

```bash
cargo stylus build --release
```

This will compile your contract into a WASM binary located in the `target/` folder. This compiled binary is what gets deployed on-chain.

Now that you have the contract compiled, you can use MetaMask or any connected wallet that supports Stylus contract deployment. Head to the [Solide IDE for Stylus](https://stylus.polearn.xyz) or the Pharos deployment tool and load your WASM binary. You’ll also need to activate the contract after deployment, which typically involves a second transaction. This step finalizes the contract and makes it callable on-chain.

Once deployed, your Stylus contract will be live and ready to interact with other contracts—including Solidity-based ERC-20 tokens like the one you created earlier in the course.

Deploying a Stylus contract shows the power and flexibility of combining Rust’s safety and performance with the familiarity of the EVM. You're now equipped to build advanced dApps that bridge ecosystems, all while leveraging the strengths of both languages on Pharos.