# bbb-manifest
Manifest for the Beaglebone Black board

repo init -u https://github.com/bathroomchef/bbb-manifest.git -m bbb.xml
repo sync


# To source the environment for Yocto
cd sources/poky/
source oe-init-build-env
