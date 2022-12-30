# IRISnet Chain Information

## Chain

### Binary

The binary published in this repo is the `iris` binary built using the `irishub` repo branch [feature/gon](https://github.com/irisnet/irishub/tree/feature/gon).

- [Linux amd64 build](iris)
- SHA256: `071d7ee2765dc97206391aa64cd42e23e9847c179ab1c4e72eb1811b2c157047`

You can generate the binary following the [build instructions](install.md).

### Genesis file

Final genesis file: **[genesis.json](genesis.json)**

- SHA256: `1b68518edac034127c06254af084dce5f1a9c547f64be79b89ec818a26b8f56c`
- Validators must replace their `config/genesis.json` file with this one before running the binary.

The genesis file with was generated using the following settings:

- Chain ID: `iris-1`
- Denom: `uiris`
- Signed blocks window: `"8640"`
- Two additional genesis accounts were added to provide funds for a faucet and a relayer that will be run by the testnet coordinators.

### Join the validator set

1. If you don't have a node configuration file yet, you can initialize a node with the following command:

```bash
iris init <moniker> --chain-id=iris-1 --home=~/.iris
```

2. Use the genesis.json provided by the chain team to overwrite the locally generated genesis.json file

```bash
curl -o ~/.iris/config/genesis.json https://raw.githubusercontent.com/bianjieai/gon-testnets/Game-of-NFT-chains/IRISnet/genesis.json
```

3. Modify the config.toml file using the configuration provided in [Endpoints](#endpoints)
4. Start node

```bash
iris start --home=~/.iris
```

5. Receive tokens from the [faucet](#faucet) and join the set of validators

```bash
iris tx staking create-validator \
    --pubkey=$(iris tendermint show-validator) \
    --moniker=<your-validator-name> \
    --amount=<amount-to-be-delegated, e.g. 10000iris> \
    --min-self-delegation=1 \
    --commission-max-change-rate=0.1 \
    --commission-max-rate=0.1 \
    --commission-rate=0.1 \
    --gas=100000 \
    --fees=0.6iris \
    --chain-id=iris-1 \
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

- [iobscan](https://irishub.iobscan.io/)
- [mintscan](https://irishub.mintscan.io/)

## Faucet

Welcome to get test tokens in our [testnet faucet channel](https://discord.gg/Z6PXeTb5Mt).
Usage: in [nyancat-faucet channel](https://discord.gg/Z6PXeTb5Mt), type "$faucet " + your address on Nyancat testnet, to get test tokens (NYAN) every 24 hours.

## Relayer

The repeaters currently supporting ics721 are as follows：

- [Cosmos Go Relayer](https://github.com/cosmos/relayer/releases/tag/v2.1.2)

## Other
