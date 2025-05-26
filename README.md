# VPS setup

Ansible playbook that sets up software on my VPS.

## Setup

2. **Update inventory:** Edit `hosts.ini` with your server details

3. **Run playbook:**
```bash
ansible-playbook -i hosts.ini setup.yml --ask-vault-pass
```

## Vault management

```bash
# Edit vault
ansible-vault edit group_vars/all/vault.yml

# Change vault password  
ansible-vault rekey group_vars/all/vault.yml
```