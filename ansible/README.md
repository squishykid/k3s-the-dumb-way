Preparation:

1. flash armbian to eMMC modules
1. change the root password to something else. we will enable ssk keys later
1. boot board and change the hostname to something unique -> use `hostnamectl set-hostname <hostname>`
1. list the hostnames in `inventory/hosts.ini`

Running it:

`ansible-playbook main.yml -i inventory/hosts.ini --extra-vars "ansible_password=<somethign here>"`

after the first time, you should be able to omit the `ansible_password` field