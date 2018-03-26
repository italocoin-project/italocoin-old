# Italocoin
Copyright (c) 2018, ItaloCoin And The Monero Project Portions Copyright (c) 2012-2013, The Cryptonote developers
## Development Resources
- Web: [italocoin.com](https://italocoin.com) - Forum: [forum.italocoin.com](https://forum.italocoin.com) - Mail: [dev@italocoin.com](mailto:dev@italocoin.com) 
- GitHub: [https://github.com/italocoin-project/italocoin](https://github.com/italocoin-project/italocoin) - IRC: [#italocoin-dev on 
Freenode](http://webchat.freenode.net/?randomnick=1&channels=%23italocoin-dev&prompt=1&uio=d4) - Discord: [#italocoin On Discord](https://discord.gg/thUzmtm)
## Introduction
Italocoin is a private, secure, untraceable, decentralised digital currency. You are your bank, you control your funds, and nobody can trace your transfers 
unless you allow them to do so. **Privacy:** Italocoin uses a cryptographically sound system to allow you to send and receive funds without your transactions 
being easily revealed on the blockchain (the ledger of transactions that everyone has). This ensures that your purchases, receipts, and all transfers remain 
absolutely private by default. **Security:** Using the power of a distributed peer-to-peer consensus network, every transaction on the network is 
cryptographically secured. Individual wallets have a 25 word mnemonic seed that is only displayed once, and can be written down to backup the wallet. Wallet 
files are encrypted with a passphrase to ensure they are useless if stolen. **Untraceability:** By taking advantage of ring signatures, a special property of a 
certain type of cryptography, Italocoin is able to ensure that transactions are not only untraceable, but have an optional measure of ambiguity that ensures 
that transactions cannot easily be tied back to an individual user or computer.
## About this Project
This is the core implementation of Italocoin. It is open source and completely free to use without restrictions, except for those specified in the license 
agreement below. There are no restrictions on anyone creating an alternative implementation of Italocoin that uses the protocol and network in a compatible 
manner. As with many development projects, the repository on Github is considered to be the "staging" area for the latest changes. Before changes are merged 
into that branch on the main repository, they are tested by individual developers in their own branches, submitted as a pull request, and then subsequently 
tested by contributors who focus on testing and code reviews. That having been said, the repository should be carefully considered before using it in a 
production environment, unless there is a patch in the repository for a particular show-stopping issue you are experiencing. It is generally a better idea to 
use a tagged release for stability. **Anyone is welcome to contribute to Italocoin's codebase!** If you have a fix or code change, feel free to submit it as a 
pull request directly to the "master" branch. In cases where the change is relatively small or does not affect other parts of the codebase it may be merged in 
immediately by any one of the collaborators. On the other hand, if the change is particularly large or complex, it is expected that it will be discussed at 
length either well in advance of the pull request being submitted, or even directly on the pull request.
## Supporting the Project
Italocoin development can be supported directly through donations. Both Italocoin and Bitcoin donations can be made to donate.italocoin.com if using a client 
that supports the [OpenAlias](https://openalias.org) standard
## DONATE
- BTC: 1FgYSKX6hqoxpCba91bigBr7xy9A3e5H1C - ITC: ipPQjQYEQsLL7Gv43PpHDLiFLsZzoGuZtEJ8ZCW2is5TGeMNPo66bTKXAAd3m3ceXp4aweqmZnAHt9bWHALkK7xR2MVhF8QFZ - Monero: 
44gNsFFqMf59DiVL3ejpfAdV3H3aFbbYM28XtvBK22SQVESBLpxRrQcFCky2yVH8Wa3FpiBbiNRJ5SQfdsVwJqYpA7XLyec Core development funding and/or some supporting services are 
also graciously provided by sponsors: There are also several mining pools that kindly donate a portion of their fees, [a list of them can be found on our 
Bitcointalk post](https://www.italocoin.com).
## License
See [LICENSE](LICENSE).
# Contributing
If you want to help out, see [CONTRIBUTING](CONTRIBUTING.md) for a set of guidelines.
## Italocoin software updates and Network Consensus Protocol Upgrade (hard fork schedule)
Italocoin uses a fixed-schedule network consensus protocol upgrade (hard fork) mechanism to implement new features. This means that users of Italocoin (end 
users and service providers) need to run current versions and upgrade their software on a regular schedule. Network consensus protocol upgrades occur during the 
months of March and September. Required software for these consensus protocol upgrades is available prior to the date of the consensus protocol upgrade. Please 
check the git repository prior to this date for the proper Italocoin software version. Below is the historical schedule and the projected schedule for the next 
upgrade. Dates are provided in the format YYYY-MM-DD.
| Consensus Upgrade Block Height | Date | Consensus version | Minimum Italocoin Version | Recommended Italocoin Version | Details | 
| ------------------------------ | -----------| ----------------- | ---------------------- | -------------------------- | 
| ---------------------------------------------------------------------------------- | 1009827 | 2016-03-22 | v2 | v0.9.4 | v0.9.4 | Allow only >= ringsize 3, 
| blocktime = 120 seconds, fee-free blocksize 60 kb | 1141317 | 2016-09-21 | v3 | v0.9.4 | v0.10.0 | Splits coinbase into denominations | 1220516 | 2017-01-05 | 
| v4 | v0.10.1 | v0.10.2.1 | Allow normal and RingCT transactions | 1288616 | 2017-04-15 | v5 | v0.10.3.0 | v0.10.3.1 | Adjusted minimum blocksize and fee 
| algorithm | 1400000 | 2017-09-16 | v6 | v0.11.0.0 | v0.11.0.0 | Allow only RingCT transactions, allow only >= ringsize 5 | XXXXXXX | 2018-03-XX | XX | 
| XXXXXXXXX | XXXXXXXXX | XXXXXX
X's indicate that these details have not been determined as of commit date, 2017-09-20.
## Installing Italocoin from a Package
Packages are available for * Ubuntu and [snap supported](https://snapcraft.io/docs/core/install) systems, via a community contributed build.
    snap install italocoin --beta Installing a snap is very quick. Snaps are secure. They are isolated with all of their dependencies. Snaps also auto update 
when a new version is released. * Arch Linux (via [AUR](https://aur.archlinux.org/)):
  - Stable release: [`italocoin`](https://aur.archlinux.org/packages/italocoin)
  - Bleeding edge: [`italocoin-git`](https://aur.archlinux.org/packages/italocoin-git) * Void Linux:
    xbps-install -S italocoin * OS X via [Homebrew](http://brew.sh)
        brew tap sammy007/cryptonight
        brew install italocoin --build-from-source * Docker
        docker build -t italocoin .
     
        # either run in foreground
        docker run -it -v /italocoin/chain:/root/.italocoin -v /italocoin/wallet:/wallet -p 13101:13101 italocoin
        # or in background
        docker run -it -d -v /italocoin/chain:/root/.italocoin -v /italocoin/wallet:/wallet -p 13101:13101 italocoin Packaging for your favorite distribution 
would be a welcome contribution!
## Compiling Italocoin from Source
### Dependencies
The following table summarizes the tools and libraries required to build.  A few of the libraries are also included in this repository (marked as "Vendored"). 
By default, the build uses the library installed on the system, and ignores the vendored sources. However, if no library is found installed on the system, then 
the vendored source will be built and used. The vendored sources are also used for statically-linked builds because distribution packages often include only 
shared library binaries (`.so`) but not static library archives (`.a`).
| Dep | Min. Version | Vendored | Debian/Ubuntu Pkg | Arch Pkg | Optional | Purpose | -------------- | ------------- | ---------| ------------------ | 
| -------------- | -------- | -------------- | GCC | 4.7.3 | NO | `build-essential` | `base-devel` | NO | | CMake | 3.0.0 | NO | `cmake` | `cmake` | NO | | 
| pkg-config | any | NO | `pkg-config` | `base-devel` | NO | | Boost | 1.58 | NO | `libboost-all-dev` | `boost` | NO | C++ libraries | OpenSSL | basically any | 
| NO | `libssl-dev` | `openssl` | NO | sha256 sum | libzmq | 3.0.0 | NO | `libzmq3-dev` | `zeromq` | NO | ZeroMQ library | libunbound | 1.4.16 | YES | 
| `libunbound-dev` | `unbound` | NO | DNS resolver | libminiupnpc | 2.0 | YES | `libminiupnpc-dev` | `miniupnpc` | YES | NAT punching | libunwind | any | NO | 
| `libunwind8-dev` | `libunwind` | YES | Stack traces | liblzma | any | NO | `liblzma-dev` | `xz` | YES | For libunwind | libreadline | 6.3.0 | NO | 
| `libreadline6-dev` | `readline` | YES | Input editing | ldns | 1.6.17 | NO | `libldns-dev` | `ldns` | YES | SSL toolkit | expat | 1.1 | NO | `libexpat1-dev` | 
| `expat` | YES | XML parsing | GTest | 1.5 | YES | `libgtest-dev`^ | `gtest` | YES | Test suite | Doxygen | any | NO | `doxygen` | `doxygen` | YES | 
| Documentation | Graphviz | any | NO | `graphviz` | `graphviz` | YES | Documentation |
[^] On Debian/Ubuntu `libgtest-dev` only includes sources and headers. You must build the library binary manually. This can be done with the following command 
```sudo apt-get install libgtest-dev && cd /usr/src/gtest && sudo cmake . && sudo make && sudo mv libg* /usr/lib/ ```
### Build instructions
Italocoin uses the CMake build system and a top-level [Makefile](Makefile) that invokes cmake commands as needed.
#### On Linux and OS X
* Install the dependencies * Change to the root of the source code directory and build:
        cd italocoin
        make
    *Optional*: If your machine has several cores and enough memory, enable
    parallel build by running `make -j<number of threads>` instead of `make`. For
    this to be worthwhile, the machine should have one core and about 2GB of RAM
    available per thread.
    *Note*: If cmake can not find zmq.hpp file on OS X, installing `zmq.hpp` from
    https://github.com/zeromq/cppzmq to `/usr/local/include` should fix that error. * The resulting executables can be found in `build/release/bin` * Add 
`PATH="$PATH:$HOME/italocoin/build/release/bin"` to `.profile` * Run Italocoin with `italocoind --detach` * **Optional**: build and run the test suite to verify 
the binaries:
        make release-test
    *NOTE*: `coretests` test may take a few hours to complete. * **Optional**: to build binaries suitable for debugging:
         make debug * **Optional**: to build statically-linked binaries:
         make release-static * **Optional**: build documentation in `doc/html` (omit `HAVE_DOT=YES` if `graphviz` is not installed):
        HAVE_DOT=YES doxygen Doxyfile
#### On the Raspberry Pi
Tested on a Raspberry Pi Zero with a clean install of minimal Raspbian Stretch (2017-09-07 or later) from https://www.raspberrypi.org/downloads/raspbian/. If 
you are using Raspian Jessie, [please see note in the following section](#note-for-raspbian-jessie-users). * `apt-get update && apt-get upgrade` to install all 
of the latest software * Install the dependencies for Italocoin from the 'Debian' column in the table above. * Increase the system swap size: ```
	sudo /etc/init.d/dphys-swapfile stop
	sudo nano /etc/dphys-swapfile
	CONF_SWAPSIZE=1024
	sudo /etc/init.d/dphys-swapfile start ``` * Clone italocoin and checkout most recent release version: ```
        git clone https://github.com/italocoin-project/italocoin.git
	cd italocoin
	git checkout tags/v0.11.0.0 ``` * Build: ```
        make release ``` * Wait 4-6 hours * The resulting executables can be found in `build/release/bin` * Add `PATH="$PATH:$HOME/italocoin/build/release/bin"` 
to `.profile` * Run Italocoin with `italocoind --detach` * You may wish to reduce the size of the swap file after the build has finished, and delete the boost 
directory from your home directory
#### *Note for Raspbian Jessie Users:*
If you are using the older Raspbian Jessie image, compiling Italocoin is a bit more complicated. The version of Boost available in the Debian Jessie 
repositories is too old to use with Italocoin, and thus you must compile a newer version yourself. The following explains the extra steps, and has been tested 
on a Raspberry Pi 2 with a clean install of minimal Raspbian Jessie. * As before, `apt-get update && apt-get upgrade` to install all of the latest software, and 
increase the system swap size ```
	sudo /etc/init.d/dphys-swapfile stop
	sudo nano /etc/dphys-swapfile
	CONF_SWAPSIZE=1024
	sudo /etc/init.d/dphys-swapfile start ``` * Then, install the dependencies for Italocoin except `libunwind` and `libboost-all-dev` * Install the latest 
version of boost (this may first require invoking `apt-get remove --purge libboost*` to remove a previous version if you're not using a clean install): ```
	cd
	wget https://sourceforge.net/projects/boost/files/boost/1.64.0/boost_1_64_0.tar.bz2
	tar xvfo boost_1_64_0.tar.bz2
	cd boost_1_64_0
	./bootstrap.sh
	sudo ./b2 ``` * Wait ~8 hours ```
	sudo ./bjam install ``` * Wait ~4 hours * From here, follow the [general Raspberry Pi instructions](#on-the-raspberry-pi) from the "Clone italocoin and 
checkout most recent release version" step.
#### On Windows:
Binaries for Windows are built on Windows using the MinGW toolchain within [MSYS2 environment](http://msys2.github.io). The MSYS2 environment emulates a POSIX 
system. The toolchain runs within the environment and *cross-compiles* binaries that can run outside of the environment as a regular Windows application. 
**Preparing the Build Environment** * Download and install the [MSYS2 installer](http://msys2.github.io), either the 64-bit or the 32-bit package, depending on 
your system. * Open the MSYS shell via the `MSYS2 Shell` shortcut * Update packages using pacman:
        pacman -Syuu * Exit the MSYS shell using Alt+F4 * Edit the properties for the `MSYS2 Shell` shortcut changing "msys2_shell.bat" to "msys2_shell.cmd 
-mingw64" for 64-bit builds or "msys2_shell.cmd -mingw32" for 32-bit builds * Restart MSYS shell via modified shortcut and update packages again using pacman:
        pacman -Syuu * Install dependencies:
    To build for 64-bit Windows:
        pacman -S mingw-w64-x86_64-toolchain make mingw-w64-x86_64-cmake mingw-w64-x86_64-boost mingw-w64-x86_64-openssl mingw-w64-x86_64-zeromq 
mingw-w64-x86_64-libsodium
    To build for 32-bit Windows:
 
        pacman -S mingw-w64-i686-toolchain make mingw-w64-i686-cmake mingw-w64-i686-boost mingw-w64-i686-openssl mingw-w64-i686-zeromq mingw-w64-i686-libsodium 
* Open the MingW shell via `MinGW-w64-Win64 Shell` shortcut on 64-bit Windows
  or `MinGW-w64-Win64 Shell` shortcut on 32-bit Windows. Note that if you are
  running 64-bit Windows, you will have both 64-bit and 32-bit MinGW shells. **Building** * If you are on a 64-bit system, run:
        make release-static-win64 * If you are on a 32-bit system, run:
        make release-static-win32 * The resulting executables can be found in `build/release/bin`
### On FreeBSD:
The project can be built from scratch by following instructions for Linux above. If you are running italocoin in a jail you need to add the flag: 
`allow.sysvipc=1` to your jail configuration, otherwise lmdb will throw the error message: `Failed to open lmdb environment: Function not implemented`. We 
expect to add Italocoin into the ports tree in the near future, which will aid in managing installations using ports or packages.
### On OpenBSD:
This has been tested on OpenBSD 5.8. You will need to add a few packages to your system. `pkg_add db cmake gcc gcc-libs g++ miniupnpc gtest`. The doxygen and 
graphviz packages are optional and require the xbase set. The Boost package has a bug that will prevent librpc.a from building correctly. In order to fix this, 
you will have to Build boost yourself from scratch. Follow the directions here (under "Building Boost"): 
https://github.com/bitcoin/bitcoin/blob/master/doc/build-openbsd.md You will have to add the serialization, date_time, and regex modules to Boost when building 
as they are needed by Italocoin. To build: `env CC=egcc CXX=eg++ CPP=ecpp DEVELOPER_LOCAL_TOOLS=1 BOOST_ROOT=/path/to/the/boost/you/built make 
release-static-64`
### On Linux for Android (using docker):
        # Build image (select android64.Dockerfile for aarch64)
        cd utils/build_scripts/ && docker build -f android32.Dockerfile -t italocoin-android .
        # Create container
        docker create -it --name italocoin-android italocoin-android bash
        # Get binaries
        docker cp italocoin-android:/opt/android/italocoin/build/release/bin .
### Building Portable Statically Linked Binaries
By default, in either dynamically or statically linked builds, binaries target the specific host processor on which the build happens and are not portable to 
other processors. Portable binaries can be built using the following targets: * ```make release-static-linux-x86_64``` builds binaries on Linux on x86_64 
portable across POSIX systems on x86_64 processors * ```make release-static-linux-i686``` builds binaries on Linux on x86_64 or i686 portable across POSIX 
systems on i686 processors * ```make release-static-linux-armv8``` builds binaries on Linux portable across POSIX systems on armv8 processors * ```make 
release-static-linux-armv7``` builds binaries on Linux portable across POSIX systems on armv7 processors * ```make release-static-linux-armv6``` builds binaries 
on Linux portable across POSIX systems on armv6 processors * ```make release-static-win64``` builds binaries on 64-bit Windows portable across 64-bit Windows 
systems * ```make release-static-win32``` builds binaries on 64-bit or 32-bit Windows portable across 32-bit Windows systems
## Running italocoind
The build places the binary in `bin/` sub-directory within the build directory from which cmake was invoked (repository root by default). To run in foreground:
    ./bin/italocoind To list all available options, run `./bin/italocoind --help`.  Options can be specified either on the command line or in a configuration 
file passed by the `--config-file` argument.  To specify an option in the configuration file, add a line with the syntax `argumentname=value`, where 
`argumentname` is the name of the argument without the leading dashes, for example `log-level=1`. To run in background:
    ./bin/italocoind --log-file italocoind.log --detach To run as a systemd service, copy [italocoind.service](utils/systemd/italocoind.service) to 
`/etc/systemd/system/` and [italocoind.conf](utils/conf/italocoind.conf) to `/etc/`. The [example service](utils/systemd/italocoind.service) assumes that the 
user `italocoin` exists and its home is the data directory specified in the [example config](utils/conf/italocoind.conf). If you're on Mac, you may need to add 
the `--max-concurrency 1` option to italocoin-wallet-cli, and possibly italocoind, if you get crashes refreshing.
## Internationalization
See [README.i18n.md](README.i18n.md).
## Using Tor
While Italocoin isn't made to integrate with Tor, it can be used wrapped with torsocks, if you add --p2p-bind-ip 127.0.0.1 to the italocoind command line. You 
also want to set DNS requests to go over TCP, so they'll be routed through Tor, by setting DNS_PUBLIC=tcp or use a particular DNS server with 
DNS_PUBLIC=tcp://a.b.c.d (default is 8.8.4.4, which is Google DNS). You may also disable IGD (UPnP port forwarding negotiation), which is pointless with Tor. To 
allow local connections from the wallet, you might have to add TORSOCKS_ALLOW_INBOUND=1, some OSes need it and some don't. Example: `DNS_PUBLIC=tcp torsocks 
italocoind --p2p-bind-ip 127.0.0.1 --no-igd` or: `DNS_PUBLIC=tcp TORSOCKS_ALLOW_INBOUND=1 torsocks italocoind --p2p-bind-ip 127.0.0.1 --no-igd` TAILS ships with 
a very restrictive set of firewall rules. Therefore, you need to add a rule to allow this connection too, in addition to telling torsocks to allow inbound 
connections. Full example: `sudo iptables -I OUTPUT 2 -p tcp -d 127.0.0.1 -m tcp --dport 13102 -j ACCEPT` `DNS_PUBLIC=tcp torsocks ./italocoind --p2p-bind-ip 
127.0.0.1 --no-igd --rpc-bind-ip 127.0.0.1 --data-dir /home/amnesia/Persistent/your/directory/to/the/blockchain` `./italocoin-wallet-cli`
# Debugging
This section contains general instructions for debugging failed installs or problems encountered with Italocoin. First ensure you are running the latest version 
built from the github repo.
## Obtaining Stack Traces and Core Dumps on Unix Systems
We generally use the tool `gdb` (GNU debugger) to provide stack trace functionality, and `ulimit` to provide core dumps in builds which crash or segfault. * To 
use gdb in order to obtain a stack trace for a build that has stalled: Run the build. Once it stalls, enter the following command: ``` gdb /path/to/italocoind 
`pidof italocoind` ``` Type `thread apply all bt` within gdb in order to obtain the stack trace * If however the core dumps or segfaults: Enter `ulimit -c 
unlimited` on the command line to enable unlimited filesizes for core dumps Enter `echo core | sudo tee /proc/sys/kernel/core_pattern` to stop cores from being 
hijacked by other tools Run the build. When it terminates with an output along the lines of "Segmentation fault (core dumped)", there should be a core dump file 
in the same directory as italocoind. It may be named just `core`, or `core.xxxx` with numbers appended. You can now analyse this core dump with `gdb` as 
follows: `gdb /path/to/italocoind /path/to/dumpfile` Print the stack trace with `bt` * To run italocoin within gdb: Type `gdb /path/to/italocoind` Pass 
command-line options with `--args` followed by the relevant arguments Type `run` to run italocoind
## Analysing Memory Corruption
We use the tool `valgrind` for this. Run with `valgrind /path/to/italocoind`. It will be slow.
## LMDB
Instructions for debugging suspected blockchain corruption as per @HYC There is an `mdb_stat` command in the LMDB source that can print statistics about the 
database but it's not routinely built. This can be built with the following command: `cd ~/italocoin/external/db_drivers/liblmdb && make` The output of 
`mdb_stat -ea <path to blockchain dir>` will indicate inconsistencies in the blocks, block_heights and block_info table. The output of `mdb_dump -s blocks <path 
to blockchain dir>` and `mdb_dump -s block_info <path to blockchain dir>` is useful for indicating whether blocks and block_info contain the same keys. These 
records are dumped as hex data, where the first line is the key and the second line is the data.
