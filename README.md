Ansible role to install Log.io
============================


Requirements
-----------
## Requirements

- Ansible 2.1


Dependencies
-----------

Steamulo npm install role


Description
-----------

This role will assume the setup of log.io

Role Variables
--------------


    # User
    elao_logio_user: root
    elao_logio_npm_prefix: /usr

    # Config
    elao_logio_config_dir:     ~/.log.io
    elao_logio_config_harvester: []

    elao_logio_logserver_bind_address: "0.0.0.0"
    elao_logio_logserver_host: "0.0.0.0"
    elao_logio_logserver_port: 28777

    elao_logio_webserver_host: "0.0.0.0"
    elao_logio_webserver_port: 28778
    #elao_logio_webserver_auth_login:
    #elao_logio_webserver_auth_pass:

    #elao_logio_webserver_ssl_key: /path/to/certificate.pem
    #elao_logio_webserver_ssl_cert: /path/to/privatekey.pem

    #elao_logio_webserver_restrictsocket: "*:*"

    #elao_logio_webserver_restrictshttp: [ "192.168.29.39", "10.0.*" ]

Example Playbook
----------------
    - hosts: servers
      vars:
        elao_logio_config_harvester:
            - nodeName: NodeXXX
            - logStreams:
              - syslog:
                - "/var/log/auth.log"
                - "/var/log/kern.log"
      roles:
         - { role: steamulo.logio }

License
-------


Author Information
------------------

STEAMULO - http://www.steamulo.com