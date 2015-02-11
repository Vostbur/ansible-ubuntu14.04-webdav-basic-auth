## Ansible playbook for start WebDAV server (dav module for Apache2) on Ubuntu

### Install Ansible

    sudo apt-add-repository -y ppa:ansible/ansible
    sudo apt-get update
    sudo apt-get install -y ansible


### Change /etc/ansible/hosts (for example - localhost)

    [local]
    localhost	ansible_connection=local

### Add roles folder to /etc/ansible/ansible.cfg (for example ~ = /home/ubuntu)

    ...
    roles_path     = /home/ubuntu/ansible/roles
    ...


### Choice username for basic authentication

    Change ansible/roles/apache2/vars/main.yml


### Run playbook

    ansible-playbook ansible/server.yml


* * *
####Links

1. [An Ansible Tutorial](https://serversforhackers.com/getting-started-with-ansible/) 
2. [How To Configure WebDAV Access with Apache on Ubuntu 12.04](https://www.digitalocean.com/community/tutorials/how-to-configure-webdav-access-with-apache-on-ubuntu-12-04)

* * *
_Tested on Ubuntu 14.04 server_
