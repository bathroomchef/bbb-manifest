# bbb-manifest
Manifest for the Beaglebone Black board

repo init -u https://github.com/bathroomchef/bbb-manifest.git -m bbb.xml

repo sync


# To source the environment for Yocto
cd sources/poky/

source oe-init-build-env

# To flash the image
sudo dd if=core-image-full-cmdline-beaglebone-yocto.wic of=/dev/sd{device} bs=1M status=progress conv=fsync oflag=sync

