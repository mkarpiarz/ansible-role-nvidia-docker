uchida.nvidia-docker
====================

ansible role to install nvidia-docker and graphics driver

Role Variables
--------------

```
nvidia_docker_install_ppa_driver: False
nvidia_docker_driver_version: 375
nvidia_docker_deb_url: https://github.com/NVIDIA/nvidia-docker/releases/download/v1.0.1/nvidia-docker_1.0.1-1_amd64.deb
```

- `nvidia_docker_install_ppa_driver` is a variable whether install graphics driver from
  [Proprietary GPU Drivers PPA](https://launchpad.net/~graphics-drivers/+archive/ubuntu/ppa) or not,
  default is `False`, install from default repository
- `nvidia_docker_driver_version` is a variable to specify version for graphics driver,
  current default is `375`, but it will change in future release.
- `nvidia_docker_deb_url` is a variable to specify deb package url for nvidia-docker
  current default is `https://github.com/NVIDIA/nvidia-docker/releases/download/v1.0.1/nvidia-docker_1.0.1-1_amd64.deb`
  and it will change in future release.

Dependencies
------------

- [uchida.docker](https://galaxy.ansible.com/uchida/docker/): to install docker community edition

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
- hosts: servers
  roles:
     - role: uchida.nvidia-docker
```

License
-------

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed)

dedicated to public domain, no rights reserved.
