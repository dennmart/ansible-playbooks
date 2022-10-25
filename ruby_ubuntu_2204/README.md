# Install Ruby from source for Ubuntu servers

This playbook can be used to perform install a specific version of [Ruby](https://www.ruby-lang.org/en/) on an Ubuntu 22.04 server.

## What does this playbook do?

- Checks if specified version of Ruby is already installed. If it is, the playbook will stop running.
- Installs prerequisite packages for Ruby via Apt.
- Download and unpack the Ruby source to a specified directory on the remote server.
- Builds Ruby from source.

## Variables used in the playbook

- `ruby_version`: The version of Ruby to install (default: `3.1.2`)
- `ruby_full_version`: The full version of Ruby to verify if it's already installed (default: `ruby 3.1.2p20`)
- `ruby_source_url`: The full URL to download the Ruby source (default: `https://cache.ruby-lang.org/pub/ruby/3.1/ruby-{{ ruby_version }}.tar.gz`)
- `ruby_source_sha`: The SHA checksum to verify the Ruby source archive (default: `sha256:61843112389f02b735428b53bb64cf988ad9fb81858b8248e22e57336f24a83e`)

## Running the playbook

After updating the variables in `vars/default.yml`, execute the following command:

```
ansible-playbook -i <path to inventory file> -l <subset of hosts> -u <remote user> main.yml
```
