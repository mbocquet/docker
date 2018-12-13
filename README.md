# docker

Ansible role to install and configure docker.

Inspired by https://docs.docker.com/engine/installation/linux/docker-ce/debian/#install-using-the-repository

## Requirements

A host capable to run docker.

## Role Variables

* docker_compose_version.
  Getting latest docker_compose version from github releases page is not
  trivial but can be found by parsing the following URL's **<title>** HTML tag.
  https://github.com/docker/compose/releases/latest

The latest version is guessed at runtime unless docker_compose_version is
defined with a valid version which should be set via parameters to the role or
the global scope (ie. inline, hostvars, group vars, etc.).

## Dependencies

None.

## Install this role as submodule in a git repository

`git submodule add https://github.com/mbocquet/docker.git roles/docker`

## Example Playbook

    - hosts: docker
      roles:
         - { role: docker, docker_compose_version: '1.15.0' }

If docker_compose_version is defined elsewhere or to let the role guess and
fetch the latest version at runtime :

    - hosts: docker
      roles:
         - docker

## License

GPLv3

## Author Information

http://www.sekoya.org
