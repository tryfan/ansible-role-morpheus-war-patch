Morpheus WAR Patch
=========

This role will patch the Morpheus UI WAR file with one provided by Morpheus.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

|Variable|Required|Default|Description|
|--------|--------|-------|-----------|
mwp_morpheus_dir|Y|`/opt/morpheus`|Morpheus install directory|
mwp_morpheus_war_dir|Y|`"{{ mwp_morpheus_dir }}/lib/morpheus"`|Morpheus WAR directory|
mwp_war_temp_file|Y|`"{{ mwp_morpheus_war_dir }}/morpheus-ui.war.new"`|Complete path for temp file|
mwp_remote_war_url|Y|``|URL of patched WAR file|
mwp_morpheus_owner|Y|`morpheus-app`|Morpheus file owner|
mwp_morpheus_group|Y|`morpheus-app`|Morpheus group|

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: patches
      become: true
      roles:
         - { role: ansible-role-morpheus-war-patch, mwp_remote_war_url: 'URL GOES HERE' }

License
-------

MIT

Author Information
------------------

Nick Celebic
Morpheus Data
