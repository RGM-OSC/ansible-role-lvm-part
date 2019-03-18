Role Name
=========

A role to handle partitioning, VG & LV creation, formatting and mounting

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

  lvm_disk:
    device: '/dev/sdb2'
    lvm_vg: 'vg_data'
    partitions:
    - name: 'logw'
      mountpoint: '/var/log'
      filesystem: 'xfs'
      size: 10G

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

GPLv2

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
