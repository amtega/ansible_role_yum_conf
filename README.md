# Ansible amtega.yum_conf role

This is an [Ansible](http://www.ansible.com) role configure yum.conf and dnf.conf options

## Requirements

[Ansible 2.7+](http://docs.ansible.com/ansible/latest/intro_installation.html)

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Tests


## Dependencies


## Usage

This is an example playbook:

```yaml
---
- hosts: all
  gather_facts: yes
  roles:
    - role: amtega.yum_conf
      vars:
        yum_conf_options:
          - option: logfile
            value: /var/log/yum.log
            state: present
          - option: gpgcheck
            value: 0
            state: present
          - option: cachedir
            value: /var/cache/yum/$basearch/$releasever
            state: absent

```

## Testing

Tests are based on [molecule with docker containers](https://molecule.readthedocs.io/en/latest/installation.html).

```shell
cd amtega.yum_conf

molecule test
```
## License

Copyright (C) <!-- YEAR --> AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Carlos Chedas Fernandez.
