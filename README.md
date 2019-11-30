# sane-airscan -- Linux support of Apple AirScan (eSCL) compatible document scanners

Currently many new document scanners and MFPs come with Apple AirScan
support, also known as AirPrint scanning or eSCL protocol. And number of
AirScan-compatible devices tends to grow.

Looks that AirScan becomes de-facto standard protocol for document
scanners, connected to the network. This is very convenient for (Apple)
users, because installation of the new scanner becomes trivial task,
everything "just works" without need to worry about device drivers,
network configuration etc.

Unfortunately, Linux doesn't support AirScan, and the goal of this
project is to fix this situation.

### Installation
#### Install required libraries - Fedora and similar
As root, execute the following commands:
```
dnf install gcc git make pkgconf-pkg-config
dnf install avahi-devel avahi-glib-devel
dnf install glib2-devel libsoup-devel libxml2-devel
dnf install libjpeg-turbo-devel sane-backends-devel
```
#### Install required libraries - Ubuntu, Debian and similar
As root, execute the following commands:
```
apt-get install libavahi-client-dev libavahi-glib-dev
apt-get install gcc git make pkg-config
apt-get install libglib2.0-dev libsoup2.4-dev libxml2-dev
apt-get install libjpeg-turbo8-dev libsane-dev
```
#### Download, build and install sane-airscan
```
git clone https://github.com/alexpevzner/sane-airscan.git
cd sane-airscan
make
make install
```

## References

[kno10/python-scan-eSCL](https://github.com/kno10/python-scan-eSCL)

[SimulPiscator/AirSane](https://github.com/SimulPiscator/AirSane)

[markosjal/AirScan-eSCL.txt](https://gist.github.com/markosjal/79d03cc4f1fd287016906e7ff6f07136)
