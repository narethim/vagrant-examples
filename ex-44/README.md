# ex-44 - Increasing Disk Space of a Linux-based Vagrant Box on Provisioning (mod)

Example that:

 1. use vagrant to spin up a vm
 2. provision it using ansible `playbook`

## Commands

Start VM

```sh
vagrant up
```

Provision

```sh
vagrant up --provision

# or
vagrant provision
```

Connect a terminal session to the VM instance

```sh
vagrant ssh
```

## Cleanup

```sh
vagrant destroy -f
```

## References

* [Increasing Disk Space of a Linux-based Vagrant Box on Provisioning](https://marcbrandner.com/blog/increasing-disk-space-of-a-linux-based-vagrant-box-on-provisioning/)
* [How To Use Ansible Playbook With Vagrant up](https://computingforgeeks.com/run-ansible-playbook-with-vagrant-up/)
