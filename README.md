# Provision for development VM or laptop

## Preprequisites

```bash
sudo dnf install ansible python-dnf python3-psycopg2
```

## Run

1. Run behalf superuser.
2. You HAVE TO pass a developer account name as command line parameter.

```bash
$ sudo ansible-playbook -i inventory.ini playbook.yml --extra-vars='user=johndoe'
```

## Hints

Execute roles are tagged by `pg` tag:

```bash
$ sudo ansible-playbook --tags pg -i inventory.ini playbook.yml
```

For debug output we can add also `-vvvv` parameter.

## Testing with Vagrant

Install:

1. VirtualBox
2. Vagrant
3. vagrant-vbguest plugin
4. Ansible

After that, execute `vagrant up` in the project directory and wait until virtual machine will be ready.
When VM is ready, execute `vagrant ssh` and check if everything works and installed fine.
