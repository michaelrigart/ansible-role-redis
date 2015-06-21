Ansible Redis Role
===================
[![Build Status](https://semaphoreci.com/api/v1/projects/088fd973-2e31-4a64-ad77-2fe575850083/461775/badge.svg)](https://semaphoreci.com/michaelrigart/ansible-role-redis) [![Build Status](https://travis-ci.org/michaelrigart/ansible-role-redis.svg?branch=master)](https://travis-ci.org/michaelrigart/ansible-role-redis)

An ansible role for installing Redis from the official Ubuntu repo or from a ppa
 
Role Variables
--------------

```yaml
redis_ppa: define the ppa you wish to install from.
redis_update_kernel: define if you want update the kernel for vm overcommit
redis_service_state: indicates the service state; Allowed setting: started, stopped
redis_service_enabled: indicates if service needs to be enabled on boot; Allowed settings: yes, no
redis_conf: dictionary with all needed configuration parameters. This is a dictionary where the key / value pairs are used. In some cases, a key can hold a list. See defaults for a better example
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - { role: MichaelRigart.redis, sudo: Yes }
```

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>