# testgear - open source test automation for embedded

## 1. Introduction

Test Gear is a modern lightweight hardware test automation framework which can
be used for production line testing and prototype testing.

For now, Test Gear is to be considered work in progress, experimental, and a
playground for testing design ideas to obtain best possible test creation and
execution flow.


### 1.1 Overview

Test Gear includes the following four components:

 * testgeard (Server)
 * libtestgear (Client library)
 * testgearctl (Control application)
 * testgear-plugins (Test and interface plugins)

The control application runs test scripts written in Lua and uses the client
library to communicate with servers featuring various test and interface
plugins. The end result is a test log listing passed and failed tests.

![Test Gear Overview](images/testgear-overview.png?raw=true)


### 1.2 Motivation

To make better and simpler open source tools for test automation that can be
used with devices running Linux or ZephyrOS.


## 2. Test plugins

The plugins listed next are generic plugins for testing or interfacing various
hardware (devices, instruments, peripherals, etc.) using popular GNU/Linux APIs.
They are made to work on most modern GNU/Linux systems.

Custom plugins for testing or interfacing custom hardware using custom APIs can
easily be added by writing plugins following the Test Gear plugin model. You
decide which license you want to apply to your plugins and whether you will make
them publicly available or not. However, it is strongly encouraged to make your
plugins open source when possible so that everyone can benefit from common work
and, most importantly, avoid or minimize duplicate work.


### 2.1 Available plugins (Linux)

| Plugin                     | Description                  |
|----------------------------|------------------------------|
| fb                         | Framebuffer test             |
| audio                      | Audio I/O test (ALSA)        |
| shell                      | Shell interface              |
| dummy                      | Dummy test                   |
| cpu                        | CPU stress test              |
| keyboard                   | Keyboard input test          |
| usb                        | USB I/O test (loopback)      |

### 2.2 Planned plugins (TODO)

| Plugin                     | Description                  |
|----------------------------|------------------------------|
| kmsdrm                     | KMS/DRM performance test     |
| touch                      | Touch input test             |
| mouse                      | Mouse input test             |
| storage                    | Storage I/O performance test |
| memory                     | Memory I/O performance test  |
| camera                     | Camera test                  |
| wifi                       | Wifi 802.11 test             |
| network                    | Network test                 |
| bluetooth                  | Bluetooth test               |
| gpio                       | GPIO interface               |
| i2c                        | I2C interface                |
| lxi                        | LXI class C interface        |
| gpib                       | GPIB interface               |


## 3. Platform support

The Test Gear server (testgeard) currently supports GNU/Linux systems only.
However, in the future it is planned to support microcontoller systems and even
embedding into bootloaders such a u-boot (which is useful for complete memory
        testing in particular).

The Test Gear control client and control application is currently a very simple
command line application for GNU/Linux systems only. In the future, the plan is
to add a user friendly graphical control client with multi-platform support. The
lxi-gui application provides some of the same features as the commandline tool
and more but presents them in a modern GUI frontend.


## 4. Download

Test Gear is still in development - there are no official release tarballs available yet.

## 5. Contributing

testgear is open source. If you want to help out with the project please feel
free to join in.

All contributions (bug reports, code, doc, ideas, etc.) are welcome.

Please use the github issue tracker and pull request features.

Also, if you find this free open source software useful please feel free to
consider making a donation of your choice:

[![Donate](images/Paypal.png)](https://www.paypal.me/lundmar)

## 6. Support

Submit bug reports [here](https://github.com/testgear/issues).

## 7. Website

Visit [testgear.github.io](https://testgear.github.io)


## 8. License

This code is released under BSD-3, commonly known as the 3-clause (or
"modified") BSD license.

## 9. Authors

Created and maintained by Martin Lund \<martin.lund@keep-it-simple.com>

See the AUTHORS file for full list of contributors.

