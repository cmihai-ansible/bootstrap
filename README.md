Role Name
=========

bootstrap

[![Build Status](https://travis-ci.org/cmihai-ansible/bootstrap.svg?branch=master)](https://travis-ci.org/cmihai-ansible/bootstrap)

Ansible galaxy:
---------------

[https://galaxy.ansible.com/crivetimihai/bootstrap](https://galaxy.ansible.com/crivetimihai/bootstrap)

```bash
ansible-galaxy install crivetimihai.bootstrap
```

Requirements
------------

- For RHEL, a Red Hat subscription or functional local repository.

Role Variables
--------------

```yaml
bootstrap_remove_packages: true
bootstrap_enable_service: true
bootstrap_enable_selinux: true
bootstrap_firewall_configure: true
bootstrap_firewall_rules:
  - service:
```

Dependencies
------------

- For Red Hat, subscription-manager.

Example Playbook
----------------

```yaml
---
- name: Install bootstrap on localhost
  hosts:
    - localhost
  connection: local

  tasks:
    - name: bootstrap is configured
      import_role:
        name: crivetimihai.bootstrap
      vars:
        bootstrap_remove_packages: true
        bootstrap_enable_service: true
        bootstrap_firewall_configure: true
        bootstrap_firewall_rules:
          - service:
      tags: bootstrap
```

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/crivetimihai/)
