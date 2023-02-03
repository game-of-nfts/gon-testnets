# Uptick Chain Information

## Chain

### Binary

The binary published in this repo is the `uptickd` binary built using the `uptick` repo branch [gon](https://github.com/UptickNetwork/uptick/tree/gon).

- SHA256: `1c386d7b365535d2e69f32d39c96ada4f733227d45d08b03da36e69bc9d54706`

You can generate the binary following the [build instructions](install.md).

### Public Endpoints

```
REST: https://peer1.testnet.uptick.network:1318
RPC: https://peer1.testnet.uptick.network:36657
grpc:https://peer1.testnet.uptick.network:9092

```


### Operattion guide about ics721

The nft implemented by each chain may be different. Use the chain of the [module/nft](https://github.com/irisnet/irismod/tree/main/modules/nft) module in irismod. For operations such as the issuance and transfer of nft, please refer to the [documentation](https://www.irisnet.org/docs/cli-client/nft.html#iris-tx-nft-edit)

After users issue nft, they can use the [ics721](https://github.com/cosmos/ibc/blob/main/spec/app/ics-721-nft-transfer/README.md) protocol to transfer nft to other chains. For specific operations, refer to the [document](ics721-cmd.md)


## Explorer

These block explorers allow you to search, view and analyze IRIS Hub data—like blocks, transactions, validators, governance including params or proposals, etc.

- [evm](https://evm-explorer.testnet.uptick.network/)
- [cosmos](https://explorer.testnet.uptick.network/uptick-network-testnet/)

## Faucet

Welcome to get test tokens in our [testnet faucet channel](https://discord.com/channels/781005936260939818/953652276508119060).
Usage: in [uptick-faucet channel](https://discord.com/channels/781005936260939818/953652276508119060), type "$faucet " + your address on 
UPTICK_7000-2 testnet, to get test tokens (Uptick) every 24 hours.

## Relayer

The repeaters currently supporting ics721 are as follows：

- [Hermes](https://github.com/informalsystems/hermes/tree/v1.1.0)

## Other
