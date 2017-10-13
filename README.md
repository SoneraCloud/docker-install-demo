docker-install-demo
==============================

The install-docker.yml playbook installs the latest docker-ce package on your running
instance regardless of which python version you have on your VM.

Tested distros:
----------
- CentOS 7
- Fedora
- Debian Stretch, Jessie
- Ubuntu Trusty, Xenial

Example usage:
----------
```
ansible-playbook -i "1.2.3.4," install-docker.yml
```
in which 1.2.3.4 is your instance's IP address. If the username that you use to log
into your instance is different from your current local username, then you need to
pass that username in the Ansible command

```
ansible-playbook -i "1.2.3.4," install-docker.yml -u <username>
```
