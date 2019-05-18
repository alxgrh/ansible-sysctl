Sysctl
======

Role for manage sysctl rules.

Requirements
------------

Tested with Ansible 1.8.2

Role Variables
--------------

Sysctl parameters can be set as dictionary. Example:
 
     sysctl_rules:
       kernel.panic: 10
       vm.swappiness: 10
 
Error at setting non-existent sysctl keys might be ignored with:

     sysctl_ignore_key_errors: "yes" (default: yes)

Any errors might be ignored with:
     sysctl_ignore_all_errors: "yes" (default: no)


Dependencies
------------

None

Example Playbook
----------------

Example of usage:

    - hosts: servers
      roles:
         - { role: sysctl }

License
-------

MIT

Feedback, improvements, bugs
----------------------------

Please use [issues](https://github.com/alxgrh/ansible-sysctl/issues).
