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
| erp_debian_installer_environment | [staging\|stable] | staging
| erp_build_number | ERP build to retrieve. | Defaults to false, in which case it will be set to the latest build number.

Out:

| variable | description | example
|----------|-------------|---------
| erp_build_number | Latest build number, based on erp_debian_installer_environment | 430

For convenience with ansible-role-mr-provisioner, this role will also set the
following variables:
- mr_provisioner_kernel_description: i.e. "debian-installer staging build 495"
- mr_provisioner_initrd_description: i.e. "debian-installer staging build 495"
- mr_provisioner_kernel_path: i.e. "./builds/debian-staging/495/linux"
- mr_provisioner_initrd_path: i.e. "./builds/debian-staging/495/initrd.gz"


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
