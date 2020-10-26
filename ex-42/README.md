# ex-42 - vagrant, ansible playbook, yocto on Ubuntu 20.04

Example that:

 1. uses vagrant to spin up a vm
 2. provisions it using ansible `playbook`
 3. uses `main.yml` playbook

## Bring VM up Commands

### Start VM

```sh
vagrant up
```

### Provision

```sh
vagrant up --provision

#or
vagrant provision
```

### Connect a terminal session to the VM instance

```sh
vagrant ssh
```

## Setup commands

```sh
cd ~/poky
git fetch --tags

git checkout tags/yocto-3.1.3 -b my-yocto-3.1.3
```

## Building Your Image¶

### 1. Initialize the Build Environment

```sh
cd ~/poky
source oe-init-build-env
```

### 2. Examine Your Local Configuration File

When you set up the build environment, a local configuration file named local.conf becomes available in a conf subdirectory of the Build Directory. For this example, the defaults are set to build for a qemux86 target, which is suitable for emulation. The package manager used is set to the RPM package manager.

Edit `conf/local.conf` file

```sh
vi conf/local.conf
```

Append to the end of file to save space.

```sh
INHERIT += "rm_work"
```

### 3. Start the Build

```sh
bitbake core-image-sato
```

### 4. Simulate Your Image Using QEMU

Once this particular image is built, you can start QEMU, which is a Quick EMUlator that ships with the Yocto Project:

```sh
runqemu qemux86-64
```

### 5. Exit QEMU

Exit QEMU by either clicking on the shutdown icon or by typing Ctrl-C in the QEMU transcript window from which you evoked QEMU.

## Teardown and cleanup commands

Stop VM

```sh
vagrant halt
```

Destroy VM

```sh
vagrant destroy

# force destroy
vagrant destroy -f
```

```sh
# list all vagrant box
vagrant box list
```
