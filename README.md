# [![Build Status](https://travis-ci.org/ca333/dsec.svg?branch=master)](https://travis-ci.org/ca333/dsec)

![alt text](https://i.imgur.com/2dAbVYW.png)
## DSEC blockchain daemon
This is the official DSEC blockchain daemon repository. Please use the dev branch.

## Development Resources
- Website: https://devsec.info
- Blockexplorer and insight API: https://dsec.ac


## Specification

- Init Supply: 7 million DSEC.
- Block Time: 10M + block on demand generation
- Algorithm: Equihash 

## Getting started
Dependencies
------------

```
#install dependencies:
sudo apt-get install build-essential pkg-config libc6-dev m4 g++-multilib autoconf libtool ncurses-dev unzip git python python-zmq zlib1g-dev wget libcurl3-gnutls-dev bsdmainutils automake
```


```
#clone and build dsec
git clone https://github.com/ca333/dsec
cd dsec
git checkout dev
git pull
./zcutil/fetch-params.sh
# -j8 uses 8 threads - replace 8 with number of threads you want to use
./zcutil/build.sh -j8
```
### launch DSEC
```
cd src/
./komodod -ac_name=DSEC -ac_supply=7000000 -addnode=185.141.60.27 &
```

### use DSEC
```
./komodo-cli -ac_name=DSEC getinfo
```

=======
This software is based on Zcash. **Zcash is unfinished and highly experimental.** Use at your own risk.

License
-------
For license information see the file [COPYING](COPYING).
