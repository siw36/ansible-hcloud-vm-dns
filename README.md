ansible_hcloud_vm_dns
=========

This role disables the automatic network configuration of a Hetzner Cloud VM and sets custom DNS servers.  
The original IPv4, IPv6 and MAC address will be kept.  

Requirements
------------

A user who can exec `sudo` commands without getting prompted for password confirmation.  

Role Variables
--------------

- `dns1`: the first DNS server. Default: `213.133.98.98`
- `dns2`: the second DNS server. Default: gets omitted
- `dns3`: the third DNS server. Default: gets omitted

Get this role
------------
```bash
ansible-galaxy install --roles-path ./roles/ siw36.ansible_hcloud_vm_dns
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  vars:
    dns1: 1.1.1.1
    dns2: 1.0.0.1
    dns3: 8.8.8.8
  - roles:
     - siw36.ansible_hcloud_vm_dns
```

License
-------

GNU General Public License v3.0

Author Information
------------------

Created by Robin 'siw36' Klussmann (08/2019)
