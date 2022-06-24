# Ansible Playbook for Ionos

This playbook configures a fresh VPS on [Ionos](https://www.ionos.co.uk/servers/vps) to host my blog [jakeprice.dev](https://jakeprice.dev).

The blog repository can be found [here](https://github.com/jakeprice-dev/jakeprice.dev) and the theme [here](https://github.com/jakeprice-dev/jpd).

## Ansible Galaxy Collections

Install the collections specified in `requirements.yml`.

```sh
ansible-galaxy collection install -r requirements.yml
```

## Ansible Vault

`vault.yml` should contain values for the below variables:

```yaml
admin_user: <value>
```

The `vault.yml` file is encrypted and passphrase protected. `.vault_password` which stores the password to open it is not committed to version control. If lost create a new `vault.yml` and enter values for the above vault variables.

## Run Playbook

Run the playbook as normal.

```sh
ansible-playbook playbook.yml 
```

