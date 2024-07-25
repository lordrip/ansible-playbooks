# ansible-playbooks
Ansible playbooks to configure Linux hosts

## Table of Contents
### [SSH Jump](./docs/ssh-jump.md)
### [Executing playbooks](#executing-playbooks)

### Executing playbooks
```
ansible-playbook -i ./inventory/hosts.ini ./playbooks/install_packages.yml --ask-vault-pass
```