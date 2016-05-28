### Ansible Workshop @ Geekybase based on Ubuntu
--------
- [Speaker Workshop Repo](https://github.com/winggundamth/ansible-workshop-01)
- [Speaker Galaxy Ansible](https://galaxy.ansible.com/winggundamth/)

### Install Ansible on MAC###

```sh
#  Install Brew http://brew.sh/
$ brew update
$ brew install ansible
```

### Install Ansible on Ubuntu###

```sh
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

### Check Ansible version

```sh
$ ansible --version
```

#### Install OpenSSH Server

```sh
sudo apt-get update
sudo apt-get install openssh-server
```

### Ansible Documents
- [Best Practices](http://docs.ansible.com/ansible/playbooks_best_practices.html)
- [Playbooks Variables](http://docs.ansible.com/ansible/playbooks_variables.html)
- [List of all modules](http://docs.ansible.com/ansible/list_of_all_modules.html)
- [Galaxy Ansible](https://galaxy.ansible.com/)

### Ansible Keywords
- playbook
- roles
  - tasks
  - handlers
  - defaults
  - templates - using [jinna2](http://jinja.pocoo.org/docs/dev/)

- inventories

- idempotent 
- var file

### Ansible Sturcture

```
├── Readme.md
├── inventories
│   └── wordpress
├── roles
│   ├── wordpress
│   │   ├── defaults
│   │   │   └── main.yml
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── tasks
│   │   │   ├── main.yml
│   │   │   ├── wordpress_install.yml
│   │   │   ├── wordpress_post.yml
│   │   │   └── wordpress_pre.yml
│   │   └── templates
│   │       └── wp-config.php.j2
│   └── wordpress-backup
│       ├── defaults
│       │   └── main.yml
│       └── tasks
│           └── main.yml
├── wordpress-backup.yml
└── wordpress.yml
```

### Ansible Commands

```sh
$ ansible-doc <module_name>

$ ansible-playbook -i inventories/wordpress --ask-pass wordpress.yml
$ ansible-playbook -i inventories/wordpress  --ask-sudo-pass wordpress.yml
$ ansible-playbook  -i inventories/wordpress wordpress.yml
$ ansible-playbook -v -i inventories/wordpress wordpress.yml

$ ansible-galaxy -p . install winggundamth.host_preparation
```
