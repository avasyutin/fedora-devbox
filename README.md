# Provision for development VM or laptop

## Preprequisites

1. Setup ssh.
2. Setup sudo without password.
3. Install ansible.
4. Install python2-dnf.

## Hints

Execute roles are tagged by `pg` tag:

```bash
$ ansible-playbook --tags pg -i inventory.ini playbook.yml --vault-password-file .ansible_vault_pass
```

For debug output we can add also `-vvvv` parameter.
