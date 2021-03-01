# Swap

Copyright (c) 2014-2019 The Monero Project.   
Crypto is based on [Monero](README_original.md) and is forked from Swap.

![Build-Linux](https://github.com/cryptocoin-dev/swap/workflows/Build-Linux/badge.svg)

## Production & Development

Active Branches:
- Stable: master(latest/release)
- Unstable: crypto-v3.2dev(latest)
- Testing: N/A

To contribute to the Crypto Project, please make all pull requests to the _crypto-v3.2dev_ branch.<br/>
For production, please use the _latest or tagged release_ of the _master_ branch.

## Resources
- Webpage: [crypt-o-coin.cash](https://crypt-o-coin.cash)
- Explorer: [explorer.crypt-o-coin.cash](https://explorer.crypt-o-coin.cash)
- Pool List: [miningpoolstats.stream/crypto](https://miningpoolstats.stream/crypto)
- GitHub: [https://github.com/GonzoTheDev/crypto](https://github.com/GonzoTheDev/crypto)

## Social/Contact

- Bitcointalk [https://bitcointalk.org/index.php?topic=5320548](https://bitcointalk.org/index.php?topic=5320548)
- Discord: [https://discord.gg/upPCtgcMJu](https://discord.gg/upPCtgcMJu)
- Reddit: [r/CryptoCoinProject/](https://www.reddit.com/r/CryptoCoinProject/)
- Twitter: [@CryptoC54328932](https://twitter.com/CryptoC54328932)
- Email: gonzosoftware0@gmail.com

## Specifications & Emission

- Coin ticker: CRYPTO
- Total supply: 600,000,000 coins before tail emission
- Tail emission: ~158,000 coins each year (starting at year 8)
- Decimal places: 12
- PoW hash algorithm: Cuckaroo29s
- Block time: 15 seconds
- Difficulty Adjustment Algorithm: Monero DAA
- Genesis block: 2021-03-01 (March 01, 2021) at 00:00:00 (UTC)
- Premine: No
- Developer fee: No
- Founders reward: No
- Mainnet default P2P port: 11111
- Mainnet default RPC port: 22222

## Donation Address
CRYPTOADDRESS

## Build on linux

install deps:

`sudo apt-get install build-essential cmake pkg-config libboost-all-dev libssl-dev libzmq3-dev libunbound-dev libsodium-dev libreadline6-dev libpgm-dev libnorm-dev`

clone repo:

`git clone --recursive https://github.com/GonzoTheDev/crypto`

build daemon and wallet:

`cd crypto && mkdir build && cd build && cmake .. && make daemon simplewallet`

or build everything:

`cd crypto && mkdir build && cd build && cmake .. && make`

## Build on Windows (using MinGW)

install deps:

`pacman -S mingw-w64-x86_64-toolchain make mingw-w64-x86_64-cmake mingw-w64-x86_64-boost mingw-w64-x86_64-openssl mingw-w64-x86_64-zeromq mingw-w64-x86_64-libsodium mingw-w64-x86_64-hidapi`

clone repo:

`git clone --recursive https://github.com/GonzoTheDev/crypto`

build daemon and wallet:

`cd crypto && make release-static-win64`

