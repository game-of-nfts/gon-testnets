# Install

## Install go

Install `go` by following the [official docs](https://golang.org/doc/install).**Go 1.18+ is required for building and installing the Uptick software**
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

## Install `uptickd`

After setting up `go` correctly, you should be able to compile and run `uptickd`.

Make sure that your server can access to google.com because our project depends on some libraries provided by google. (If you are not able to access google.com, you can also try to add a proxy: `export GOPROXY=https://goproxy.io`)

```bash
git clone https://github.com/UptickNetwork/uptick
cd uptick
git checkout gon
make install
```

If your environment variables have set up correctly, you should not get any errors by running the above commands.
Now check your `uptickd` version.

```bash
uptickd version
```

### Genesis file

Final genesis file: **[genesis.json](genesis.json)**

- SHA256: `f96764c7ae1bc713b2acc87b5320f2d10ee26716b3daa6cc455cb3a3906f05c2`
- Validators must replace their `config/genesis.json` file with this one before running the binary.

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