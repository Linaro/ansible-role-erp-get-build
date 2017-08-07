ERP Get Build
=============

Download an Enterprise Reference Platform (ERP) release.

By default, this role will discover the latest staging ERP build from jenkins,
set 'erp_build_number' number, and download the build to ./builds/staging/.

Role Variables
--------------

In:

| variable | description | default
|----------|-------------|---------
| erp_debian_installer_environment | [staging|stable] | staging
| erp_build_number | ERP build to retrieve. | Defaults to false, in which case it will be set to the latest build number.

Out:

| variable | description | example
|----------|-------------|---------
| erp_build_number | Latest build number, based on erp_debian_installer_environment | 430

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: Linaro.erp-get-build

License
-------

BSD

Author Information
------------------

Dan Rue <dan.rue@linaro.org>
