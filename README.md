Ansible Redis Role
===================

An ansible role for installing Redis from the official Ubuntu repo or from a ppa
 

Role Variables
--------------

    redis_ppa: define the ppa you wish to install from.
    redis_update_kernel: define if you want update the kernel for vm overcommit
    redis_service_state: indicates the service state; Allowed setting: started, stopped
    redis_service_enabled: indicates if service needs to be enabled on boot; Allowed settings: yes, no
    redis_conf: dictionary with all needed configuration parameters. This is a dictionary where the key / value pairs
     are used. In some cases, a key can hold a list. See defaults for a better example

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: MichaelRigart.redis }

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>