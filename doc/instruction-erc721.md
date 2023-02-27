# Instruction on NFT Basic Operations

A few tasks require participants to issue Denoms(Collections), mint NFTs, and transfer NFTs. Here are a few instructions on how to do that. The NFT Module of SDK Chain is based on Cosmos `x/nft` module, thus they have different implementations and module names.

## Transaction

For tasks, you only need to issue, mint and transfer on IRISnet. More details can be found [here](https://www.irisnet.org/docs/cli-client/nft.html#available-commands).

**issue**

```bash
iris tx nft issue <denom-id> \
--name <name> \
--uri <uri> \
--data <json-string-denom-data> \
--schema <denom-schema> \
--symbol <denom-symbol> \
--mint-restricted <true|false> \
--update-restricted <true|false>
```
**mint**

```bash
iris tx nft mint <denom-id> <nft-id> \
--name <nft-name> \
--uri <nft-uri> \
--uri-hash <nft-uri-hash> \
--data <json-string-token-data> \
--recipient <nft-recipient>
```

**transfer**

```bash
iris tx nft transfer <recipient> <denom-id> <nft-id>
```

## Query

For task, you probably need to query NFT Info on different chains, here are the commands for different SDK chains. As for CosmWasm query, you can refer [here](./instruction-ics721.md#query).

**Collection**

Query the detailed collection info.

```bash
iris q nft collection <denom-id> 

uptickd q collection collection <denom-id>

omniflixhubd query onft collection <denom-id>
```

**Owner**

Query the NFTs owned by an address.

```bash
iris q nft owner <address>

uptickd q collection owner <address>

omniflixhubd q onft owner <address>
```