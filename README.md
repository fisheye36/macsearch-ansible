# Description

`macsearch.yml` is a simple Ansible playbook that returns manufacturer name of a network device, given its MAC address.

It uses web API provided by https://macaddress.io/.

# Usage

## Prerequisites

You need to have Ansible installed on your system to execute the playbook. Visit
[this page](https://docs.ansible.com/ansible/latest/installation_guide/index.html) for installation instructions.

## Running Ansible playbook

To run the playbook, use:

```shell
ansible-playbook macsearch.yml --extra-vars "api_key=${MACSEARCH_API_KEY} mac=44:38:39:ff:ef:57"
```

If you already have `MACSEARCH_API_KEY` environment variable set, you don't need to set it explicitly during playbook
execution:

```shell
export MACSEARCH_API_KEY
ansible-playbook macsearch.yml --extra-vars "mac=44:38:39:ff:ef:57"
```
