Docker
======
Install Docker.

Docker is installed from packages available in Docker's CE Stable package repository. For Centos, the `centos-extra` repository must be enabled. For Red Hat, `centos-extra` needs to be also added, including Centos GPG key. These dependencies are not included in this role. The latest docker version found in the repository is installed unless it is overridden with `docker_version`. Same version will be installed for docker engine and docker cli.

User namespaces can be optionally activated with variable `docker_user_namespace` (default is `no`). This might require regenerating the GRUB configuration and in turn restarting the server. A standard dorremap user will also be added to `/etc/subuid` and `/etc/subgid`.

A list of environment variables can be added to Docker's systemd service using `docker_env`.

Requirements
------------
See `meta/main.yml`.

Role Variables
--------------
See `defaults/main.yml`.

Dependencies
------------
`centos-extra` repository is needed for CentOS and Red Hat (see above).

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
- Support docker-ee
- Make sure docker service is restarted after firewalld service, if firewalld is active
- Install bash completion for docker-compose

License
-------
Released under the [MIT license](https://opensource.org/licenses/MIT).

Author Information
------------------
Luis Gracia while at [EMBL-EBI](http://www.ebi.ac.uk/):
- luis.gracia [at] ebi.ac.uk
- GitHub at [luisico](https://github.com/luisico)
- Galaxy at [luisico](https://galaxy.ansible.com/luisico)
