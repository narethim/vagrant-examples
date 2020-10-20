# ex-4 - vagrant and yocto

Example that:

 1. uses vagrant to spin up a vm

## Commands

Start VM

```sh
vagrant up
```

Connect a terminal session to the VM instance

```sh
vagrant ssh
```

Destroy VM

```sh
vagrant destroy -f

# force destroy
vagrant destroy -f
```

```sh
# list all vagrant box
vagrant box list
```

## Bootlin build instruction for its Class lab

```sh
## --------------------
##
## Bootlin build instruction for its Class lab
##
## --------------------
```

## Install lab data

```sh
sudo dpkg-query -f '${binary:Package}\n' -W > packages_list_00.txt
sudo dpkg-query -f '${binary:Package}\n' -W | wc -l

sudo apt update

sudo dpkg-query -f '${binary:Package}\n' -W > packages_list_01.txt
sudo dpkg-query -f '${binary:Package}\n' -W | wc -l


cd
wget https://bootlin.com/doc/training/yocto/yocto-labs.tar.xz
tar xvf yocto-labs.tar.xz
```

## Setup

```sh
sudo apt -y install bc build-essential chrpath cpio diffstat gawk git python texinfo wget

sudo dpkg-query -f '${binary:Package}\n' -W > packages_list_02.txt
sudo dpkg-query -f '${binary:Package}\n' -W | wc -l
```

## Download Yocto

```sh
cd $HOME/yocto-labs/
git clone git://git.yoctoproject.org/poky.git
cd $HOME/yocto-labs/poky
git checkout -b sumo-19.0.0 sumo-19.0.0
git am $HOME/yocto-labs/bootlin-lab-data/0001-bblayers-do-not-include-meta-yocto-bsp.patch


cd $HOME/yocto-labs/
git clone git://git.yoctoproject.org/meta-ti.git
cd $HOME/yocto-labs/meta-ti
git checkout -b sumo ti2018.02
git am $HOME/yocto-labs/bootlin-lab-data/0001-Simplify-linux-ti-staging-recipe.patch
git am $HOME/yocto-labs/bootlin-lab-data/0002-do-not-use-base_read_file.patch
git am $HOME/yocto-labs/bootlin-lab-data/0003-recipes-bsp-u-boot-fix-non-booting-U-Boot.patch
git am $HOME/yocto-labs/bootlin-lab-data/0004-fix-bitbake-warnings.patch
```

## Set up the build environment

```sh
cd $HOME/yocto-labs
source poky/oe-init-build-env

bitbake core-image-minimal
```
