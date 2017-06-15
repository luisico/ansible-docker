Docker
======
Install Docker.

Docker is installed from packages available in Docker's CE Stable package repository.

User namespaces can be optionally activated with variable `docker_user_namespace`. This might require regenerating the GRUB configuration and in turn restarting the server. A standard dorremap user will also be added to `/etc/subuid` and `/etc/subgid`.

A list of environment variables can be added to Docker's systemd service using `docker_env`.

Requirements
------------
See `meta/main.yml`.

Role Variables
--------------
See `defaults/main.yml`.

Dependencies
------------
None.

Example Playbook
----------------
Example:
```
- hosts: servers
  roles:
    - docker
```

TODO
----
- Install specific version
- Support docker-ee

License
-------
Licensed under [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).

Author Information
------------------
Luis Gracia while at [EMBL-EBI](http://www.ebi.ac.uk/):
- luis.gracia [at] ebi.ac.uk
- GitHub at [luisico](https://github.com/luisico)
- Galaxy at [luisico](https://galaxy.ansible.com/luisico)
