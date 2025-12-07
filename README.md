# GNTL Coin
<img src="https://github.com/The-GNTL-Project/Images/raw/master/GNTL_Icon_Round_200x200.png" alt="GNTL Coin">

Copyright (c) 2021-2024, The GNTL Project    
Copyright (c) 2018-2020, The Arqma Network   
Copyright (c) 2014-2020, The Monero Project  
Portions Copyright (c) 2012-2013 The Cryptonote developers.

## Table of Contents

  - [Specifications](#specifications)
  - [Resources](#resources)
  - [Introduction](#introduction)
  - [SSL](#ssl)
  - [About this project](#about-this-project)
  - [Supporting the project](#supporting-the-project)
  - [License](#license)
  - [Contributing](#contributing)
  - [Compiling GNTL from source](#compiling-gntl-from-source)
    - [Build Process](#build-process)
      - [Install the Dependencies](#install-the-dependencies)
      - [Start the Build](#start-the-build)
        - [Running the Built Executables](#running-the-built-executables)
    - [Cross Compiling](#cross-compiling)
  - [Internationalization](#internationalization)
  - [Using Tor](#using-tor)
    - [Tails](#tails)
  - [Debugging](#debugging)
    - [Obtaining stack traces and core dumps on Unix systems](#obtaining-stack-traces-and-core-dumps-on-unix-systems)
    - [Analysing memory corruption](#analysing-memory-corruption)
    - [LMDB](#lmdb)

## Specifications

- Name: GNTL Coin
- Ticker: GNTL
- Max supply: 77.7 ml
- Pre-mine: 0.000000030 (all burnt)
- Governance Fee: 10% for 4 months (height < 87,000), 5% for a further 8 months (height < 260,000), and then 1% thereafter (height > 260,000)
- Block time: 120 seconds
- Decimals: 9
- Algorithm: RandomARQ
- Consensus: PoW
- Anonymity: BulletProof RingCT

## Resources

- Coin: [gntl.cash](https://gntl.cash)
- Project: [gntl.uk](https://gntl.uk)
- Explorer (Primary): [explorer.gntl.cash](https://explorer.gntl.cash)
- Explorer (Backup): [explorer.gntl.uk](https://explorer.gntl.uk)
- Mining Pools: [https://miningpoolstats.stream/gntlcoin](https://miningpoolstats.stream/gntlcoin)
- E-Mail (Coin): [support@gntl.cash](mailto:support@gntl.cash)
- E-Mail (Project): [support@gntl.uk](mailto:support@gntl.uk)
- Discord: [https://discord.gntl.uk](https://discord.gntl.uk)
- Telegram: [https://t.me/GNTLCoin](https://t.me/GNTLCoin)
- Wiki: [https://github.com/The-GNTL-Project/Documentation/wiki/](https://github.com/The-GNTL-Project/Documentation/wiki/)
- Exchanges:
  - Exbitron: [https://app.exbitron.com/](https://app.exbitron.com/)
  - CEXSwap: [https://cexswap.cc/](https://cesswap.cc/)
  - BITGoGet: [https://bitgoget.com/](https://bitgoget.com/)
- Mainnet Nodes: [https://mainnet.gntl.uk/](https://mainnet.gntl.uk/)
- Stagenet Nodes: [https://stagenet.gntl.uk/](https://stagenet.gntl.uk/)
- Nodes Uptime Monitor: [https://stats.uptimerobot.com/wNWOvs003Y](https://stats.uptimerobot.com/wNWOvs003Y)

## Introduction

GNTL is a private, secure, untraceable, decentralised digital currency. You are your bank, you control your funds, and nobody can trace your transfers unless you allow them to do so.

**Privacy:** GNTL uses a cryptographically sound system to allow you to send and receive funds without your transactions being easily revealed on the blockchain (the ledger of transactions that everyone has). This ensures that your purchases, receipts, and all transfers remain absolutely private by default.

**Security:** Using the power of a distributed peer-to-peer consensus network, every transaction on the network is cryptographically secured. Individual wallets have a 25 word mnemonic seed that is only displayed once, and can be written down to backup the wallet. Wallet files are encrypted with a passphrase to ensure they are useless if stolen.

**Untraceability:** By taking advantage of ring signatures, a special property of a certain type of cryptography, GNTL is able to ensure that transactions are not only untraceable, but have an optional measure of ambiguity that ensures that transactions cannot easily be tied back to an individual user or computer.

## SSL

As a network, GNTL supports complete, cryptographically secured connections at all levels. This includes, but is not limited to The GNTL Project Nodes (Full nodes), Remote Nodes and all wallets.    

The GNTL Project will be consistently implementing the highest security protocols to achieve the greatest privacy for all transactions, as well as all communications made over The GNTL Project.

The use of SSL connections means that there will not be any possibility to use The GNTL Project with unsecured or tampered connections (daemons), and that your privacy will remain a feature built in a protocol level.

 * Below is an example how to generate SSL Keys with openssl.  This example will generate 4096bit SSL Cert at /tmp (which can be changed)

```
openssl genrsa -out /tmp/KEY 4096
openssl req -new -key /tmp/KEY -out /tmp/REQ
openssl x509 -req -days 999999 -sha256 -in /tmp/REQ -signkey /tmp/KEY -out /tmp/CERT
```

## About this project

This is the core implementation of GNTL. It is open source and completely free to use without restrictions, except for those specified in the license agreement below. There are no restrictions on anyone creating an alternative implementation of GNTL that uses the protocol and network in a compatible manner.

As with many development projects, the repository on Github is considered to be the "staging" area for the latest changes. Before changes are merged into that branch on the main repository, they are tested by individual developers in their own branches, submitted as a pull request, and then subsequently tested by contributors who focus on testing and code reviews. That having been said, the repository should be carefully considered before using it in a production environment, unless there is a patch in the repository for a particular show-stopping issue you are experiencing. It is generally a better idea to use a tagged release for stability.

**Anyone is welcome to contribute to GNTL's codebase!** If you have a fix or code change, feel free to submit it as a pull request directly to the "master" branch. In cases where the change is relatively small or does not affect other parts of the codebase it may be merged in immediately by any one of the collaborators. On the other hand, if the change is particularly large or complex, it is expected that it will be discussed at length either well in advance of the pull request being submitted, or even directly on the pull request.

## Supporting the project

GNTL is a 100% community developed.  If you would like to donate to our cause, please do so via the following donation addresses:

GNTL Wallet: `gnt1ibrAtYtThQWQ8QdeLPWGD9ZeqnDsJ9A4d86DMC2RD7frBSE1uZmFezsbW7TXHdNHYWDWsccRo8TpE55p2HWR74ofajRWc5`

GNTL Viewkey: `d0abbf9c47bdf8189676eed67bfb31a2ef16ef276a8077877a987bff9fcb8203`

## License

See [LICENSE](LICENSE).

## Contributing

If you want to help out, see [CONTRIBUTING](CONTRIBUTING.md) for a set of guidelines.

## Compiling GNTL from source
**Our build has been tested on Debian 11 and Ubuntu Server 20.04.  Other versions of OS should work, but are out of scope in this guide**

### Build Process
**IMPORTANT**

The master branch is used for active development and can be either unstable or incompatible with release software. Please compile release branches instead.

[![TravisCI master branch](https://img.shields.io/travis/gntl/gntl/master?label=master%20branch&style=for-the-badge)](https://travis-ci.org/gntl/gntl)
![Monitored by DiscordHooks](https://img.shields.io/static/v1?label=Monitored%20by&message=DiscordHooks&color=brightgreen&style=for-the-badge)

**Tools and Libraries Used**

The following table summarizes the tools and libraries required to build. A few of the libraries are also included in this repository (marked as "Vendored"). By default, the build uses the library installed on the system, and ignores the vendored sources. However, if no library is found installed on the system, then the vendored source will be built and used. The vendored sources are also used for statically-linked builds because distribution packages often include only shared library binaries (`.so`) but not static library archives (`.a`).

| Dep          | Min. version  | Vendored | Debian/Ubuntu pkg  | Arch pkg     | Fedora            | Optional | Purpose        |
| ------------ | ------------- | -------- | ------------------ | ------------ | ----------------- | -------- | -------------- |
| autoconf     | 2.69          | NO       | `autoconf`         | ?            | ?                 | NO       |                |
| automake     | 1.16          | NO       | `automake`         | ?            | ?                 | NO       |                |
| Boost        | 1.73          | NO       | `libboost-all-dev` | `boost`      | `boost-devel`     | NO       | C++ libraries  |
| CMake        | 3.17.3        | NO       | `cmake`            | `cmake`      | `cmake`           | NO       |                |
| Doxygen      | 1.8.17        | NO       | `doxygen`          | `doxygen`    | `doxygen`         | YES      | Documentation  |
| expat        | 2.2.9         | NO       | `libexpat1-dev`    | `expat`      | `expat-devel`     | YES      | XML parsing    |
| GCC          | 9.3.0         | NO       | `gcc-9 g++-9`      | ?            | ?                 | NO       |                |
| gperf        | 3.1           | NO       | `gperf`            | ?            | ?                 | NO       |                |
| Graphviz     | 2.42.2        | NO       | `graphviz`         | `graphviz`   | `graphviz`        | YES      | Documentation  |
| GTest        | 1.10.0        | YES      | `libgtest-dev`     | `gtest`      | `gtest-devel`     | YES      | Test suite     |
| HIDAPI       | 0.9.0         | NO       | `libhidapi-dev`    | ?            | ?                 | NO       | for Device     |
| miniupnpc    | 2.1.20190824  | NO       | `miniupnpc`        | ?            | ?                 | NO       |                |
| ldns         | 1.7.0         | NO       | `libldns-dev`      | `ldns`       | `ldns-devel`      | YES      | SSL toolkit    |
| libevent     | 2.1.11        | NO       | `libevent-dev`     | ?            | ?                 | NO       |                |
| liblzma      | 5.2.4         | NO       | `liblzma-dev`      | `xz`         | `xz-devel`        | YES      | For libunwind  |
| libreadline  | 8.0           | NO       | `libreadline-dev`  | `readline`   | `readline-devel`  | YES      | Input editing  |
| libsodium    | 1.0.18        | NO       | `libsodium-dev`    | ?            | `libsodium-devel` | NO       | Cryptography   |
| libtool      | 2.4.6         | NO       | `libtool-bin`      | ?            | ?                 | NO       |                |
| libudev      | 245.4         | NO       | `libudev-dev`      | ?            | ?                 | NO       |                |
| libunbound   | 1.9.4         | NO       | `libunbound-dev`   | ?            | ?                 | NO       |                |
| libunwind    | 1.2.1         | NO       | `libunwind-dev`    | `libunwind`  | `libunwind-devel` | YES      | Stack traces   |
| libusb-1.0   | 1.0.23        | NO       | `libusb-1.0-0-dev` | ?            | ?                 | NO       |                |
| libzmq5      | 4.3.2         | NO       | `libzmq5-dev`      | ?            | ?                 | NO       |                |
| OpenSSL      | 1.1.1         | NO       | `libssl-dev`       | `openssl`    | `openssl-devel`   | NO       | sha256 sum     |
| pkg-config   | 0.29.1        | NO       | `pkg-config`       | `base-devel` | `pkgconf`         | NO       |                |
| xsltproc     | 1.1.34        | NO       | `xsltproc`         | ?            | ?                 | NO       |                |

-------------------------------------------------------------------------------------------------------------------------------

### Install the Dependencies 

#### Debian / Ubuntu dependancies

##### Install Cmake v3.17.3
```
wget https://github.com/Kitware/CMake/releases/download/v3.17.3/cmake-3.17.3-Linux-x86_64.sh
sudo mv cmake-3.17.3-Linux-x86_64.sh /opt
cd /opt
sudo chmod +x cmake-3.17.3-Linux-x86_64.sh
sudo bash ./cmake-3.17.3-Linux-x86_64.sh
sudo rm cmake-3.17.3-Linux-x86_64.sh
sudo ln -s /opt/cmake-3.17.3-Linux-x86_64/bin/* /usr/local/bin
cd ~
```

##### Install GCC 9.3
```
sudo apt update -y
sudo apt install gcc-9 g++-9 -y
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-9 90 --slave /usr/bin/g++ g++ /usr/bin/g++-9 --slave /usr/bin/gcov gcov /usr/bin/gcov-9
```

##### Install Boost 1.73.0
```
sudo apt remove libboost* -y
sudo apt autoremove -y
wget https://downloads.sourceforge.net/project/boost/boost/1.73.0/boost_1_73_0.tar.gz
tar xzvf boost_1_73_0.tar.gz
rm boost_1_73_0.tar.gz
sudo mv boost_1_73_0 /opt/boost_1_73_0
cd /opt/boost_1_73_0
./bootstrap.sh --prefix=/opt/boost_1_73_0
./b2 install
export BOOST_ROOT=/opt/boost_1_73_0
cd ~
```

##### Install All other Dependencies
```
sudo apt update && sudo apt install -y git autoconf automake build-essential curl doxygen libexpat1-dev gperf graphviz libhidapi-dev miniupnpc libldns-dev libevent-dev liblzma-dev libreadline-dev libsodium-dev libtool-bin libudev-dev libunbound-dev libunwind-dev libusb-1.0-0-dev libssl-dev libzmq5-dev pkg-config xsltproc
```

##### Install libgtest-dev
`libgtest-dev` only includes sources and headers.  You must build the library binary manually.  This can be done with the following command:

```
sudo apt install -y libgtest-dev && cd /usr/src/gtest && sudo cmake . && sudo make
sudo mv lib/libg* /usr/lib/
cd ~
```

#### OSX dependancies
```
brew update && brew bundle --file=contrib/apple/brew
```

### Start the Build
GNTL uses the CMake build system and a top-level [Makefile](Makefile) that invokes cmake commands as needed.

**NOTE**: We will use the **v1.0.6** branch as an example, you should switch to the most recent released branch.

#### Clone the Repository recursively to pull-in needed submodule(s)
```
git clone --recursive https://github.com/The-GNTL-Project/gntl
```

##### If you already have a repo cloned, initialize and update:
```
cd gntl && git checkout v1.0.6
git submodule init && git submodule update
```

#### Debian / Ubuntu / OS X
* Change to the root of the source code directory, switch branch, and build:

**NOTE**: If your machine has several cores and enough memory, enable parallel build by running `make -j<number of threads>` instead of `make` below.  For this to be worthwhile, the machine should have one core and about 2GB of RAM available per thread.

```
cd gntl
git checkout v1.0.6
USE_SINGLE_BUILDDIR=1 make release
cd ~
```

##### Running the Built Executables
The resulting executables can be found in: `build/release/bin`

Add `PATH="$PATH:$HOME/gntl/build/release/bin"` to `.profile`

Run `. ~/.profile` to reload profile changes.

Run GNTL Daemon using `gntld --detach`

Other executables, such as `gntl-wallet-cli` are also available in `build/release/bin`

#### Raspberry Pi Zero
Tested on a Raspberry Pi Zero with a clean install of minimal Raspbian Stretch (2017-09-07 or later) from https://www.raspberrypi.org/downloads/raspbian/. If you are using Raspian Jessie, [please see note in the following section](#note-for-raspbian-jessie-users).

* `apt-get update && apt-get upgrade` to install all of the latest software

* Install the dependencies for GNTL from the 'Debian' column in the table above.

* Increase the system swap size:

```
sudo /etc/init.d/dphys-swapfile stop
sudo nano /etc/dphys-swapfile
CONF_SWAPSIZE=1024
sudo /etc/init.d/dphys-swapfile start
```

* Clone gntl and checkout most recent release version:
```
git clone https://github.com/The-GNTL-Project/gntl.git
cd gntl
```

* Build:

```
make release
```

* Wait a while, depending on you system specifications.

* The resulting executables can be found in `build/release/bin`

* Add `PATH="$PATH:$HOME/gntl/build/release/bin"` to `.profile`

* Run GNTL with `gntld --detach`

* You may wish to reduce the size of the swap file after the build has finished, and delete the boost directory from your home directory

#### Raspbian Jessie

If you are using the older Raspbian Jessie image, compiling GNTL is a bit more complicated. The version of Boost available in the Debian Jessie repositories is too old to use with GNTL, and thus you must compile a newer version yourself. The following explains the extra steps, and has been tested on a Raspberry Pi 2 with a clean install of minimal Raspbian Jessie.

* As before, `apt-get update && apt-get upgrade` to install all of the latest software, and increase the system swap size

```
sudo /etc/init.d/dphys-swapfile stop
sudo nano /etc/dphys-swapfile
CONF_SWAPSIZE=1024
sudo /etc/init.d/dphys-swapfile start
```

* Then, install the dependencies for GNTL except `libunwind` and `libboost-all-dev`

* Install the latest version of boost (this may first require invoking `apt-get remove --purge libboost*` to remove a previous version if you're not using a clean install):

```
cd
wget https://sourceforge.net/projects/boost/files/boost/1.68.0/boost_1_68_0.tar.bz2
tar xvfo boost_1_68_0.tar.bz2
cd boost_1_68_0
./bootstrap.sh
sudo ./b2
```
* Wait a while, depending on you system specifications.

```
sudo ./bjam install
```

* Wait a while, depending on you system specifications.

* From here, follow the [general Raspberry Pi instructions](#on-the-raspberry-pi) from the "Clone gntl and checkout most recent release version" step.

#### Raspberry Pi 2b and Pi 400

Tested on Raspberry Pi 2b and Pi 400 using official OS raspbian buster armhf (32bit). This should work on all pi3's and pi4's including compute modules untested though but pretty sure it will work.

This will not work on pi64 os or by adding arm_64bit in config.txt in boot at present working progress.

First we need to update glibc as the current raspbian system only has 2.28 while min 2.29 is needed. This will not update the whole system as this will run the gntl wallet in closed system as it could cause issues with raspiban os and related software etc.

* Instructions for glibc
(change -j4 to appropriate number related to your thread count)
```
sudo apt install gawk bison -y
wget http://ftp.gnu.org/gnu/glibc/glibc-2.33.tar.gz
tar -xf glibc-2.33.tar.gz
rm -r glibc-2.33.tar.gz
cd glibc-2.33
mkdir build
cd build
../configure --prefix=$home
make -j4
```

* Wait a while, depending on you system specifications.

* wallet instructions
Please make sure you get the armv7 version at present the armv8 wont work on 64bit os or arm_64bit in config.txt in boot

(We will renames file for easy typing later on)
```
cd ~
wget https://gntl.cash/downloads/GNTL-ARM-v7-v1.0.6.tar.gz
tar -xf GNTL-ARM-v7-v1.0.6.tar.gz
rm GNTL-ARM-v7-v1.0.6.tar.gz
```

* To run the wallet you need to run it in the glibc container we just built.
(please make sure data-dir is not on a small sd card)
```
cd glibc-2.33/build
sudo ./testrun.sh ~/gntl/gntld --data-dir /gntl
```

* First time update blockchain will take a while depending on what storage your using. Please wait till this complete syncs up before you carry on to wallet.

* Open another command prompt while leaving the above

```
sudo ./testrun.sh ~/gntl/gntl-wallet-cli
```

#### Windows 10:
Binaries for Windows are built on Windows using the MinGW toolchain within [MSYS2 environment](http://msys2.github.io). The MSYS2 environment emulates a
POSIX system. The toolchain runs within the environment and *cross-compiles* binaries that can run outside of the environment as a regular Windows application.

**Preparing the build environment**

1. Download and install the [MSYS2 installer](http://msys2.github.io).

2. Open the MSYS shell via the `MSYS2 MSYS` shortcut at Menu Start

3. Update packages using pacman:

```
pacman -Syu
```

4. Exit the MSYS shell using Alt+F4 or by clicking X at top-right corner. It is Very Important to do not exit to shell!!.

5. Start `MSYS2 MINGW64` from Menu Start

6. Update packages again using pacman:

```
pacman -Syu
```

7. Install dependencies:

    To build for 64-bit Windows:

```
pacman -S git mingw-w64-x86_64-toolchain make mingw-w64-x86_64-cmake mingw-w64-x86_64-boost mingw-w64-x86_64-openssl mingw-w64-x86_64-libsodium mingw-w64-x86_64-hidapi automake autoconf binutils patch
```

**Building**

* Download GNTL with command:

```
git clone https://github.com/The-GNTL-Project/gntl
```

* Change branch to last Release:

```
cd gntl && git checkout <branch or release>
```

* Activate and update submodules:

```
git submodule init && git submodule update
```

* If you are on a 64-bit system, run:

```
USE_SINGLE_BUILDDIR=1 make release-static-win
```

* The resulting executables can be found in `build/release/bin`

* **Optional**: to build Windows binaries suitable for debugging on a 64-bit system, run:

```
make debug-static-win
```

* The resulting executables can be found in `build/debug/bin`

*** GNTL does Not support 32-bit Windows anymore ***

#### Linux for Android (using docker):

##### Build image
```
docker build -f utils/build_scripts/android32.Dockerfile -t gntl-android .
```
##### Create container
```
docker create -it --name gntl-android gntl-android bash
```
##### Get binaries
```
docker cp gntl-android:/opt/android/gntl/build/release/bin .
```
#### Running gntld

The build places the binary in `bin/` sub-directory within the build directory
from which cmake was invoked (repository root by default). To run in
foreground:

```
./bin/gntld
```

To list all available options, run `./bin/gntld --help`.  Options can be
specified either on the command line or in a configuration file passed by the
`--config-file` argument.  To specify an option in the configuration file, add
a line with the syntax `argumentname=value`, where `argumentname` is the name
of the argument without the leading dashes, for example `log-level=1`.

To run in background:

```
./bin/gntld --log-file gntld.log --detach
```

To run as a systemd service, copy
[gntld.service](utils/systemd/gntld.service) to `/etc/systemd/system/` and
[gntld.conf](utils/conf/gntld.conf) to `/etc/`. The [example
service](utils/systemd/gntld.service) assumes that the user `gntl` exists
and its home is the data directory specified in the [example
config](utils/conf/gntld.conf).

If you're on Mac, you may need to add the `--max-concurrency 1` option to
gntl-wallet-cli, and possibly gntld, if you get crashes refreshing.

### Cross Compiling
You can also cross-compile GNTL static binaries on Linux for Windows and macOS with the `depends` system.

* `make depends target=x86_64-linux-gnu` for 64-bit linux binaries.
* `make depends target=x86_64-w64-mingw32` for 64-bit windows binaries. Requires: python3 g++-mingw-w64-x86-64 wine1.6 bc
* `make depends target=x86_64-apple-darwin19.2.0` for macOS binaries. Requires: cmake imagemagick libcap-dev librsvg2-bin libz-dev libbz2-dev libtiff-tools curl bsdmainutils python3-setuptools
* `make depends target=arm-linux-gnueabihf` for armv7 binaries. Requires: g++-arm-linux-gnueabihf
* `make depends target=aarch64-linux-gnu` for armv8 binaries. Requires: g++-aarch64-linux-gnu

*** For `x86_64-apple-darwin19.2.0` you need to download SDK first ***        

The required packages are the names for each toolchain on apt. Depending on your OS Distribution, they may have different names.

Using `depends` might also be easier to compile GNTL on Windows than using MSYS. Activate Windows Subsystem for Linux (WSL) with a distribution (for example Ubuntu), install the apt build-essentials and follow the `depends` steps as stated above.

## Internationalization

See [README.i18n.md](README.i18n.md).

## Using Tor

> There is a new, still experimental, [integration with Tor](ANONYMITY_NETWORKS.md). The
> feature allows connecting over IPv4 and Tor simultaneously - IPv4 is used for
> relaying blocks and relaying transactions received by peers whereas Tor is
> used solely for relaying transactions received over local RPC. This provides
> privacy and better protection against surrounding node (sybil) attacks.

While GNTL isn't made to integrate with Tor, it can be used wrapped with torsocks, by
setting the following configuration parameters and environment variables:

* `--p2p-bind-ip 127.0.0.1` on the command line or `p2p-bind-ip=127.0.0.1` in
  gntld.conf to disable listening for connections on external interfaces.
* `--no-igd` on the command line or `no-igd=1` in gntld.conf to disable IGD
  (UPnP port forwarding negotiation), which is pointless with Tor.
* `DNS_PUBLIC=tcp` or `DNS_PUBLIC=tcp://x.x.x.x` where x.x.x.x is the IP of the
  desired DNS server, for DNS requests to go over TCP, so that they are routed
  through Tor. When IP is not specified, gntld uses the default list of
  servers defined in [src/common/dns_utils.cpp](src/common/dns_utils.cpp).
* `TORSOCKS_ALLOW_INBOUND=1` to tell torsocks to allow gntld to bind to interfaces
   to accept connections from the wallet. On some Linux systems, torsocks
   allows binding to localhost by default, so setting this variable is only
   necessary to allow binding to local LAN/VPN interfaces to allow wallets to
   connect from remote hosts. On other systems, it may be needed for local wallets
   as well.
* Do NOT pass `--detach` when running through torsocks with systemd, (see
  [utils/systemd/gntld.service](utils/systemd/gntld.service) for details).
* If you use the wallet with a Tor daemon via the loopback IP (eg, 127.0.0.1:9050),
  then use `--untrusted-daemon` unless it is your own hidden service.

Example command line to start gntld through Tor:

```
DNS_PUBLIC=tcp torsocks gntld --p2p-bind-ip 127.0.0.1 --no-igd
```

### Tails

TAILS ships with a very restrictive set of firewall rules. Therefore, you need
to add a rule to allow this connection too, in addition to telling torsocks to
allow inbound connections. Full example:

```
sudo iptables -I OUTPUT 2 -p tcp -d 127.0.0.1 -m tcp --dport 16662 -j ACCEPT
DNS_PUBLIC=tcp torsocks ./gntld --p2p-bind-ip 127.0.0.1 --no-igd --rpc-bind-ip 127.0.0.1 \
        --data-dir /home/amnesia/Persistent/your/directory/to/the/blockchain
```

## Debugging

This section contains general instructions for debugging failed installs or problems encountered with GNTL. First ensure you are running the latest version built from the Github repository.

### Obtaining stack traces and core dumps on Unix systems

We generally use the tool `gdb` (GNU debugger) to provide stack trace functionality, and `ulimit` to provide core dumps in builds which crash or segfault.

* To use gdb in order to obtain a stack trace for a build that has stalled:

Run the build.

Once it stalls, enter the following command:

```
gdb /path/to/gntld `pidof gntld`
```

Type `thread apply all bt` within gdb in order to obtain the stack trace

* If however the core dumps or segfaults:

Enter `ulimit -c unlimited` on the command line to enable unlimited filesizes for core dumps

Enter `echo core | sudo tee /proc/sys/kernel/core_pattern` to stop cores from being hijacked by other tools

Run the build.

When it terminates with an output along the lines of "Segmentation fault (core dumped)", there should be a core dump file in the same directory as gntld. It may be named just `core`, or `core.xxxx` with numbers appended.

You can now analyse this core dump with `gdb` as follows:

```
gdb /path/to/gntld /path/to/dumpfile
```

Print the stack trace with `bt`

* To run gntl within gdb:

Type `gdb /path/to/gntld`

Pass command-line options with `--args` followed by the relevant arguments

Type `run` to run gntld

### Analysing memory corruption

We use the tool `valgrind` for this.

Run with `valgrind /path/to/gntld`. It will be slow.

### LMDB

Instructions for debugging suspected blockchain corruption as per @HYC

There is an `mdb_stat` command in the LMDB source that can print statistics about the database but it's not routinely built. This can be built with the following command:

```
cd ~/gntl/external/liblmdb && make
```

The output of `mdb_stat -ea <path to blockchain dir>` will indicate inconsistencies in the blocks, block_heights and block_info table.

The output of `mdb_dump -s blocks <path to blockchain dir>` and `mdb_dump -s block_info <path to blockchain dir>` is useful for indicating whether blocks and block_info contain the same keys.

These records are dumped as hex data, where the first line is the key and the second line is the data.
