# Explore Open Containers

https://github.com/opencontainers

# Download and build runc

## Install Go

```bash
./install_go
```
OR
```bash
cd ~
wget https://dl.google.com/go/go1.11.linux-amd64.tar.gz
tar -xzv < go1.11.linux-amd64.tar.gz
rm go1.11.linux-amd64.tar.gz
ln -s ~/go/bin/go ~/bin/go
```

## Build runc

Build:
```
cd ~/go/src
mkdir -p github.com/opencontainers
cd github.com/opencontainers
git clone https://github.com/opencontainers/runc
cd runc

# make with libseccomp
make

# make without libseccomp
make BUILDTAGS=""

# copy the runc executable to /sbin
sudo make install
```
