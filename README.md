Ansible Blackbox Exporter
=========

This role installs the prometheus blackbox-exporter.
The exporter will be run as systemd service with it's own user and Group.
The default is listening on 127.0.0.1:9115.

Requirements
------------

- Ansible >= 2.9, may work with other versions, but no guarantee

Role Variables
--------------

All variables can be found at `defaults/main.yml`.

For making the exporter accessible from outside, you need to change the value of blackbox_exporter_web_listen_address:

    blackbox_exporter_web_listen_address: "0.0.0.0:9115"

For better understanding of the configuration, check out the blackbox-exporter documentation:  
https://github.com/prometheus/blackbox_exporter

Example Playbook
----------------

    - hosts: blackbox_exporter
      roles:
         - { role: kornkalle.ansible_blackbox_exporter }

License
-------

MIT

Author Information
------------------

Nils Berg

-   nils.berg [at] helmholtz-berlin.de
-   nils [at] kulturkosmos.de
