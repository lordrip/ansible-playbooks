# ansible-playbooks
Ansible playbooks to configure Linux hosts

## Table of Contents
### [SSH Jump](./docs/ssh-jump.md)
### [Executing playbooks](#executing-playbooks)

### Executing playbooks
```
# Install packages
ansible-playbook -i ./inventory/hosts.ini ./playbooks/install_packages.yml --ask-vault-pass

# Update packages to latest version
ansible-playbook -i ./inventory/hosts.ini ./playbooks/update_packages.yml --ask-vault-pass

# Run all playbooks
ansible-playbook -i ./inventory/hosts.ini ./playbooks/ --ask-vault-pass
```