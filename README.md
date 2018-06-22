# docker

Ansible role to install and configure docker.

Inspired by https://docs.docker.com/engine/installation/linux/docker-ce/debian/#install-using-the-repository

## Requirements

A host capable to run docker.

## Role Variables

Finding latest docker_compose version from github releases page is not trivial ! So we use this variable :
- docker_compose_version.
  This should be set via parameters to the role or the global scope (ie. hostvars, group vars, etc.).

## Dependencies

None.

## Install this role as submodule in a git repository

`git submodule add https://github.com/mbocquet/docker.git roles/docker`

## Example Playbook

    - hosts: servers
      roles:
         - { role: docker, docker_compose_version: '1.15.0' }

or if docker_compose_version is defined elsewhere :

    - hosts: servers
      roles:
         - docker

## License

GPLv3

## Author Information

http://www.sekoya.org
