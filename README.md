# DO Community - Ansible Playbooks

A collection of minimalist Ansible playbooks for automating server setups, based on DigitalOcean's Community guides.

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

## Documentation

To use the automation provided by these playbooks, you first need to install Ansible on a control node
and configure it to connect to your remote hosts using SSH keys. To set this up, please follow the guide on [How to Install and Configure Ansible on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-18-04).

Guides covering these playbooks:

 - [How to use Ansible to Automate Initial Server Setup on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-automate-server-setup-with-ansible-on-ubuntu-18-04)
 - [How to Use Ansible to Install and Set Up Docker on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-install-and-set-up-docker-on-ubuntu-18-04)
 - [How to Use Ansible to Install and Set Up LEMP on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-install-and-set-up-lemp-on-ubuntu-18-04) *soon*

