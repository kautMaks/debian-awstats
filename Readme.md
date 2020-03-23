# debian-awstats

This repository provides awstats debianized source package for Debian.

Source repository - https://salsa.debian.org/debian/awstats

## Install build requirements:

```
apt-get -qq update && apt-get -y install build-essential debhelper devscripts dpkg-dev fakeroot git ant default-jdk sharutils

```

## Clone this branch to your build server:

```
cd /root
git clone https://github.com/kautMaks/debian-awstats.git
```

## Get awstats sources:

```
wget https://prdownloads.sourceforge.net/awstats/awstats-7.7.tar.gz
tar -xvf awstats-7.7.tar.gz && mv awstats-7.7/* debian-awstats/
cd  debian-awstats/
```

## Build awstats with enabled tests:

```
debuild -us -uc -b
```

## Build awstats with disabled tests:

```
DEB_BUILD_OPTIONS=nocheck debuild -us -uc -b
```
