# ex-3 - vagrant, ansible playbook, templates example

Example that:

 1. uses vagrant to spin up a vm
 2. provisions it using ansible `playbook`
 3. uses `site.yml` playbook which make use of variable substitution and template using jinja

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

## Verify

firefox http://192.168.50.15:8000

Modify /etc/hosts with the following line

192.168.50.15 flask.mydomain.com

firefox http://flask.mydomain.com

## Cleanup

```sh
vagrant destroy -f
```

## References

* [Vagrant and Ansible](https://www.bogotobogo.com/DevOps/Vagrant/Vagrant_Ansible.php)
