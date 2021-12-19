graylog-collector
=========

Ansible role to install and configure the Graylog sidecar and NXLog

Supported platforms
------------

##### Debian
*  buster (10)
*  bullseye (11)

##### Ubuntu
*  focal (20.04)

Role Variables
--------------

Please see a file: defaults/main.yml

You can also use tags: 

*  __install__ - only install packages and services
*  __configure__ - сonfigure graylog-sidecar and NXLog to send to your Graylog server
*  __check_services__ - сheck the status of services

Dependencies
------------

* None

Example Playbook
----------------

    - name: Deploy graylog-collector role
      roles:
        - graylog-collector
      vars:
        graylog_sidecar_server_url: http://192.168.0.1:9000/api/
        graylog_sidecar_server_api_token: j3pqlka8kktlgggat0man
        nxlog_journalctl_PRIORITY: 0..7

License
-------

MIT

Author Information
------------------

Aleksandr Anishchenko
