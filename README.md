Enix/mariadb for Ansible
=================

A role for deploying and configuring [mariadb](http://mariadb.org) on unix hosts using [Ansible](http://www.ansible.com/).


Requirements
------------

Supported targets:

- Ubuntu 16.04 "Xenial"
- Debian 8 "Jessie"
- Debian 9 "Stretch"
- ...


Role Variables
--------------

This roles comes preloaded with almost every available default. You can override each one in your hosts/group vars, in your inventory, or in your play. See the annotated defaults in `defaults/main.yml` for help in configuration. All provided variables start with `mariadb__`.

- `mariadb__extra_packages` - List of extra packages to install (like plugins, ...), `default: []`.

Dependencies
------------

- None

Extra
-----

Callable tasks:

- `task`: ...


Usage
-----

Clone this repo into your roles directory:

    $ git clone https://gitlab.enix.org/ansible/ansible-mariadb.git roles/mariadb

Or use Ansible galaxy requirements.yml

And add it to your play's roles:

    - hosts: servers
      roles:
        - role: mariadb:
          mariadb__root_password='secret'


You can also use the role as a playbook. Asked which hosts to provision, and you can further configure the play by using `--extra-vars`.

    $ ansible-playbook -i inventory --extra-vars='{...}' main.yml


Still to do
-----------

- Add support for upstream or default distribution versions
- Add support for automysqlbackup

Changelog
---------

### 0.1

Initial version.

License
-------

GPL

Author Information
------------------

Laurent CORBES <laurent.corbes@enix.fr> - http://www.enix.fr