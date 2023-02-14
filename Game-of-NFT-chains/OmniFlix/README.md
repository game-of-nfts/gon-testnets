# OmniFlixHub Chain Information

## Chain

### Binary

The binary published in this repo is the `omniflixhubd` binary built using the `omniflixhub` repo branch [omniflix-gon](https://github.com/OmniFlix/omniflixhub/tree/omniflix-gon).

- [Linux amd64 build](omniflixhubd)
- SHA256: `TBA`

You can generate the binary following the [build instructions](install.md).

### Genesis file

Final genesis file: **[genesis.json](genesis.json)**

- SHA256: `TBA`
- Validators must replace their `config/genesis.json` file with this one before running the binary.

The genesis file with was generated using the following settings:

- Chain ID: `gon-flixnet-1`
- Denom: `uflix`
- Signed blocks window: `"8640"`
- Two additional genesis accounts were added to provide funds for a faucet and a relayer that will be run by the testnet coordinators.

### Join the validator set

1. If you don't have a node configuration file yet, you can initialize a node with the following command:

```bash
omniflixhubd init <moniker> --chain-id=gon-flixnet-1 --home=~/.omniflixhub
```

2. Use the genesis.json provided by the chain team to overwrite the locally generated genesis.json file

```bash
curl -o ~/.omniflixhub/config/genesis.json `link_to_genesis`
```

3. Modify the config.toml file using the configuration provided in [Endpoints](#endpoints)
4. Start node

```bash
omniflixhubd start --home=~/.omniflixhub
```

5. Receive tokens from the [faucet](#faucet) and join the set of validators

```bash
omniflixhubd tx staking create-validator \
    --pubkey=$(omniflixhubd tendermint show-validator) \
    --moniker=<your-validator-name> \
    --amount=<amount-to-be-delegated, e.g. 10000000uflix> \
    --min-self-delegation=1 \
    --commission-max-change-rate=0.1 \
    --commission-max-rate=0.1 \
    --commission-rate=0.1 \
    --gas=100000 \
    --fees=500uflix \
    --chain-id=gon-flixnet-1 \
    --from=<key-name>
```

### Operattion guide about ics721

The nft implemented by each chain may be different. Use the chain of the [onft](https://github.com/OmniFlix/onft/tree/onft-gon/modules/nft) module in OmniFlix. For operations such as the creating collection and transfer of nft, please refer to the [documentation](https://github.com/omniflix/onft#onft)

After users creates nft, they can use the [ics721](https://github.com/cosmos/ibc/blob/main/spec/app/ics-721-nft-transfer/README.md) protocol to transfer nft to other chains. For specific operations, refer to the [document](ics721-cmd.md)

## Endpoints

- **p2p seeds : ``**
- **p2p persistent peers : ``**

## Explorer

These block explorers allow you to search, view and analyze OmniFlixHub data—like blocks, transactions, validators, governance including params or proposals, etc.
```
TBA
```

## Faucet

```
TBA
```
## Relayer

The repeaters currently supporting ics721 are as follows：

- [Cosmos Go Relayer](https://github.com/cosmos/relayer/releases/tag/v2.1.2)

## Other
