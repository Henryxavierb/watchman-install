# Installing watchman on Ubuntu

### Install possible missing dependencies
```bash
sudo apt-get install git

sudo apt-get install libtool

sudo apt-get install libssl-dev

# Only Windows by WSL
sudo apt install pkg-config
```

### Preparing environment

```bash
cd ~

git clone https://github.com/facebook/watchman.git

cd watchman/

git checkout v4.9.0

sudo apt-get install -y autoconf automake build-essential python-dev

./autogen.sh

./configure --without-python --without-pcre --enable-lenient

make

sudo make install
```

Watchman installed!

```bash
watchman --version
```
