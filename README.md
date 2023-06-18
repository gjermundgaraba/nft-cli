# nft-cli

The NFT cli is an _interactive_ command line tool for interacting with the NFTs in the interchain (currently, the Cosmos
ecosystem).

![gon.gif](./gon.gif)

The goal of this CLI is to let users easily manage their NFTs across multiple chains. It is currently in development and
is not ready for production use.

Most of this CLI was built during the game of NFT hackathon phase 1 to help people do different tasks. It is
currently being repurposed to be a more general tool for managing NFTs. After the hackathon the plan is to
add support for mainnets and make it easy to configure and use for anyone (who is at least somewhat comfortable with the
command line). To see the previous version of this CLI, see
the [gon tools repo](https://github.com/gjermundgaraba/gon-tools)

## Features

One of the key features of the cli is the ability to **self-relay nft-transfers** without having to actually set up and
configure a relayer yourself, or relay anyone else's transactions.

| Chain                  | Create Class | Mint NFTs | Transfer NFTs (over IBC) | Query NFTs |
|------------------------|--------------|-----------|--------------------------|------------|
| IRIS (GoN testnet)     | ✅            | ✅         | ✅                        | ✅          |
| Stargaze (GoN testnet) | ❌            | ❌         | ✅                        | ✅          |
| Juno (GoN testnet)     | ❌            | ❌         | ✅                        | ✅          |
| Uptick (GoN testnet)   | ❌            | ❌         | ✅                        | ✅          |
| OmniFlix (GoN testnet) | ✅            | ✅         | ✅                        | ✅          |

Extra helper tools and features:

- ✅ Self relaying ([docs](./self-relay.md))
- ✅ IBC Transaction lookup
- ✅ Key management
- ✅ Multiline editor for NFT metadata
- ✅ List IBC Connections
- ✅ Calculate Class Hash
- ✅ Generate Class IBC trace (by choosing each hop)
- ✅ Generate relay commands so that you can relay yourself with `rly` or `hermes` on the paths you need only

## Installation

1. Install go (https://go.dev/doc/install)
2. `go build -o . ./...`
3. `./nft-cli` 

Next you can add the binary to your path or just use it from the current directory.

You can also download the binary (for linux) from the releases page.

## Future work

- Add support for mainnets
- Add support for self-config (with a config file and via the CLI itself)
- Incorporate Stargaze indexer to make querying NFTs easier
- Add user guide (both as a doc and inline in the CLI during operation to guide users better)
- Better key management
- Improve docs and contribution guidelines
