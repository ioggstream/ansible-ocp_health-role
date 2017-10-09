Role Name
=========

Basic Openshift 3.4 health checks

Requirements
------------

Openshift Ansible

Role Variables
--------------

- ocp_version: set it to the expected OCP version. It will be checked against `openshift version` output. Default is "" that won't check the version.

```
ocp_version: "3.4.1.44.11"
```

- create_test_project: if `true` will create the `ocp-health` project (if not present) with two app from ocp examples:
    
    * cakephp-mysql with ephemeral volume
    * django-psql-persistent with a pgsql persistent volume
  
  Default is `false`, which won't create anything.

```
create_test_project: false
```

Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: nodes
      roles:
         - role: ioggstream.ocp_health
           create_test_project: false


You'll find this sample playbook under `tests/ocp_health.yml`

License
-------

BSD

Author Information
------------------

Roberto Polli @ioggstream

