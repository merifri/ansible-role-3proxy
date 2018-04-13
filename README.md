3proxy Ansible Role
=========

Install 3proxy from source

Requirements
------------

None.

Role Variables
--------------

```
---
proxy_version: "0.8.11"
proxy_source: "https://github.com/z3APA3A/3proxy/archive/{{ proxy_version }}.tar.gz"

proxy_config_path: "/etc/3proxy"

proxy_socks_port: 1235
proxy_users: []
#- name: test
#  password: pass

proxy_dependencies:
- build-essential
- tar
- gzip
```

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: servers
  roles:
    - role: merifri.3proxy
      proxy_users:
      - name: test
        password: pAssw0rD
```

License
-------

MIT
