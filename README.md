uchida.nvidia-docker
====================

ansible role to install nvidia-docker and graphics driver

Role Variables
--------------

```
nvidia_docker_deb_url: https://github.com/NVIDIA/nvidia-docker/releases/download/v1.0.1/nvidia-docker_1.0.1-1_amd64.deb
```

- `nvidia_docker_deb_url` is a variable to specify deb package url for nvidia-docker
  current default is `https://github.com/NVIDIA/nvidia-docker/releases/download/v1.0.1/nvidia-docker_1.0.1-1_amd64.deb`
  and it will change in future release.

Dependencies
------------

- [uchida.docker](https://galaxy.ansible.com/uchida/docker/): to install docker community edition
- [uchida.nvidia-driver](https://galaxy.ansible.com/uchida/nvidia-driver/): to install NVIDIA Graphics driver
  you may want to select APT repository and driver version, consult README for this role

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
