# PostgreSQL server setup for Ubuntu 22.04 servers

This playbook sets up the latest version of [PostgreSQL](https://www.postgresql.org/) on an Ubuntu 22.04 server.

## What does this playbook do?

- Installs prerequisite packages for PostgreSQL via Apt.
- Downloads and imports the Apt repository key for PostgreSQL.
- Sets up the [official PostgreSQL Apt repository for Ubuntu](https://www.postgresql.org/download/linux/ubuntu/).
- Installs the latest PostgreSQL server.
- Starts the PostgreSQL service.

## Running the playbook

Execute the following command:

```
ansible-playbook -i <path to inventory file> -l <subset of hosts> -u <remote user> main.yml
```
