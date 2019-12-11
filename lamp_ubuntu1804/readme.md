# LAMP on Ubuntu 18.04

This playbook will install a LAMP environment (**L**inux, **A**pache, **M**ySQL and **P**HP) on an Ubuntu 18.04 machine, as explained in the guide on [How to Use Ansible to Install and Configure LAMP on Ubuntu 18.04](#). A virtualhost will be created with the options specified in the `vars/default.yml` variable file.

## Settings

- `mysql_root_password`: the password for the MySQL root account.
- `app_user`: a remote non-root user on the Ansible host that will own the application files.
- `http_host`: your domain name.
- `http_conf`: the name of the configuration file that will be created within Apache.
- `http_port`: HTTP port, default is 80.
- `disable_default`: whether or not to disable the default Apache website. When set to true, your new virtualhost should be used as default website. Default is true.


## Running this Playbook

Quickstart guide for those already familiar with Ansible:

### 1. Obtain the playbook
```shell
git clone https://github.com/do-community/ansible-playbooks.git
cd ansible-playbooks/lamp_ubuntu1804
```

### 2. Customize Options

```shell
nano vars/default.yml
```

```yml
---
mysql_root_password: "mysql_root_password"
app_user: "sammy"
http_host: "your_domain"
http_conf: "your_domain.conf"
http_port: "80"
disable_default: true
```

### 3. Run the Playbook

```command
ansible-playbook -l [target] -i [inventory file] -u [remote user] playbook.yml
```

For more information on how to run this Ansible setup, please check this guide: [soon]().