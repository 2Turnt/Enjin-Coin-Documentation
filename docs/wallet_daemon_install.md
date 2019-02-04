# Enjin Wallet Daemon Installation

Here are the instruction to install the Enjin Wallet Daemon application under various OSes. This document necessitates an up-to-date OS, and knowledge of the command line and system administration.

Administrator access to the target computer is required.

## Windows 10

### Requirements Summary
* node.js
* Python 2
* Visual Studio Build Tools
* git

See <https://github.com/nodejs/node-gyp/#on-windows>

### Install node.js

Install node.js 11 from the official website <https://nodejs.org/>. Then, in an administrator command prompt (Windows+R `cmd` run with ctrl-shift-enter):

```
npm install --global --production windows-build-tools
```

Install git from the official website <https://git-scm.com/download/win>

### Install Wallet Daemon
Right-click `enjin-wallet-daemon-master.zip` and select "_Extract All..._" Then, in a command line (replace `<CODE_FOLDER>` with whatever folder you extracted the archive to):
```
cd <CODE_FOLDER>\enjin-wallet-daemon-master
npm install
```

## macOS

### Requirements Summary
* macOS command line developer tools
* node.js

### Install homebrew
```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Install node.js
```bash
brew install node
```

### Install Wallet Daemon
```bash
unzip enjin-wallet-daemon-master.zip
cd enjin-wallet-daemon-master
npm install
```

## Linux (Debian 10 _Buster_)

### Requirements Summary
* build tools (gcc, make, etc.) build-essential
* git
* node.js
* unzip

### Install node.js
```bash
su -
apt install build-essential curl git unzip
curl -sL https://deb.nodesource.com/setup_11.x | bash -
apt install nodejs
```

### Install Wallet Daemon
```bash
unzip enjin-wallet-daemon-master.zip
cd enjin-wallet-daemon-master
npm install
```

## Linux (Ubuntu Server 18.04 LTS)
### Requirements Summary
* build tools (gcc, make, etc.) build-essential
* node.js
* unzip

### Install node.js
```bash
sudo apt install unzip build-essential
curl -sL https://deb.nodesource.com/setup_11.x | sudo -E bash -
sudo apt install nodejs
```

### Install Wallet Daemon
```bash
unzip enjin-wallet-daemon-master.zip
cd enjin-wallet-daemon-master
npm install
```

## All Platforms

### Run Wallet Daemon _(New Wallet)_
Open an account on the trusted platform and get a link code (e.g. XY1ABC). Replace the `<LINK_CODE>` placeholder bellow with that code.

```bash
node src/main.js account new
node src/main.js link <LINK_CODE>
node src/main.js
```