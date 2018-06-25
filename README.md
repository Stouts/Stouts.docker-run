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

docker_run_mounts: []
docker_run_volumes: []
docker_run_logins: []
docker_run_networks: []
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

