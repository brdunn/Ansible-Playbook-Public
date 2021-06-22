# Plex

The Plex playbook configures Plex on specified hosts.

## Setup
Make sure you have a hosts file setup in /inventories/ENV/hosts

## Running
- Make sure your public ssh key is on the remote server in the /home/ansible/.ssh/authorized_keys file.
- Make sure authorized keys are enabled in the /etc/ssh/sshd_config file
Run:
```
ansible-playbook -u ansible -i inventories/ENV/hosts --ask-become-pass playbooks/plex.yml
```

Enter the ansible user's password when prompted