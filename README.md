# Provision for development VM or laptop

## Preprequisites

1. Setup ssh.
2. Setup sudo without password.
3. Install ansible.
4. Install python2-dnf.
5. Install libselinux-python.
6. Install ruby, ruby-devel via dnf.

## Neovim

After neovim was installed run it and execute:

1. :PlugInstall (and restart Neovim).
2. :UpdateRemotePlugins (and restart Neovim also).

## Hints

Execute roles are tagged by `pg` tag:

```bash
$ ansible-playbook --tags pg -i inventory.ini playbook.yml --vault-password-file .ansible_vault_pass
```

For debug output we can add also `-vvvv` parameter.

## Testing with Vagrant

Install:

1. VirtualBox
2. Vagrant
3. vagrant-vbguest plugin
3. libvirt
4. vagrant-libvirt
5. libvirt-devel

After that, execute `vagrant up` in the project directory and wait until virtual machine will be ready.

TODO: ansible, vm checking instructions
