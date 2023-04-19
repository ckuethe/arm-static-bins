# What

Some armhf static binaries that I've found useful while analyzing
some IoT things.

# Why?

Because not all the tools I want are in Saumil's [repo](https://github.com/therealsaumil/static-arm-bins/).

# How?

1. install `qemu-user-static` on your workstation
1. grab your favorite armhf distribution. I used [DietPi for ZeroPi](https://dietpi.com/docs/hardware/#nanopi-series-friendlyelec)
1. mount the image and copy the contents of the rootfs into a directory
1. chroot into it
1. install build tools, eg. `apt update && apt install build-essential`
1. download the sources for the static tools you want to build
1. Configure. `env CFLAGS="-static -O2"` or `--enable-static` might be helpful.

# Packages
* dtach - https://github.com/crigler/dtach
* hexedit - https://github.com/pixel/hexedit
* sntpc - https://github.com/ckuethe/sntpc
* tcpdump - https://github.com/the-tcpdump-group/tcpdump
