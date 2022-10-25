# Initial setup for Ubuntu servers

This playbook can be used to perform an initial setup for an Ubuntu server. This playbook has been tested on Ubuntu 22.04 but should work for other Ubuntu LTS versions with little to no revisions.

## What does this playbook do?

- Ensures the `wheel` group is present.
- Adds the `wheel` group to `/etc/sudoers` to allow users in the group to have passwordless sudo rights.
- Creates a new regular user on the remote server.
- Copies a local public SSH key to the remote server.
- Disables password authentication via SSH to the `root` server.
- Installs an initial set of packages via Apt.
- Updates [UFW](https://wiki.ubuntu.com/UncomplicatedFirewall?action=show&redirect=UbuntuFirewall) to allow SSH connections and deny all other connections.

## Variables used in the playbook

- `create_user`: The username for the new regular user to create on the remote server. (default: `dennmart`)
- `copy_local_key`: The location of the public SSH file to copy from the local machine to the remote server. (default: `$HOME/.ssh/id_rsa.pub`)
- `sys_packages`: A list of Apt packages to install on the remote server. (default: `curl`, `vim`, `git` and `ufw`)

## Running the playbook

After updating the variables in `vars/default.yml`, execute the following command:

```
ansible-playbook -i <path to inventory file> -l <subset of hosts> -u <remote user> main.yml
```
