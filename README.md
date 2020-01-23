# ansible-role-openldap
Role to install openldap (optionally with phpldapadmin and optionally restore a backup .ldif) on Enterprise Linux

Requirements
------------

An already provisioned machine with Centos7 or RHEL7 ( not tested )

Role Variables
--------------
    ds_base_suffix: "dc=subdomain,dc=example,dc=com"
    root_dn_cn: Manager
    install_phpldapadmin: false
    openldap_admin_password: 12345678
    backup_file_path: UNDEFINED
    
Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: ldapserver
      become: True
      vars:
        install_phpldapadmin: true
        ds_base_suffix: "dc=example,dc=com"
        openldap_admin_password: shouldbevaulted
        backup_file_path: /tmp/restore.ldif
      roles:
        - openldap

License
-------

BSD

Author Information
------------------

Henk den Hartog

