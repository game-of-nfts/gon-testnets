# ICS-721 Instruction for Go Implementation

IRISnet, Uptick and OmniFlix use [nft-transfer]() to implement Interchain NFT functionality. These chains share the same instruction in their clients. 

**Note, whether it is the original chain or the target chain, the portID of cross-chain transfer nft is fixed `nft-transfer`**

## Transfer

For cross-chain transfer nft, please execute the following command:

```bash
simd tx nft-transfer transfer <src-chain-port> <src-chain-channel> <dst-chain-receiver> <classID> <nftID>  \
    --from <signer> \
    --chain-id <chain-id> \
    --keyring-dir <key-path> \
    --keyring-backend=<backend> \  
    --fees <fee> \
    -b block \ 
    --node <rpc-address> \ 
```

## Class-hash

When the nft is received by the target chain, a new class category will be generated according to the definition of ics721. For details, please refer to the [ics721 spec](https://github.com/cosmos/ibc/blob/main/spec/app/ics-721-nft-transfer/README.md). Of course, you can query the classID generated on the target chain with the following command

```bash
simd query nft-transfer class-hash <port>/<dst-chain-channel>/<src-chain-class-id> 
```

## Class-trace

If you want to query the original information of cross-chain nft, you can use the following command

```bash
simd query nft-transfer class-trace [class-hash] [flags]
```

## Escrow-address

When the nft cross-chain transfer to the destination chain is successful, the nft on the original chain will be hosted at the specified system account address, you can use the following command to query the system account address

```bash
simd query nft-transfer escrow-address [port] [src-channel-id]
```
