# RTPEngine initialize
Auto build,deploy rtpengine with ansible. ![Version](https://img.shields.io/github/v/release/mach1el/ansible-role-rtpengine?color=blue&style=plastic) ![License](https://img.shields.io/github/license/mach1el/ansible-role-rtpengine?color=grey&style=plastic)

## Role variables
See [`default/main.yml`](https://github.com/mach1el/ansible-role-rtpengine/blob/master/defaults/main.yml)

Some variables that you may want to change

* `rtpengine_interface` 
* `rtpengine_listen_host`
* `rtpengine_listen_ng_port`
* `rtpengine_listen_tcp_port`
* `rtpengine_port_min`
* `rtpengine_port_max`

## Role tree

```
├── defaults
│   └── main.yml
├── handlers
│   └── main.yml
├── tasks
│   ├── configure.yml
│   ├── main.yml
│   ├── setup_bcg.yml
│   ├── setup_debian.yml
│   └── setup_rtpengine.yml
└── templates
    ├── rtpengine.conf.j2
    └── rtpengine-recording.conf.j2
```

## Example playbook

```
---
- name: Initialize RTPEngine
  hosts: all
  become: true
  roles: 
    - 'ansible-role-rtpengine'
```
