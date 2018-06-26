Stouts.docker-run
=================

Ansible role to run Docker containers

Features:

* Create and bind filesystem mounts
* Create and bind docker volumes
* Login into Docker registries
* Create docker networks
* Run/update/remove docker containers

#### Variables

```yaml
# Create Docker Mounts on Host
docker_run_mounts: []

# Create Docker Volumes
docker_run_volumes: []

# Login into Docker Registries
docker_run_logins: []

# Create Docker Networks
docker_run_networks: []

# Copy files on Docker Host
docker_run_copy: []

# Run Docker Containers
docker_run_containers: []
```

#### Usage

Add `Stouts.docker-run` to your roles and set vars in your playbook file.

Example:

```yaml

- hosts: all

  roles:
  - Stouts.docker-run

  vars:
    docker_run_mounts: /opt/storage
    docker_run_networks:
    - mynetwork
    docker_run_containers:
    - name: redis
```

#### License

Licensed under the MIT License. See the LICENSE file for details.

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Stouts/Stouts.docker-run/issues)!

