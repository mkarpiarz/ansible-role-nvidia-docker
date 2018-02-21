uchida.nvidia-docker
====================

ansible role to install nvidia-docker and graphics driver

Role Variables
--------------

```
nvidia_docker_version: 1.0.1
```

- `nvidia_docker_version` is a variable to specify which version of nvidia-docker, current default value is `1.0.1`

Dependencies
------------

- [uchida.docker](https://galaxy.ansible.com/uchida/docker/): to install docker community edition
- [uchida.nvidia-driver](https://galaxy.ansible.com/uchida/nvidia-driver/): to install NVIDIA Graphics driver
  you may want to select APT repository and driver version, consult README for this role

Example Playbook
----------------

install nvidia-docker:

```
- hosts: servers
  roles:
    - role: uchida.nvidia-docker
```

install nvidia-docker version 2.0.2:

```
- hosts: servers
  roles:
    - role: uchida.nvidia-docker
      nvidia_docker_version: 2.0.2
```

License
-------

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed)

dedicated to public domain, no rights reserved.
