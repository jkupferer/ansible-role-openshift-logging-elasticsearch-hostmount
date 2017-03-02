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

OCP 3.3 or 3.4

Role Variables
--------------

* `openshift_hosted_logging_elasticsearch_hostmount_path` - Host path for elasticsearch

* `openshift_hosted_logging_elasticsearch_nodeselector` - Node selector for cassandra placement

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
