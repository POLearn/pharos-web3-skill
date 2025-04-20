## Rust programming on Pharos EVM base network 

When we think of writing smart contracts on Ethereum or other EVM-compatible chains, Solidity is usually the first language that comes to mind. But with the evolution of blockchain infrastructure, developers now have more tools than ever—and **Stylus** is one of the most exciting.

**Stylus** is a powerful smart contract framework built on the Arbitrum technology stack that allows you to write high-performance smart contracts in **Rust**. Unlike Solidity, which runs in the Ethereum Virtual Machine (EVM), Stylus contracts run in the **WASM (WebAssembly)** runtime, which is designed for speed and efficiency.

### Why Stylus?

Stylus opens the door to smart contract development for developers coming from systems programming backgrounds. Rust is already known for its safety, speed, and rich ecosystem—and now, it’s a first-class citizen in the blockchain world too. Here's what makes Stylus special:

- 🦀 **Write Smart Contracts in Rust**  
  Rust is a modern, memory-safe language that’s already loved by systems programmers and crypto developers. Stylus brings this powerful language to the world of decentralized applications.

- ⚡ **Performance Gains with WASM**  
  Stylus contracts run in a WASM-based environment, which means much faster execution compared to traditional EVM contracts—ideal for compute-heavy logic.

- 🔐 **Memory Safety & Security**  
  With Rust’s strict compile-time checks, you avoid many of the pitfalls that can lead to bugs and vulnerabilities in smart contracts.

- 🔧 **Better Tooling and Developer Experience**  
  The Rust ecosystem has mature tooling (like Cargo for dependency management and Clippy for linting), making development smoother and more maintainable.

### Stylus on Pharos

Pharos supports Stylus as a first-class citizen alongside Solidity. This means developers can choose the best tool for the job: Solidity for familiar EVM-style development, or Stylus for more performance-sensitive applications or if they prefer writing in Rust.

In this section of the course, you’ll learn how to write, compile, and deploy your very first Rust-based token smart contract using Stylus on the Pharos network. 
