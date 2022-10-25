# Ansible Playbooks

This is a personal collection of Ansible playbooks that I've put together to automate common server tasks. These playbooks are meant to serve as a base to create other playbooks that are more customized to a specific need.

## How to use

This repo assumes you have [installed Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) in your local system. It also assumes you have [an inventory file](https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html) to run the Ansible playbooks against.

Each directory in this repo contains a stand-alone Ansible playbook (`main.yaml`). If any variables are used in the playbook, they will be either defined in the main playbook or in the `vars/default.yml` file inside the directory.

In most cases, you can run the Ansible playbook inside a directory by modifying the variables you need and executing the following command:

```
ansible-playbook -i <path to inventory file> -l <subset of hosts> -u <remote user> main.yml
```

The `README` file in the directory will contain additional information on variables used in each playbook and how to run the playbook.
