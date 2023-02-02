# Uptick Chain Information

## Chain

### Binary

The binary published in this repo is the `uptickd` binary built using the `uptick` repo branch [gon](https://github.com/UptickNetwork/uptick/tree/gon).

- [Linux amd64 build](uptickd)
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
curl -o ~/.uptickd/config/genesis.json https://github.com/UptickNetwork/uptick-testnet/blob/main/uptick_7000-2/genesis.json
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

### Operattion guide about ics721

The nft implemented by each chain may be different. Use the chain of the [module/nft](https://github.com/irisnet/irismod/tree/main/modules/nft) module in irismod. For operations such as the issuance and transfer of nft, please refer to the [documentation](https://www.irisnet.org/docs/cli-client/nft.html#iris-tx-nft-edit)

After users issue nft, they can use the [ics721](https://github.com/cosmos/ibc/blob/main/spec/app/ics-721-nft-transfer/README.md) protocol to transfer nft to other chains. For specific operations, refer to the [document](ics721-cmd.md)

## Endpoints

- **p2p seeds : `c5f4b33d904adaeacc1ca05bfcd7376ca4d51519@tenderseed.ccvalidators.com:29029`**
- **p2p persistent peers : `4b5cee15e6a9c4b96b8c1c4f396a18b0461edc17@104.248.161.33:26656,835173badfc41ecbd867a0395c6a452bda2bb90f@178.62.105.39:26656`**

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
