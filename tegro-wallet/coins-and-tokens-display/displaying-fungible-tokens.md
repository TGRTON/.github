# Displaying fungible tokens

Tegro Wallet prioritizes in the network those metadata that meet the token's metadata standard.

For fungible tokens, Tegro Wallet will display the following information:

<table><thead><tr><th width="327.9256545410941" align="center">Field</th><th align="center">Description</th></tr></thead><tbody><tr><td align="center">Name</td><td align="center">Token name (for example: "Tegro Gusev Ruban")</td></tr><tr><td align="center">Symbol</td><td align="center">Token symbol (for example: "TGR")</td></tr><tr><td align="center">Image</td><td align="center">URI pointing to the token logo</td></tr></tbody></table>

If the interchangeable token has name and character fields that are both in the metadata account on the chain and in the JSON file outside the chain (linked via URI field on the chain), then Tegro Wallet will give priority to fields on the chain.

In case the interchangeable token does not have a metadata account on the chain, then Tegro Wallet will display data from a list of tokens. This list is obsolete and should not be used to place new tokens. When reading from the token list, Tegro Wallet will display the following information:

<table><thead><tr><th width="325.94852864075295" align="center">Field</th><th align="center">Описание</th></tr></thead><tbody><tr><td align="center">Name</td><td align="center">Token name (for example: "Tegro Gusev Ruban")</td></tr><tr><td align="center">Symbol</td><td align="center">Token symbol (for example: "TGR")</td></tr><tr><td align="center">Image</td><td align="center">URI pointing to the token logo</td></tr><tr><td align="center">extensions.coingeckoID</td><td align="center">The token identifier defined by the Coingecko API. Tegro Wallet uses it to get the price of the token</td></tr></tbody></table>
