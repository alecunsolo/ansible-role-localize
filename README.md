[![build status](https://github.com/alecunsolo/ansible-role-localize/actions/workflows/ci.yml/badge.svg)](https://github.com/alecunsolo/ansible-role-localize/actions/workflows/ci.yml)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit)](https://github.com/pre-commit/pre-commit)

Ansible Role: localize
=========
## DISCLAIMER
After [this](https://www.redhat.com/en/blog/furthering-evolution-centos-stream) announcement I will not test on RHEL anymore.

---------
This role configure the system-wide locale

Requirements
------------

None.

Role Variables
--------------

```yaml
locale_packages: locales or glibc-locale-source
```
This is the name of the package containing the locales sources. It is different for EL and Debian.

```yaml
config_system_locale: en_US.UTF-8
```
This is the default locale value

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: alecunsolo.localize, config_system_locale: 'it_IT.UTF-8' }

License
-------

MIT

Notes
-----

Testing with molecule (including the docker images used) is ~~stolen from~~ heavily inspired by [Jeff Geerling](https://www.jeffgeerling.com/). Watch [his video](https://youtu.be/FaXVZ60o8L8) (and the other ones as well).
