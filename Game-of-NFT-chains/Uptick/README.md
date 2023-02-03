# Uptick Chain Information

## Chain

### Binary

The binary published in this repo is the `uptickd` binary built using the `uptick` repo branch [gon](https://github.com/UptickNetwork/uptick/tree/gon).

- SHA256: `1c386d7b365535d2e69f32d39c96ada4f733227d45d08b03da36e69bc9d54706`

You can generate the binary following the [build instructions](install.md).

### Genesis file

Final genesis file: **[genesis.json](genesis.json)**

- SHA256: `f96764c7ae1bc713b2acc87b5320f2d10ee26716b3daa6cc455cb3a3906f05c2`
- Validators must replace their `config/genesis.json` file with this one before running the binary.

The genesis file with was generated using the following settings:

- Chain ID: `uptick_7000-2`
- Denom: `auptick`
- Signed blocks window: `"14000"`


### Join the validator set

1. If you don't have a node configuration file yet, you can initialize a node with the following command:

```bash
uptickd init <moniker> --chain-id=uptick_7000-2 --home=~/.uptickd
```

2. Use the genesis.json provided by the chain team to overwrite the locally generated genesis.json file

```bash
curl -o $HOME/.uptickd/config/genesis.json https://raw.githubusercontent.com/UptickNetwork/uptick-testnet/main/uptick_7000-2/genesis.json
sed -i -e "s|^seeds *=.*|seeds = \"f97a75fb69d3a5fe893dca7c8d238ccc0bd66a8f@uptick-seed.p2p.brocha.in:30554,eecdfb17919e59f36e5ae6cec2c98eeeac05c0f2@peer0.testnet.uptick.network:26656\"|" $HOME/.uptickd/config/config.toml

```

3. Modify the config.toml file using the configuration provided in [Endpoints](#endpoints)

4. Start node

```bash
uptickd start --home=~/.uptickd
```

5. Receive tokens from the [faucet](#faucet) and join the set of validators

```bash
uptickd tx staking create-validator \
    --pubkey=$(upitckd tendermint show-validator) \
    --moniker=<your-validator-name> \
    --amount=<amount-to-be-delegated, e.g. 10000uptick> \
    --min-self-delegation=1 \
    --commission-max-change-rate=0.1 \
    --commission-max-rate=0.1 \
    --commission-rate=0.1 \
    --gas=100000 \
    --fees=0.6uptick \
    --chain-id=uptick_7000-2 \
    --from=<key-name>
```
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
