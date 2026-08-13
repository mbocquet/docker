# docker

Ansible role to install and configure docker.

Inspired by https://docs.docker.com/engine/installation/linux/docker-ce/debian/#install-using-the-repository

## Requirements

A host capable to run docker.

## Role Variables

None.

## Dependencies

None.

## Install this role as submodule in a git repository

```sh
git submodule add https://git.sekoya.org/mb/docker.git roles/docker
```

## Example Playbook

    - hosts: docker
      roles:
         - docker

## License

GPLv3

## Author Information

http://www.sekoya.org
