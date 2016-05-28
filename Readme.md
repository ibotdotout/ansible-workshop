### Ansible
--------
[Author Workshop Repo](https://github.com/winggundamth/ansible-workshop-01)

ubuntu password - `ansibleclass`

# Ansible Documents
[Playbooks Variables](http://docs.ansible.com/ansible/playbooks_variables.html)
[List of all modules](http://docs.ansible.com/ansible/list_of_all_modules.html)

# Ansible Keywords
tasks
roles
playbook

inventories

** idempotent 

handlers

templates - using [jinna2](http://jinja.pocoo.org/docs/dev/)

# Ansible Commnad

```sh
$ ansible-doc <module_name>

$ ansible-playbook -i inventories/wordpress --ask-pass wordpress.yml
$ ansible-playbook -i inventories/wordpress  --ask-sudo-pass wordpress.yml
$ ansible-playbook  -i inventories/wordpress wordpress.yml
$ ansible-playbook -v -i inventories/wordpress wordpress.yml
```
# Other command

```sh
$ debconf
```
