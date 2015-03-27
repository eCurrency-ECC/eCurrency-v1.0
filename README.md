Coin Type: SHA256 PoW
Halving at 210,000 Blocks
Initial Coins per Block = 100 ECC
Target Spacing = 3 Minutes
Target Timespan = 100 Hours
Coinbase Maturity = 99 Blocks
Premine = 0 %
Max coinbase = 42000000 + 0 Pre-Mine = 42000000 coins
P2P Port = 11075
RPC Port = 21075

Nix Setup:

apt-get update
apt-get upgrade

apt-get install build-essential
apt-get install libssl-dev
apt-get update
apt-get install libdb4.8++
apt-get install libboost-all-dev
apt-get install libdb++-dev libminiupnpc-dev
apt-get install git-core
apt-get install ntp

cd ~
mkdir eCurrency
cd /usr/local/
git clone https://github.com/eCurrency-ECC/eCurrency-v1.0.git
cd eCurrency-v1.0
cd /src
make -f makefile.unix USE_UPNP=
strip bitcoind
cp bitcoind ~/eCurrency/ecurrencyd

**(If it fails to compile, be sure that the entire folder is chmod 777 recursively to all folders and directories.)**

To start the daemon:

./ecurrencyd

eCurrency Commands:
./ecurrencyd getinfo
./ecurrencyd help
./ecurrencyd getaccountaddresses ""