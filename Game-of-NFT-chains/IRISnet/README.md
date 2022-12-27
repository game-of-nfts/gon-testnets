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

### Operattion guide about ics721

## Endpoints

- **p2p seeds : `c5f4b33d904adaeacc1ca05bfcd7376ca4d51519@tenderseed.ccvalidators.com:29029`**
- **p2p persistent peers : `4b5cee15e6a9c4b96b8c1c4f396a18b0461edc17@104.248.161.33:26656,835173badfc41ecbd867a0395c6a452bda2bb90f@178.62.105.39:26656`**

## Explorer

## Faucet

## Relayer

## Other
