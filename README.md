# bbb-manifest
Manifest for the Beaglebone Black board

# Installing the Dependencies
$ sudo apt-get install gawk wget git-core diffstat unzip texinfo gcc-multilib build-essential chrpath socat cpio python python3 python3-pip python3-pexpect xz-utils debianutils iputils-ping python3-git python3-jinja2 libegl1-mesa libsdl1.2-dev pylint3 xterm rsync curl

# Installing the repo Utility
$ mkdir ~/bin

$ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo

$ chmod a+x ~/bin/repo

$ export PATH=~/bin:$PATH

# Configuring git
$ git config --global user.name "Your Name"

$ git config --global user.email "Your Email"

# To pull the manifest

1A). Pull from main

repo init -u https://github.com/bathroomchef/bbb-manifest.git -m bbb.xml

1B). Pull from a branch

repo init -u https://github.com/bathroomchef/bbb-manifest.git -b {branch_name} -m bbb.xml

2). repo sync

repo sync


# To source the environment for Yocto

source environment-script build


# To build the image
bitbake core-image-full-cmdline



# To flash the image
sudo dd if=core-image-full-cmdline-beaglebone-yocto.wic of=/dev/sd{device} bs=1M status=progress conv=fsync oflag=sync

