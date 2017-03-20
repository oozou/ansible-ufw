ansible-ufw
========

Enables ufw firewall and sets rules to open up specified ports

Requirements
------------

Operating system that uses ufw.

Role Variables
--------------

* ufw_allowed_ports - list of port numbers to allow traffic in.

Example Playbook
-------------------------

The example below opens ports 22 (ssh), 80 (http) and 443 (https):

```yaml
- hosts: webservers
  roles:
    - role: ansible-ufw
      ufw_allowed_ports:
        - 22
        - 80
        - 443
```

Default Variables
-----------------

```
---
# defaults file for ansible-ufw
ufw_allowed_ports:
  - 22
  - 80
  - 443
```

AUTHOR
------

Rick Apichairuk
