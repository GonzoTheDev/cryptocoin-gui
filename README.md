![Logo](https://raw.githubusercontent.com/GonzoTheDev/cryptocoin-gui/master/images/appicons/256x256.png)

# CryptoCoin Wallet GUI

Copyright (c) 2021, The CryptoCoin Project

![Build-Linux](https://github.com/swap-dev/swap-gui/workflows/Build-Linux/badge.svg)

## Resources

- Homepage: [crypt-o-coin.cash](https://crypt-o-coin.cash/)
- Discord: [https://discord.gg/upPCtgcMJu](https://discord.gg/upPCtgcMJu)
- Explorer: [explorer.crypt-o-coin.cash](https://explorer.crypt-o-coin.cash/)
- Reference Pool: [mining.crypt-o-coin.cash](https://mining.crypt-o-coin.cash)
- Pool List: [miningpoolstats.stream/crypto](https://miningpoolstats.stream/crypto)
- Markets: [coinmarketcap.com](https://coinmarketcap.com/currencies/crypto/markets/)


## Introduction

CryptoCoin is a private, secure, untraceable, decentralised digital currency. You are your bank, you control your funds, and nobody can trace your transfers unless you allow them to do so.

**Privacy:** CryptoCoin uses a cryptographically sound system to allow you to send and receive funds without your transactions being easily revealed on the blockchain (the ledger of transactions that everyone has). This ensures that your purchases, receipts, and all transfers remain absolutely private by default.

**Security:** Using the power of a distributed peer-to-peer consensus network, every transaction on the network is cryptographically secured. Individual wallets have a 25 word mnemonic seed that is only displayed once, and can be written down to backup the wallet. Wallet files are encrypted with a passphrase to ensure they are useless if stolen.

**Untraceability:** By taking advantage of ring signatures, a special property of a certain type of cryptography, CryptoCoin is able to ensure that transactions are not only untraceable, but have an optional measure of ambiguity that ensures that transactions cannot easily be tied back to an individual user or computer.

## About this project

This is the GUI for the [core CryptoCoin implementation](https://github.com/GonzoTheDev/crypto). It is open source and completely free to use without restrictions, except for those specified in the license agreement below. There are no restrictions on anyone creating an alternative implementation of CryptoCoin that uses the protocol and network in a compatible manner.

As with many development projects, the repository on Github is considered to be the "staging" area for the latest changes. Before changes are merged into that branch on the main repository, they are tested by individual developers in their own branches, submitted as a pull request, and then subsequently tested by contributors who focus on testing and code reviews. That having been said, the repository should be carefully considered before using it in a production environment, unless there is a patch in the repository for a particular show-stopping issue you are experiencing. It is generally a better idea to use a tagged release for stability.

## Supporting the project

CryptoCoin is a 100% community-sponsored endeavor. If you want to join our efforts, the easiest thing you can do is support the project financially. Both CryptoCoin, Swap and Bitcoin donations can be made below.

The CryptoCoin donation address is: `cashHsZY9eefTt2TrFjhVoMBPp17jjjN142gM3h9Qy7jZqMviQuMM9rbCjujk5G5i5A4bUPUgEBbnehaCXizUJEn6n4d6NpMNk` (viewkey: `bb69a4eb99bc4f339ac2d453bc248f6885fcc4518107406a84fc4b33a98bc407`)

The Swap donation address is: `fh2QarMUyHu5auz39ULrTKNXWdSVvQ2SKEnkxXwfkfiCau7cBMzRpt3exo4PVj6xVcgZjYYDCgRoTNg2HWqw4bCj2SJ4AS386` (viewkey: `0b9802716de1ab773c6f2355d5610847dd5919d298dbc74d4af0c488ac60aa07`)

The Bitcoin donation address is: `1CryptoXLcGvaEtNGMwRF4SpLaXZ3d5kNg`


## License

See [LICENSE](LICENSE).

## Installing the CryptoCoin GUI from a package

Packages are available for

* Arch Linux: pacman -S cryptocoin-gui
* Void Linux: xbps-install -S cryptocoin-core
* GuixSD: guix package -i cryptocoin-core

Packaging for your favorite distribution would be a welcome contribution!

## Compiling the CryptoCoin GUI from source

*Note*: Qt 5.9.7 is the minimum version required to build the GUI.

### On Linux:

(Tested on Ubuntu 17.10 x64, Ubuntu 18.04 x64 and Gentoo x64)

1. Install CryptoCoin dependencies

  - For Debian distributions (Debian, Ubuntu, Mint, Tails...)

	`sudo apt install build-essential cmake libboost-all-dev miniupnpc libunbound-dev graphviz doxygen libunwind8-dev pkg-config libssl-dev libzmq3-dev libsodium-dev libhidapi-dev libnorm-dev libusb-1.0-0-dev libpgm-dev libprotobuf-dev protobuf-compiler libgcrypt20-dev`

  - For Gentoo

	`sudo emerge app-arch/xz-utils app-doc/doxygen dev-cpp/gtest dev-libs/boost dev-libs/expat dev-libs/openssl dev-util/cmake media-gfx/graphviz net-dns/unbound net-libs/ldns net-libs/miniupnpc net-libs/zeromq sys-libs/libunwind dev-libs/libsodium dev-libs/hidapi dev-libs/libgcrypt`

  - For Fedora

	`sudo dnf install make automake cmake gcc-c++ boost-devel miniupnpc-devel graphviz doxygen unbound-devel libunwind-devel pkgconfig openssl-devel libcurl-devel hidapi-devel libusb-devel zeromq-devel libgcrypt-devel`

2. Install Qt:

  *Note*: The Qt 5.9.7 or newer requirement makes **some** distributions (mostly based on debian, like Ubuntu 16.x or Linux Mint 18.x) obsolete due to their repositories containing an older Qt version.

 The recommended way is to install 5.9.7 from the [official Qt installer](https://www.qt.io/download-qt-installer) or [compiling it yourself](https://wiki.qt.io/Install_Qt_5_on_Ubuntu). This ensures you have the correct version. Higher versions *can* work but as it differs from our production build target, slight differences may occur.

The following instructions will fetch Qt from your distribution's repositories instead. Take note of what version it installs. Your mileage may vary.

  - For Ubuntu 17.10+

    `sudo apt install qtbase5-dev qt5-default qtdeclarative5-dev qml-module-qtquick-controls qml-module-qtquick-controls2 qml-module-qtquick-dialogs qml-module-qtquick-xmllistmodel qml-module-qt-labs-settings qml-module-qt-labs-folderlistmodel qttools5-dev-tools qml-module-qtquick-templates2 libqt5svg5-dev`

  - For Gentoo

    `sudo emerge dev-qt/qtcore:5 dev-qt/qtdeclarative:5 dev-qt/qtquickcontrols:5 dev-qt/qtquickcontrols2:5 dev-qt/qtgraphicaleffects:5`

  - Optional : To build the flag `WITH_SCANNER`

    - For Ubuntu

      `sudo apt install qtmultimedia5-dev qml-module-qtmultimedia libzbar-dev`

    - For Gentoo

      The *qml* USE flag must be enabled.

      `emerge dev-qt/qtmultimedia:5 media-gfx/zbar`


3. Clone repository

    `git clone https://github.com/GonzoTheDev/cryptocoin-gui.git`

4. Build

    ```
    cd cryptocoin-gui
    QT_SELECT=5 ./build.sh
    ```

The executable can be found in the build/release/bin folder.

### On OS X:

1. Install Xcode from AppStore

2. Install [homebrew](http://brew.sh/)

3. Install [cryptocoin](https://github.com/GonzoTheDev/crypto) dependencies:

  `brew install boost hidapi zmq libpgm miniupnpc ldns expat libunwind-headers protobuf libgcrypt PkgConfig openssl`

4. Install Qt:

  `brew install qt5`  (or download QT 5.9.7+ from [qt.io](https://www.qt.io/download-open-source/))

5. Add the Qt bin directory to your path

  - Example for Qt: `export PATH=$PATH:$HOME/Qt/5.9.7/clang_64/bin`
  - Example for Homebrew: `export PATH=$PATH:/usr/local/opt/qt/bin`

6. Grab an up-to-date copy of the cryptocoin-gui repository

  `git clone https://github.com/GonzoTheDev/cryptocoin-gui.git`

7. Go into the repository

  `cd cryptocoin-gui`

8. Install the submodule libraries

  `./get_libwallet_api.sh`
  
9. Start the build

  `./build.sh`

The executable can be found in the `build/release/bin` folder.

### On Windows:

The CryptoCoin GUI on Windows is 64 bits only; 32-bit Windows GUI builds are not officially supported anymore.

1. Install [MSYS2](https://www.msys2.org/), follow the instructions on that page on how to update system and packages to the latest versions

2. Open an 64-bit MSYS2 shell: Use the *MSYS2 MinGW 64-bit* shortcut, or use the `msys2_shell.cmd` batch file with a `-mingw64` parameter

3. Install MSYS2 packages for CryptoCoin dependencies; the needed 64-bit packages have `x86_64` in their names

    ```
    pacman -S mingw-w64-x86_64-toolchain make mingw-w64-x86_64-cmake mingw-w64-x86_64-boost mingw-w64-x86_64-openssl mingw-w64-x86_64-zeromq mingw-w64-x86_64-libsodium mingw-w64-x86_64-hidapi mingw-w64-x86_64-protobuf-c mingw-w64-x86_64-libusb mingw-w64-x86_64-libgcrypt
    ```

    Optional : To build the flag `WITH_SCANNER`

      ```
      pacman -S mingw-w64-x86_64-zbar
      ```

    You find more details about those dependencies in the [CryptoCoin documentation](https://github.com/GonzoTheDev/crypto). Note that that there is no more need to compile Boost from source; like everything else, you can install it now with a MSYS2 package.

4. Install Qt5

    ```
    pacman -S mingw-w64-x86_64-qt5
    ```

    There is no more need to download some special installer from the Qt website, the standard MSYS2 package for Qt will do in almost all circumstances.

5. Install git

    ```
    pacman -S git
    ```

6. Clone repository

    ```
    git clone https://github.com/GonzoTheDev/cryptocoin-gui.git
    ```

7. Build

    ```
    cd cryptocoin-gui
    source ./build.sh release-static
    cd build
    make deploy
    ```

    **Note:** The use of `source` above is a dirty workaround for a suspected bug in the current QT version 5.11.2-3 available in the MSYS2 packaging system, see https://github.com/monero-project/monero-gui/issues/1559 for more info.

The executable can be found in the `.\release\bin` directory.
