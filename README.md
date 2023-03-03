# osx-on-docker
Run macOS on top of Docker with near-native performance with ease

## Requirements
- Docker
- docker-compose or Docker compose plugin
- X11

## List of supported macOS variant
- Ventura  [34Gi]
- Monterey [?Gi]
- Big Sur  [?Gi]

## How to use it?
- Clone this repository
```shell
$ git clone https://github.com/lutfailham96/osx-on-docker
```
- Choose macOS variant, ex: ventura
```shell
$ export variant="ventura" \
    && cd osx-on-docker \
    && cd ${variant} \
    && ./run.sh
```
- The script will automatically download macOS base image & run it in qemu

## Default username & password
- username: admin
- password: letmein

## Common Issues
### Error "gtk initialization failed"
- Arch Linux
``` shell
$ sudo pacman -S xorg-xhost
```
- Debian, Ubuntu, Linux Mint
```shell
$ sudo apt update \
    && sudo apt install -y x11-xserver-utils \
    && xhost +
```
- RHEL, Centos, Fedora
```shell
$ sudo yum install xorg-x11-server-utils
```
