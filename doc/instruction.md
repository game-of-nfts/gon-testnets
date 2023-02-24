# Instruction on Interchain NFT Transfer

## SDK Implementation

IRISnet, Uptick and OmniFlix use [nft-transfer](https://github.com/bianjieai/nft-transfer/tree/v1.1.1-beta) to implement Interchain NFT functionality. These chains share the same instruction in their clients. 

**Note, whether it is the original chain or the target chain, the portID of cross-chain transfer nft is fixed `nft-transfer`**

### Transfer

For cross-chain transfer nft, please execute the following command:

```bash
simd tx nft-transfer transfer \
<src-chain-port> \
<src-chain-channel> \
<dst-chain-receiver> \
<classID> \
<nftID>  
```

### Query

When the nft is received by the target chain, a new class category will be generated according to the definition of ics721. For details, please refer to the [ics721 spec](https://github.com/cosmos/ibc/blob/main/spec/app/ics-721-nft-transfer/README.md). Of course, you can query the classID generated on the target chain with the following command

```bash
simd query nft-transfer class-hash <class-prefix>/<class-base-id>
```

If you want to query the original information of cross-chain nft, you can use the following command

```bash
simd query nft-transfer class-trace [class-hash] [flags]
```

When the nft cross-chain transfer to the destination chain is successful, the nft on the original chain will be hosted at the specified system account address, you can use the following command to query the system account address

```bash
simd query nft-transfer escrow-address [port] [src-channel-id]
```

## CosmWasm Implementation

Stargaze and Juno use [cosmwasm-ics721](https://github.com/public-awesome/ics721) to implement [ICS 721 speicification](https://github.com/cosmos/ibc/tree/main/spec/app/ics-721-nft-transfer) in CosmWasm.

### Transfer

```bash
simd tx wasm execute <cw-721-addr> \
{"send_nft": {"contract": "<ics-721-addr>", "token_id": "<token-id>", "msg": \ "<basa64_encoded_msg>"}}
```

In which the `<base6_encoded_msg>` should be the following JSON string encoded with base64.

```json
{
  "receiver": "<reciver-addr>",
  "channel_id": "<src-channel-id>",
  "timeout": {
    "block": {
      "revision": <chain-revision>,
      "height": <timeout-height>
    }
  }
}
```

### Query

Query the CW-721 contract address of the arrived NFT on this chain:

```bash
simd q wasm contract-state smart <ics-721-addr> '{"nft_contract": {"class_id" : "<class-prefix/class-base-id>"}}'
```

Query the NFT info of this CW-721 contract address:

```bash
simd q wasm contract-state smart <cw-721-addr> '{"all_nft_info":{"token_id": "<token-id>"}}'
```

Query the NFT number under this CW-721 contract address:

```bash
simd q wasm contract-state smart <cw-721-addr> '{"num_tokens":{}}'
```
