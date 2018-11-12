Role Name
=========

Sets a Static IP on the host. After this role is run a reboot is needed for the new settings to take effect

Requirements
------------

None

Role Variables
--------------

static_ip: "192.168.0.207" # IP You want the host to have
netmask: "255.255.255.0" # Subnet You want the host to have
gateway: "192.168.0.1" # Gateway IP You want the host to have



Example Playbook
----------------

---
# This playbook deploys the whole application stack in this site.

  - name: apply common configuration to all nodes
    hosts: 127.0.0.1
    connection: local
    become: yes
    become_user: root
    become_method: su

    roles:
      - set_static_ip


License
-------

BSD

Author Information
------------------

Michael McLean
haggistech@gmail.com