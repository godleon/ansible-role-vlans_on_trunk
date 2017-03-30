[![Build Status](https://travis-ci.org/godleon/ansible-role-vlans_on_trunk.svg?branch=master)](https://travis-ci.org/godleon/ansible-role-vlans_on_trunk)


Role Name
=========

**godleon.vlans_on_trunk**

Requirements
------------

The target machine is going to be provisioned should have a NIC be attached to a trunk port with multiple VLANs on switch.


Role Variables
--------------

The variables that should be passed to this role and a brief description about them are as follows:

```yaml
# Specify the trunk interface name.
vlan_on_trunk_TrunkInterfaceName: 'eth1'

# Specify the vlan networking information.
# Just leave the gateway configuration to be blank if you don't need it.
vlan_on_trunk_MultiVlanConfig:
  - { 'vlan_id': 121, 'ip': '10.12.1.254', 'netmask': '255.255.255.0', 'gateway': '' }
  - { 'vlan_id': 122, 'ip': '10.12.2.254', 'netmask': '255.255.255.0', 'gateway': '' }
  - { 'vlan_id': 123, 'ip': '10.12.3.254', 'netmask': '255.255.255.0', 'gateway': '' }
```


Dependencies
------------

None


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - godleon.vlans_on_trunk

License
-------

MIT

Author Information
------------------

**Leon Tseng** 

-  ([godleon@GitHub](https://github.com/godleon))
