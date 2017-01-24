Create AMI
==========

Small rol to deploy a new AMI with a specific format

Requirements
------------

The role uses the EC2 module

Role Variables
--------------

Settable variables that are in defaults/main.yml.

* environment : PRO/PRE/DEV
* projectname : Name of the project
* version     : Version of the AMI
* region      : AWS region
* ec2_id      : AWS EC2 instance ID

Example Playbook
----------------

It assumes you use the ec2 dynamic inventory

```yaml
- hosts: localhost
  connection: local
  gather_facts: no
  roles:
    - role: create-ami
```

License
-------

GPL
