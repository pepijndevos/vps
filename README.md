# VPS setup

Ansible playbook that sets up software on my VPS.

## Setup

1. **Create vault for CouchDB password:**
```bash
ansible-vault create group_vars/all/vault.yml
```

Add your password:
```yaml
vault_couchdb_password: "your_secure_password_here"
```

2. **Update inventory:** Edit `hosts.ini` with your server details

3. **Run playbook:**
```bash
ansible-playbook -i hosts.ini nginx-setup.yml --ask-vault-pass
```

## Vault management

```bash
# Edit vault
ansible-vault edit group_vars/all/vault.yml

# Change vault password  
ansible-vault rekey group_vars/all/vault.yml
```