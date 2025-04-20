## Creating Your First Token on Pharos

Now that you have a solid understanding of the ERC-20 standard, it’s time to build your own token. In this section, we’ll guide you through deploying a simple `Token.sol` smart contract that follows the ERC-20 standard using OpenZeppelin’s trusted implementation. This contract is fully compatible with the Pharos EVM environment.

You can find the contract in the Pharos example repository here:

```bash
https://github.com/PharosNetwork/examples/blob/main/token/hardhat/contract/contracts/Token.sol
```

Feel free to download it and load it into your preferred development environment. Alternatively, for a smoother experience, you can use the [Solide IDE](https://evm.polearn.xyz) and load the contract directly with this link:

```bash
https://evm.polearn.xyz/?url=https://github.com/PharosNetwork/examples/blob/main/token/hardhat/contract/contracts/Token.sol
```

The contract should look like this:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract Token is ERC20 {
    constructor(uint256 initialSupply) ERC20("Token", "MTK") {
        _mint(msg.sender, initialSupply);
    }
}
```

This smart contract defines a basic ERC-20 token using OpenZeppelin’s widely adopted library. The contract is named `Token` and inherits from the `ERC20` base contract, which provides all the core functionalities expected of an ERC-20 token, such as balance tracking, transfers, and approvals.

In the constructor, the token is initialized with a name (`"Token"`) and a symbol (`"MTK"`), both of which are used by wallets and block explorers to identify the token. The `_mint` function is called to create the initial supply and assign it to the deployer’s address (`msg.sender`).

This setup is a common starting point for launching simple fungible tokens. It can also be easily extended with additional features like burning, minting, or pausing by incorporating other modules from OpenZeppelin. It’s a great foundation for developers building on Pharos or any EVM-compatible blockchain.