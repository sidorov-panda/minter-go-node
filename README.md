# Minter Node

Minter is a blockchain network that lets people, projects, and companies issue and manage their own coins and trade them at a fair market price with absolute and instant liquidity.

[![version](https://img.shields.io/github/tag/MinterTeam/minter-go-node.svg)](https://github.com/MinterTeam/minter-go-node/releases/latest)
[![Go version](https://img.shields.io/badge/go-1.10-blue.svg)](https://github.com/moovweb/gvm)
[![license](https://img.shields.io/github/license/MinterTeam/minter-go-node.svg)](https://github.com/MinterTeam/minter-go-node/blob/master/LICENSE)
[![last-commit](https://img.shields.io/github/last-commit/MinterTeam/minter-go-node.svg)](https://github.com/MinterTeam/minter-go-node/commits/master)
[![Documentation Status](//readthedocs.org/projects/minter-go-node/badge/?version=latest)](https://minter-go-node.readthedocs.io/en/latest/?badge=latest)
[![Go Report Card](https://goreportcard.com/badge/github.com/MinterTeam/minter-go-node)](https://goreportcard.com/report/github.com/MinterTeam/minter-go-node)

_NOTE: This is alpha software. Please contact us if you intend to run it in production._

## Installation

You can get official installation instructions in our [docs](https://minter-go-node.readthedocs.io/en/dev/install.html).

## Documentation

For documentation, [Read The Docs](https://minter-go-node.readthedocs.io/en/dev/).

## Versioning

### SemVer

Minter uses [SemVer](http://semver.org/) to determine when and how the version changes.
According to SemVer, anything in the public API can change at any time before version 1.0.0

To provide some stability to Minter users in these 0.X.X days, the MINOR version is used
to signal breaking changes across a subset of the total public API. This subset includes all
interfaces exposed to other processes, but does not include the in-process Go APIs.

### Upgrades

In an effort to avoid accumulating technical debt prior to 1.0.0,
we do not guarantee that breaking changes (ie. bumps in the MINOR version)
will work with existing blockchain. In these cases you will
have to start a new blockchain, or write something custom to get the old
data into the new chain.

However, any bump in the PATCH version should be compatible with existing histories
(if not please open an [issue](https://github.com/MinterTeam/minter-go-node/issues)).