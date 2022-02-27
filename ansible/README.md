Getting set up

Create virtual environment
`python3 -m venv .venv`

Go into virtual env
` . .venv/bin/activate`

Install python requirements
`pip install -m requirements.txt`

Install Ansible Requirements
`ansible-galaxy install -r requirements.yml`

Preparation:

1. flash armbian to eMMC modules
1. change the root password to something else. we will enable ssk keys later
1. boot board and change the hostname to something unique -> use `hostnamectl set-hostname <hostname>`
1. list the hostnames in `inventory/hosts.ini`

Running it:

`ansible-playbook main.yml -i inventory/hosts.ini --extra-vars "ansible_password=<somethign here>"`

after the first time, you should be able to omit the `ansible_password` field