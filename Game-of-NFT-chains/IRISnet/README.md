# IRISnet Chain Information

Contents

- Chain
- Endpoints
- Join Validator Set
- Explorer
- Faucet
- Other

## Chain

### Binary

The binary published in this repo is the `iris` binary built using the `irishub` repo branch [feature/gon](https://github.com/irisnet/irishub/tree/feature/gon).

- [Linux amd64 build](iris)
- SHA256: `071d7ee2765dc97206391aa64cd42e23e9847c179ab1c4e72eb1811b2c157047`

You can generate the binary following the build instructions.

#### Install go

Install `go` by following the [official docs](https://golang.org/doc/install).**Go 1.19+ is required for building and installing the IRIShub software**
Remember to set your `$GOPATH`, `$GOBIN`, and `$PATH` environment variables, for example:

```bash
mkdir -p $HOME/go/bin
echo "export GOPATH=$HOME/go" >> ~/.bashrc
source ~/.bashrc
echo "export GOBIN=$GOPATH/bin" >> ~/.bashrc
source ~/.bashrc
echo "export PATH=$PATH:$GOBIN" >> ~/.bashrc
source ~/.bashrc
```

Verify that `go` has been installed successfully

```bash
go version
```

#### Install `iris`

After setting up `go` correctly, you should be able to compile and run `iris`.

Make sure that your server can access to google.com because our project depends on some libraries provided by google. (If you are not able to access google.com, you can also try to add a proxy: `export GOPROXY=https://goproxy.io`)

```bash
git clone https://github.com/irisnet/irishub
cd irishub
git checkout feature/gon
make install
```

If your environment variables have set up correctly, you should not get any errors by running the above commands.
Now check your `iris` version.

```bash
iris version
```

### Genesis file

Final genesis file: **[genesis.json](genesis.json)**

- SHA256: `1b68518edac034127c06254af084dce5f1a9c547f64be79b89ec818a26b8f56c`
- Validators must replace their `config/genesis.json` file with this one before running the binary.

The genesis file with was generated using the following settings:

- Chain ID: `iris-1`
- Denom: `uiris`
- Signed blocks window: `"8640"`
- Two additional genesis accounts were added to provide funds for a faucet and a relayer that will be run by the testnet coordinators.

## Endpoints

- **p2p seeds : `c5f4b33d904adaeacc1ca05bfcd7376ca4d51519@tenderseed.ccvalidators.com:29029`**
- **p2p persistent peers : `4b5cee15e6a9c4b96b8c1c4f396a18b0461edc17@104.248.161.33:26656,835173badfc41ecbd867a0395c6a452bda2bb90f@178.62.105.39:26656`**

## Join Validator Set

On the node machine:

- Copy the `node_key.json` and `priv_validator_key.json` files for your validator.
- Run one of the following scripts:
  - Apollo service: [apollo-init.sh](apollo-init.sh)
  - Cosmovisor service: [apollo-init-cv.sh](apollo-init-cv.sh)

## Other
