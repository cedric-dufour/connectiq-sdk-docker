Containerized ConnectIQ Development Environment for Linux
==

TL;DR:

* have a working [Docker](https://www.docker.com/) environment

* export CIQ_SDK_VERSION='<version>'

* build the Docker Image: [./build](./build)

* run the Docker Image: [./run](./run)

* launch the SDK manager to install devices: `sdkmanager`

* build one of my CIQ project (e.g. [RawLogger](https://github.com/cedric-dufour/connectiq-app-rawlogger/)): `make iq`

Other available environment variables:

* `CIQ_SDK_DIR`: path to SDK installation directory (default: `${HOME}/.Garmin/ConnectIQ`)`

* `CIQ_SRC_DIR`: path to your CIQ projects source code, mounted in ` /home/ciq/src` (default: none)

Post scriptum: Garmin ConnectIQ SDK uses long-deprecated libraries - like `libwebkit-1.0` or `libjpeg8` -
which are no longer available on recent Linux distributions. This containerized development environment
works around this issue by being based on `ubuntu:bionic (18.04, LTS)` image.
