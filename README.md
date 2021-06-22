# Ansible Playbook
This Ansible playbook was created to easily deploy the services that I use on my home network. To run any of the playbooks, you must have a user named 'ansible' on the remote machine(s) and your public ssh key in the ansible user's authorized_keys file. You must also update the hosts file to reflect your environment.

## Add Ansible user
1. ```useradd -m ansible```
1. ```passwd ansible```
1. ```usermod -aG sudo ansible```
1. Add the following line to /etc/sudoers:
    ```ansible ALL=(ALL) NOPASSWD: ALL```

## Create Inventories
To use the playbooks and roles, you must have host files and group_vars created for each playbook. The structure should be as follows:
├── inventories
│   └── prod
│       ├── group_vars
│       │   ├── alertmanager.yml
│       │   ├── all.yml
│       │   ├── node_exporter.yml
│       │   ├── pihole.yml
│       │   ├── plex.yml
│       │   ├── prometheus.yml
│       │   └── proxmox.yml
│       └── hosts
├── playbooks
│   └── ...
└── roles
    └── ...
