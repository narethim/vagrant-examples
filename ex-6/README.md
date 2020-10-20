# ex-6 - vagrant to spin up multiple VMs

Example that:

 1. uses vagrant to spin up multiple VMs

## Commands

Start VM

```sh
vagrant up
```

Check host names

```sh
vagrant ssh-config
```

Connect a terminal session to the VM instance

```sh
vagrant <hostname>
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
