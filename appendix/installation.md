# Installation

This section instructs users on how to install the client software.

| Software     | Branch             | Version           |
| ------------ | ------------------ | ----------------- |
| iris         | v1.4.1-gon-testnet | 1.4.1-gon-testnet |
| starsd       | v8.1.0             | 8.1.0             |
| junod        | v12.0.0            | v12.0.0           |
| uptickd      | v0.2.5             | v0.2.5            |
| omniflixhubd | v0.9.0-gon-test    | 0.9.0-gon-test    |

## Prerequisite

Install `go` by following the [official docs](https://golang.org/doc/install). **Go 1.19+ is required for building and installing the IRIShub software**
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

Make sure that your server can access to google.com because our project depends on some libraries provided by google. (If you are not able to access google.com, you can also try to add a proxy: `export GOPROXY=https://goproxy.io`)

## Iris

After setting up `go` correctly, you should be able to compile and run `iris`.

```bash
git clone https://github.com/irisnet/irishub.git
cd irishub
git checkout v1.4.1-gon-testnet
make install
```

If your environment variables have set up correctly, you should not get any errors by running the above commands.
Now check your `iris` version.

```bash
iris version
```

## Stargaze

After setting up `go` correctly, you should be able to compile and run `starsd`.

```bash
git clone https://github.com/public-awesome/stargaze.git
cd stargaze
git checkout v8.1.0
make install
```

If your environment variables have set up correctly, you should not get any errors by running the above commands.
Now check your `starsd` version.

```bash
starsd version 
```

## Juno

After setting up `go` correctly, you should be able to compile and run `junod`.

```bash
git clone https://github.com/CosmosContracts/juno.git
cd juno
git checkout v12.0.0 
make install
```

If your environment variables have set up correctly, you should not get any errors by running the above commands.
Now check your `junod` version.

```bash
junod version
```

## Uptick

After setting up `go` correctly, you should be able to compile and run `uptickd`.

```bash
git clone https://github.com/UptickNetwork/uptick.git
cd irishub
git checkout v0.2.5
make install
```

If your environment variables have set up correctly, you should not get any errors by running the above commands.
Now check your `uptickd` version.

```bash
uptickd version
```

## Omniflix

After setting up `go` correctly, you should be able to compile and run `omniflixhubd`.

```bash
git clone https://github.com/OmniFlix/omniflixhub.git
cd omniflixhub
git checkout v0.9.0-gon-test
make install
```

If your environment variables have set up correctly, you should not get any errors by running the above commands.
Now check your `omniflixhubd` version.

```bash
omniflixhubd version
```