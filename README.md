Create AMI
==========

Small rol to deploy a new AMI with a specific format

Requirements
------------

The role uses the EC2 module

Role Variables
--------------

Settable variables that are in defaults/main.yml.

* `environment` : PRO/PRE/DEV
* `projectname` : Name of the project
* `version`     : Version of the AMI
* `region`      : AWS region
* `ec2_id`      : AWS EC2 instance ID

Those three variables are defined in case you use the default new ami name (shown below), if you specify another new_ami_name you can ignore them.

* `new_ami_name`: Name of the new AMI, by default it looks similar to `PRE-PortalASG-v8.18.81-2017-02-07T12-43-18Z`

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
