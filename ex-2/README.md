# ex-2 - vagrant, simple ansible playbook example

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

#or
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

* [How To Use Ansible Playbook With Vagrant up](https://computingforgeeks.com/run-ansible-playbook-with-vagrant-up/)
