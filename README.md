# ansible-role-autossh
Role for installing, configuring and enabling a persistent ssh tunnel using autossh

[![license](https://img.shields.io/github/license/petalmd/ansible-role-autossh.svg)](https://github.com/petalmd/ansible-role-autossh)

Tested only on Centos7

## Installation
```
$ ansible-galaxy install petalmd.autossh
```

## Features
- Supports local and remote port forwarding 
- Creates the system daemon 

## Getting started
```
---
- name: Redis Server
  hosts: redis
  roles:
    - { role: autossh, autossh_daemon_name: autossh-redis-tunnel.service, autossh_daemon_description: redis-ssh-replication, autossh_server_ip: a.b.c.d, autossh_local_or_remote_switch: L, autossh_to_port: 6379, autossh_from_port: 6380}
    - redis
```

## Contributing
Contributions, questions, and comments are all welcomed and encouraged!

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Credits

- [Julien Vigneux-Salesse](https://github.com/jvigneux)
