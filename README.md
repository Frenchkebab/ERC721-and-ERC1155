## ERC1155 Explanation

**Description**
Explain the differences between ERC721 and ERC1155. Specifically, explain how the transfer functions differ.

Explain how 1155 is capable of providing non-fungible tokens the way ERC721 can (hint read the original EIP).

### How ERC721 and ERC1155 differ.

In ERC1155, there are 'copies' of tokens.
So when you mint the token, you also can decide 'how many copies of the token' to be minted.

**ERC721.sol**

```solidity
function _mint(address to, uint256 tokenId) internal virtual;
```

**ERC1155.sol**

```solidity
function _mint(address to, mint256 id, uint256 amount, bytes memory data) internal virtual
```

Also when you transfer tokens under ERC-1155 standard, you have to decide the amount of token to send.

**ERC721**

```solidity
function transferFrom(address from, address to, uint256 tokenId) public virtual override;
```

**ERC1155**

```solidity
function safeTransferFrom(address from, address to, uint256 id, uint256 amount, bytes memory data) public virtual override;
```

### How ERC1155 is capable of providing non-fungible tokens the way ERC721 can.

Just like ERC721, ERC1155 is capable of providing non-fungible tokens by giving each unique token a token id.
Additional to ERC721, ERC1155 provides the way to mint cerntain amount of copies for each token.
