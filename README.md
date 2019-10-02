Ansible role role-lvm-partitionner
==========================

A role to handle partitioning, VG & LV creation, formatting and mounting

Requirements
------------

This role is using lvm and parted ansibles modules. It requires the parted and lvm-tools system packages are available
on target system but it does **not** install them by itself.

So it's up to the calling playbook to ensure these prerequisites are filled.


Role Variables
--------------

The role expects a complex data structure stored in a variable ```lvm_disk```:

```yaml
  lvm_disk:
    device: '/dev/sdb2'
    lvm_vg: 'vg_data'
    partitions:
    - name: 'logw'
      mountpoint: '/var/log'
      filesystem: 'xfs'
      size: 10G
```

Dependencies
------------

No dependencies for this role

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
    - hosts: servers
      roles:
      - { role: username.rolename, x: 42 }
```

License
-------

GPLv2

Author Information
------------------

Initial write by Eric Belhomme <ebelhomme@fr.scc.com> (2018), released under the terms of GPLv2 license