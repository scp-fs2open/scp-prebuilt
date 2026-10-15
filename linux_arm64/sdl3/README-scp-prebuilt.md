SDL version 3.4.18 built on Ubuntu 22.04 (docker)

[SDL3-3.4.18.tar.gz](https://github.com/libsdl-org/SDL/releases/download/release-3.4.18/SDL3-3.4.18.tar.gz)

Set up prerequisites:

```bash
apt update && apt upgrade
```
```bash
apt install build-essential gcc-9 g++-9 git make pkg-config cmake ninja-build gnome-desktop-testing libasound2-dev libpulse-dev libaudio-dev libfribidi-dev libjack-dev libsndio-dev libx11-dev libxext-dev libxrandr-dev libxcursor-dev libxfixes-dev libxi-dev libxss-dev libxtst-dev libxkbcommon-dev libdrm-dev libgbm-dev libgl1-mesa-dev libgles2-mesa-dev libegl1-mesa-dev libdbus-1-dev libibus-1.0-dev libudev-dev libthai-dev libusb-1.0-0-dev libpipewire-0.3-dev libwayland-dev libdecor-0-dev liburing-dev libunwind-dev
```
```bash
update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-9 90 --slave /usr/bin/g++ g++ /usr/bin/g++-9
```

Build:

```bash
cd SDL3-3.4.18
```
```bash
cmake -B build.`uname -m` .
```
```bash
cmake --build build.`uname -m`
```
```bash
strip --strip-unneeded build.`uname -m`/libSDL3.so.0.*
```
