# Provision for development VM or laptop

## Preprequisites

1. Setup sudo without password.
2. Install ansible.
3. Install python2-dnf.
4. Install libselinux-python.

## Run

1. Run behalf superuser.
2. You HAVE TO pass a developer account name as command line parameter.

```bash
$ sudo ansible-playbook -i inventory.ini playbook.yml --extra-vars='dev_user=johndoe'
```

## Hints

Execute roles are tagged by `pg` tag:

```bash
$ sudo ansible-playbook --tags pg -i inventory.ini playbook.yml
```

For debug output we can add also `-vvvv` parameter.

## Testing with Vagrant

Install:

1. ruby
2. ruby-devel
3. VirtualBox
4. Vagrant
5. vagrant-vbguest plugin
6. libvirt
7. vagrant-libvirt
8. libvirt-devel

After that, execute `vagrant up` in the project directory and wait until virtual machine will be ready.
When VM is ready, execute `vagrant ssh` and check if everything works and installed fine.
