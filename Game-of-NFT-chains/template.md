# How to Join

The reading object of this document is the chain team participating in the establishment of the GoN testnet. Currently, the main chain parties involved in the activity are IRISnet, Stargaze, and Uptick. The [ics721](https://github.com/cosmos/ibc/blob/main/spec/app/ics-721-nft-transfer/README.md) protocol that these chains have already loaded supports nft cross-chain transfer . In order to facilitate participation in the ics721 test team, each chain team needs to complete the documentation, which currently mainly includes the following parts:

- Chain
- Endpoints
- Explorer
- Faucet
- Relayer
- Other

## Chain

The main reason is that the executable files needed to start the node have been parameterized, such as the genesis file. If the chain team provides a compiled executable file, you need to specify the sha256hash information of the executable file, the code factory library used, and the version. If no executable file is provided, the chain team is required to provide detailed information such as compiled scripts and execution environment.

In addition, the chain team is also required to provide detailed command-line documents about the ics721 part of the chain for the test team to perform tasks, as well as documents on how to join the validator set.

## Endpoints

This part requires the chain team to provide available chain end point information for validators to join, mainly including:

- p2p seeds
- p2p persistent peers
  
## Explorer

This part requires the chain team to provide the browser information of the chain, so that the contestants can query the information they need.

## Faucet

The chain team needs to provide a way to collect test coins to facilitate the contestants to participate in the competition.

## Relayer

The chain team needs to provide the available relayer information for this chain to communicate with other chains, including code factory library, version, etc.

## Other

Other additional supplementary information.
