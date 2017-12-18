hxpro.adminer
===============

Database management in a single PHP file

Requirements
------------

CentOS 7

Role Variables
--------------

    adminer_server_name: localhost
    adminer_version: 4.3.1
    adminer_design: price
    adminer_language: en
    adminer_ssl_cert: /path/to/ssl/cert.pem
    adminer_ssl_key: /path/to/ssl/key.pem
    adminer_install_path: /var/www/html/adminer
    adminer_phpfpm_listen: "{{ phpfpm_default_listen }}"
    adminer_allow_from:
      - 127.0.0.1

Dependencies
------------

 - hxpro.nginx

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: hxpro.adminer
          adminer_server_name: adminer.example.com
          adminer_design: price
          adminer_version: 4.3.1
          adminer_install_path: /var/www/html/adminer
          adminer_allow_from:
            - 192.168.1.0/24

License
-------

WTFPL

Author Information
------------------

Matěj Koudelka <matej@hxpro.cz>
