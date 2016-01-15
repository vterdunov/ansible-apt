apt
=========
[![Build Status](https://travis-ci.org/vterdunov/ansible-apt.svg?branch=master)](https://travis-ci.org/vterdunov/ansible-apt)

Эта роль устанавливает пакеты с помощью apt.

Requirements
------------
None

Role Variables
--------------

```
apt_packages: []
apt_cache_valid_time: 1200
apt_state: latest
```

Dependencies
------------
None

Example Playbook
----------------
```
- hosts: all
  roles:
     - role: apt, apt_packages: git
```

Хорошей практикой будет задать список устанавливаемых пакетов в переменной `apt_packages` внутри `group_vars` или `host_vars`. Например:

```
---
apt_packages:
  - git
  - libmysqlclient-dev
  - libsqlite3-dev
  - mc
  - vim
```

Author Information
------------------
Разработано и протестировано для Ubuntu 14.04 (trusty)
