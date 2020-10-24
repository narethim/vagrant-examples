# ex-61 - vagrant to spin up multiple VMs and use `ansible.cfg` in current directory

A simplified version of ex-6 example.

Example that:

 1. uses vagrant to spin up multiple VMs
 2. uses `ansible.cfg` in current directory
 3. uses vagrant created inventory file indicated in `ansible.cfg` in current directory

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

## Ansible playbook

```sh
# Will use ansible.cfg in current dir
ansible-playbook main.xml
```
