# Pihole Exporter

The pihole exporter playbook installs pihole_exporter onto specified hosts.  This playbook was specifically created to deploy the exporter on servers that run on my home network.

## Setup
Make sure you have a hosts file setup in /inventories/ENV/hosts

## Running
- Make sure your public ssh key is on the remote server in the /home/ansible/.ssh/authorized_keys file.
- Make sure authorized keys are enabled in the /etc/ssh/sshd_config file
Run:
```
ansible-playbook -u ansible -i inventories/ENV/hosts -K --limit IP_ADDR playbooks/pihole_exporter.yml
```

Enter the ansible user's password when prompted