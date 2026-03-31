# NFT-Faucet
NFT Faucet
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC721/ERC721.sol";

contract NFTFaucet is ERC721 {
    uint256 public nextId;

    constructor() ERC721("NFTFaucet", "NFF") {}

    function drip() public {
        _mint(msg.sender, nextId++);
    }
}
