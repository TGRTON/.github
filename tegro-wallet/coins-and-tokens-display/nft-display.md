---
description: Coming soon
---

# NFT display

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

### In future updates there will be support for NFT, which will give the following features:

* Displaying NFT in the wallet&#x20;
* Sending NFTs to other users&#x20;
* Ability to instantly put up for sale through Marketplace integration

On the TON blockchain, NFTs are most often implied as SPL tokens with 0 decimal places and a stock of 1. According to the token metadata standard, some tokens may have similar characteristics to NFT.

However, we would like to clarify that the metadata standard for tokens on the TON blockchain does not imply a specific classification of tokens as NFT, FungibleAsset or otherwise. It depends on the developer of the token and its metadata.

Regarding Tegro Wallet, it will display tokens according to the classification specified in the token's metadata. If the token has metadata indicating its collectible nature, it will be displayed in a separate tab for collectible tokens. If the token is a FungibleAsset, it will be displayed in the general list of tokens.

### Grouping non-fungible tokens

The grouping of non-fungible (NFT) tokens (NFTs) on TON takes place through certification.

NFT-collection certification begins with the creation of a special contract on the TON blockchain, which is responsible for issuing new tokens. This contract contains the necessary functions for mining (creating new tokens) and transferring (transferring tokens from one owner to another).

Next, the creator of the NFT collection must publish the collection's metadata on the TON blockchain. The metadata contains information about how the tokens within the collection can be mined and used, and may include images and descriptions of each token.

Once the metadata is published, the creator of an NFT collection can request certification of his collection. To do so, he or she must submit a certification request that includes the address of the contract that issues the tokens, as well as the collection's metadata. In response to the request, the creator receives a unique identifier (ID) of his certified NFT collection.

For Tegro Wallet, NFT tokens are grouped by this unique ID of the certified NFT collection. If Tegro Wallet detects that some NFT tokens reference the same collection ID, they will be displayed as a group in a separate "Collections" tab. If no ID is found, however, Tegro Wallet will use other parameters (e.g. creator address) to group the NFT tokens.
