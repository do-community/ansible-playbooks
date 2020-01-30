# DO Community - Ansible Playbooks

A collection of minimalist Ansible playbooks for automating server setups, based on DigitalOcean's Community guides.

- [Initial Server Setup for Ubuntu 18.04](https://github.com/do-community/ansible-playbooks/tree/master/setup_ubuntu1804) *
- [Apache on Ubuntu 18.04](https://github.com/do-community/ansible-playbooks/tree/master/apache_ubuntu1804)
- [LEMP on Ubuntu 18.04](https://github.com/do-community/ansible-playbooks/tree/master/lemp_ubuntu1804)
- [LAMP on Ubuntu 18.04](https://github.com/do-community/ansible-playbooks/tree/master/lamp_ubuntu1804)
- [WordPress with LAMP on Ubuntu 18.04](https://github.com/do-community/ansible-playbooks/tree/master/wordpress-lamp_ubuntu1804)
- [Docker on Ubuntu 18.04](https://github.com/do-community/ansible-playbooks/tree/master/docker_ubuntu1804)

_\*the Initial Server Setup should be your starting point for fresh servers._

## Playbook Structure

The playbooks contained in this repository were created for educational purposes, and should serve as a base for you to create your own playbooks and roles.

Although we opt to not use roles, our playbooks follow a distinctive structure to facilitate reuse while keeping them mostly self-contained and straightforward.

For instance, this is how the `lemp` playbook is structured:

```
lemp_ubuntu1804
├── files
│   ├── info.php.j2
│   └── nginx.conf.j2
├── vars
│   └── default.yml
├── playbook.yml
└── readme.md
```


- `files/`: directory containing templates and other files required by the playbook.
- `vars/`: directory to save variable files. A `default.yml` var file is included by default.
- `playbook.yml`: the playbook file.
- `readme.md`: instructions and links related to this playbook.

## Getting Started

To set up your Ansible environment, please follow our guide on [How to Install and Configure Ansible on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-18-04).

### Connection Test

From your local machine or Ansible control node, run:

```command
ansible all -m ping -u remote_user
```

If you're able to get a "pong" reply back from your node(s), your setup works as expected and you'll be able to run both ad-hoc commands and playbooks on your nodes, using Ansible.

## Guides

The following guides cover how to use the playbooks you'll find in this repository.

### Initial Server Setup

- [Initial Server Setup for Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-18-04)

Once you have executed the initial server setup, you can choose from any of the available server setup playbooks:

### Web Servers
- [Apache on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-install-and-set-up-apache-on-ubuntu-18-04)
- [LEMP (Linux, Nginx, MySQL, PHP) on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-install-and-set-up-lemp-on-ubuntu-18-04)
- [LAMP (Linux, Apache, MySQL, PHP) on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-install-and-set-up-lamp-on-ubuntu-18-04)

### Applications & CMSs

- [WordPress with LAMP on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-install-and-set-up-wordpress-with-lamp-on-ubuntu-18-04)

### Containers & K8s
- [Docker on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-install-and-set-up-docker-on-ubuntu-18-04)

