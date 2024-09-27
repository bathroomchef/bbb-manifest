# bbb-manifest
Manifest for the Beaglebone Black board

repo init -u https://github.com/bathroomchef/bbb-manifest.git -m bbb.xml

repo sync


# To source the environment for Yocto

source environment-script build


# To build the image
bibake core-image-full-cmdline



# To flash the image
sudo dd if=core-image-full-cmdline-beaglebone-yocto.wic of=/dev/sd{device} bs=1M status=progress conv=fsync oflag=sync

