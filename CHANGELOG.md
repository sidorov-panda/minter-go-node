# Changelog

## TBD

- [api] Add validators rewards to block api

## 0.1.8
*Aug 4th, 2018*

BUG FIXES
- [core] Critical fix

## 0.1.7
*Jule 30th, 2018*

BREAKING CHANGES

- [testnet] New testnet id

IMPROVEMENT

- [validators] Added flag ``--reset-private-validator``
- [testnet] Main validator stake is set to 1 mln MNT by default

## 0.1.6
*Jule 30th, 2018*

BREAKING CHANGES

- [testnet] New testnet id

BUG FIXES

- [core] Fixed critical bug

## 0.1.5
*Jule 28th, 2018*

BUG FIXES

- [tendermint] Update tendermint to 0.22.8
- [core] Temporary critical fix

## 0.1.4
*Jule 25th, 2018*

IMPROVEMENT

- [tendermint] Update tendermint to 0.22.6

## 0.1.3
*Jule 25th, 2018*

IMPROVEMENT

- [tendermint] Update tendermint to 0.22.5

## 0.1.0
*Jule 23th, 2018*

BREAKING CHANGES

- [core] 0.1x transaction fees
- [core] Genesis is now encapsulated in code
- [core] Add new transaction type: SellAllCoin
- [core] Add GasCoin field to transaction
- [config] New config directories
- [api] Huge API update. For more info see docs

IMPROVEMENT

- [binary] Now Minter is available as single binary. There is no need to install Tendermint
- [config] 10x default send/recv rate
- [config] Recheck after empty blocks
- [core] Check transaction nonce before adding to mempool
- [performance] Huge performance enhancement due to getting rid of network overhead between tendermint and minter
- [gui] GUI introduced! You can use it by visiting http://localhost:3000/ in your local browser

BUG FIXES

- [api] Fixed raw transaction output

## 0.0.6
*Jule 16th, 2018*

BREAKING CHANGES

- [core] Change commissions
- [testnet] New testnet id
- [core] Fix transaction decoding issue
- [core] Remove transaction ConvertCoin, add SellCoin and BuyCoin. For details see the docs.
- [core] Coin name is now limited to max 64 bytes
- [api] Update estimate exchange endpoint

IMPROVEMENT

- [api] Update transaction api
- [api] Add transaction result to block api
- [mempool] Mempool cache is disabled
- [tendermint] Updated to v0.22.4
- [versioning] Adapt Semantic Versioning https://semver.org/
- [client] Add --disable-api flag to client

## 0.0.5
*Jule 4rd, 2018*

BREAKING CHANGES

- [core] Remove Reserve Coin from coin object. All coins should be reserved with base coin
- [core] Limit tx payload and service data to 128 bytes
- [core] Fix critical issue with instant convert of 2 custom coins 
- [testnet] New testnet chain id (minter-test-network-9)
- [tendermint] Switched to v0.22.0

IMPROVEMENT

- [api] Fix issue with not found coins

BUG FIXES

- [api] Fix transaction endpoint

## 0.0.4

*June 24th, 2018*

BREAKING CHANGES

- [validators] Reward now is payed each 12 blocks
- [validators] Change total "validators' power" to 100 mln
- [tendermint] Switched to v0.21.0
- [testnet] New testnet chain id
- [api] Changed */api/block* response format

IMPROVEMENT

- [docs] Updated docs

BUG FIXES

- [validators] Fixed issue with incorrect pubkey length
