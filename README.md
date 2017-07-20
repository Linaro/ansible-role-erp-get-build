ERP Get Build
=============

Download an Enterprise Reference Platform (ERP) release.

By default, this role will discover the latest staging ERP build from jenkins,
set 'erp_latest_build' number, and download the build to ./builds/staging/.

Role Variables
--------------

In:

| variable | description | default
|----------|-------------|---------
| erp_debian_installer_environment | [staging|release] | staging

Out:

| variable | description | example
|----------|-------------|---------
| erp_latest_build | Latest build number, based on debian_installer_environment | 430

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: get_erp_build

License
-------

BSD

Author Information
------------------

Dan Rue <dan.rue@linaro.org>
