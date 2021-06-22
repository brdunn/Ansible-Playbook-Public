# Prometheus

The prometheus playbook installs Alertmanager onto specified hosts.  This playbook was specifically created to deploy Alertmanager on servers that run on my home network.

## Setup
Make sure you have a hosts file setup in /inventories/ENV/hosts

## Running
- Make sure your public ssh key is on the remote server in the /home/ansible/.ssh/authorized_keys file.
- Make sure authorized keys are enabled in the /etc/ssh/sshd_config file
Run:
```
ansible-playbook -u ansible -i inventories/ENV/hosts --ask-become-pass --ask-vault-pass playbooks/alertmanager.yml
```

Enter the ansible user's password when prompted