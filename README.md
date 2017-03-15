# docker-install-demo
When you need to run Docker containers in a cloud that does not natively support container orchestration, you can install Docker engine yourself on a VM that is running in the cloud.

Docker installation can be done with the default package managers of Linux distros, but that will often result in quite old version and therefore it is better to do a manual installation. And example of such manual installation is the Ansible playbook in this docker-install-demo repository. The playbook installs the latest Docker engine on Ubuntu 16.04. Pre-requirement is that you are familiar with using Ansible and have the Ansible client installed on the workstation that you are working on.

Example command to execute the playbook against host 11.22.33.44, after you have cloned the Git repository to your workstation:
```
ansible-playbook -i "11.22.33.44," install-docker.yml
```

After installation, open a new SSH session to the VM as user "ubuntu" and verify that the Docker engine works by running command `docker run hello-world`. That should result output `Hello from Docker`.
