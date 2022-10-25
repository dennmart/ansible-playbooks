# Caddy server setup for Ubuntu 22.04 servers

This playbook sets up [Caddy 2](https://caddyserver.com/) on an Ubuntu 22.04 server.

## What does this playbook do?

- Installs prerequisite packages for Caddy via Apt.
- Downloads the Apt repository key for Caddy.
- Sets up the Caddy Apt repository.
- Installs the Caddy server.
- Starts the Caddy service.
- Updates [UFW](https://wiki.ubuntu.com/UncomplicatedFirewall?action=show&redirect=UbuntuFirewall) to allow HTTP and HTTPS connections.

## Running the playbook

Execute the following command:

```
ansible-playbook -i <path to inventory file> -l <subset of hosts> -u <remote user> main.yml
```
