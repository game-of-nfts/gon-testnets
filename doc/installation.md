# Installation

This section provides instructions for participants on how to install client software.

To play the game, participants should use the specified versions of the following software:

| Software                  | Tag                | Version           |
| ------------------------- | ------------------ | ----------------- |
| [iris](#iris)             | v1.4.1-gon-testnet | 1.4.1-gon-testnet |
| [starsd](#stargaze)       | v8.1.0             | 8.1.0             |
| [junod](#juno)            | v12.0.0            | v12.0.0           |
| [uptickd](#uptick)        | v0.2.6             | v0.2.6            |
| [omniflixhubd](#omniflix) | v0.9.0-gon-test2   | v0.9.0-gon-test2  |

## Prerequisite

To install go, please follow [the official documentation](https://golang.org/doc/install). It is recommended to have Go 1.19 or higher installed for building and installing client software.

After installing go, you need to set the environment variables $GOPATH, $GOBIN, and $PATH:

```bash
mkdir -p $HOME/go/bin
echo "export GOPATH=$HOME/go" >> ~/.bashrc
source ~/.bashrc
echo "export GOBIN=$GOPATH/bin" >> ~/.bashrc
source ~/.bashrc
echo "export PATH=$PATH:$GOBIN" >> ~/.bashrc
source ~/.bashrc
```

To verify that go has been installed successfully on your system, you can run the following command in your terminal:

```bash
go version
```

In addition, before installing any software that depends on libraries provided by Google, you should make sure that your server can access `google.com`. If you are not able to access `google.com`, you can try adding a proxy by running the following command in your terminal:

```bash
echo "export GOPROXY=https://goproxy.io" >> ~/.bashrc
source ~/.bashrc
```

## Install dependencies
```
sudo apt install curl build-essential git wget jq make gcc tmux chrony -y
```

## Clients

### Iris

To install `iris` client, follow the steps below:

```bash
git clone https://github.com/irisnet/irishub.git
cd irishub
git checkout v1.4.1-gon-testnet
make install
```

If your environment variables are set up correctly, you should not encounter any errors while running the above commands. To verify the iris version installed on your system, run the following command:

```bash
iris version
```

### Stargaze

To install `starsd` client, follow the steps below:

```bash
git clone https://github.com/public-awesome/stargaze.git
cd stargaze
git checkout v8.1.0
make install
```

If your environment variables are set up correctly, you should not encounter any errors while running the above commands. To verify the `starsd` version installed on your system, run the following command:

```bash
starsd version 
```

### Juno

To install `junod` client, follow the steps below:

```bash
git clone https://github.com/CosmosContracts/juno.git
cd juno
git checkout v12.0.0 
make install
```

If your environment variables are set up correctly, you should not encounter any errors while running the above commands. To verify the `junod` version installed on your system, run the following command:

```bash
junod version
```

### Uptick

To install `uptickd` client, follow the steps below:

```bash
git clone https://github.com/UptickNetwork/uptick.git
cd uptick
make install
```

If your environment variables are set up correctly, you should not encounter any errors while running the above commands. To verify the `uptickd` version installed on your system, run the following command:

```bash
uptickd version
```

### Omniflix

To install `omniflixhubd` client, follow the steps below:

```bash
git clone https://github.com/OmniFlix/omniflixhub.git
cd omniflixhub
git checkout v0.9.0-gon-test2
make install
```

If your environment variables are set up correctly, you should not encounter any errors while running the above commands. To verify the `omniflixhubd` version installed on your system, run the following command:

```bash
omniflixhubd version
```
