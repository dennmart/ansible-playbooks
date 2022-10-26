# Install Node.js from NodeSource repository for Ubuntu servers

This playbook can be used to install Node.js using [NodeSource](https://github.com/nodesource/distributions) on an Ubuntu 22.04 server.

## What does this playbook do?

- Ensure that curl is installed on the remote server.
- Runs the NodeSource setup script using curl to set up the Apt repo and dependencies.
- Installs the latest version of Node.js according to the setup script used.

## Variables used in the playbook

- `nodesource_setup_url`: The URL of the NodeSource setup script for Ubuntu (default: `https://deb.nodesource.com/setup_18.x`)

## Running the playbook

After updating the variables in `vars/default.yml`, execute the following command:

```
ansible-playbook -i <path to inventory file> -l <subset of hosts> -u <remote user> main.yml
```
