# vagrant-examples

vagrant examples

## Useful elementary `vagrant` CLI commands

```sh
# Initialize
vagrant init ubuntu/bionic64

# Start it
vagrant up

# Stop it
vagrant halt

# Destroy it
vagrant destroy

vagrant destroy -f
```

## Useful `vagrant box` CLI commands

```sh
# Vagrant box help
vagrant box -h

# List boxes
vagrant box list
```

## Useful `vagrant ssh-config` CLI commands

```sh
# Vagrant box help
vagrant ssh-config
```

Examples

```sh
c:\projects\otsuarez\vagrant-k3s-mod2>vagrant ssh-config
Host master
  HostName 127.0.0.1
  User vagrant
  Port 2222
  UserKnownHostsFile /dev/null
  StrictHostKeyChecking no
  PasswordAuthentication no
  IdentityFile c:/projects/otsuarez/vagrant-k3s-mod2/.vagrant/machines/master/virtualbox/private_key
  IdentitiesOnly yes
  LogLevel FATAL

Host node1
  HostName 127.0.0.1
  User vagrant
  Port 2200
  UserKnownHostsFile /dev/null
  StrictHostKeyChecking no
  PasswordAuthentication no
  IdentityFile c:/projects/otsuarez/vagrant-k3s-mod2/.vagrant/machines/node1/virtualbox/private_key
  IdentitiesOnly yes
  LogLevel FATAL
```

```sh
# Connect to `master` node
vagrant ssh master

# Connect to `node1` node
vagrant ssh node1
```

## Other examples

* [geerlingguy/ansible-vagrant-examples](https://github.com/geerlingguy/ansible-vagrant-examples)

```sh
cd ~/projects/GitHub/

git clone https://github.com/geerlingguy/ansible-vagrant-examples.git
```

* [ex-1 - vagrant, ansible roles example](ex-1/README.md)
* [ex-2 - vagrant, simple ansible playbook example](ex-2/README.md)
* [ex-3 - vagrant, ansible playbook, templates example](ex-3/README.md)