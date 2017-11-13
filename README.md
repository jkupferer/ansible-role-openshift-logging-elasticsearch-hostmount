Role Name
=========

An Ansible role for configuring hostmount for the OpenShift logging elasticsearch database.

Installation
------------

```
ansible-galaxy install https://github.com/jkupferer/ansible-role-openshift-logging-elasticsearch-hostmount/archive/master.tar.gz#/openshift-logging-elasticsearch-hostmount
```

Requirements
------------

OCP 3.3+

Role Variables
--------------

* `openshift_hosted_logging_elasticsearch_hostmount_path` - Host path for
  elasticsearch storage

* `openshift_hosted_logging_elasticsearch_nodeselector` - Node selector for
  elasticsearch placement (ex: "region=infra")

* `openshift_logging_es_nodeselector` - Node selector for elasticsearch
  placement in object format (ex: {"region": "infra"})

Settings for managing hostmount path configuration:

* `openshift_hosted_logging_elasticsearch_hostmount_path_owner`: default 1000
* `openshift_hosted_logging_elasticsearch_hostmount_path_group`: default 0
* `openshift_hosted_logging_elasticsearch_hostmount_path_mode`: default ug=rwx,o=

Example Playbook
----------------

    - hosts: masters[0]
      roles:
         - role: openshift-logging-elasticsearch-hostmount

License
-------

BSD

Author Information
------------------

Johnathan Kupferer (jkupfere@redhat.com)
