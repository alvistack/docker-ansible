# Docker Image Packaging for Ansible

[![Travis](https://img.shields.io/travis/com/alvistack/docker-ansible.svg)](https://travis-ci.com/alvistack/docker-ansible)
[![GitHub release](https://img.shields.io/github/release/alvistack/docker-ansible.svg)](https://github.com/alvistack/docker-ansible/releases)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-ansible.svg)](https://github.com/alvistack/docker-ansible/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/ansible.svg)](https://hub.docker.com/r/alvistack/ansible/)

Ansible is an open source community project sponsored by Red Hat, it's the simplest way to automate IT.

Learn more about Ansible: <https://www.ansible.com/>

## Supported Tags and Respective Packer Template Links

  - [`2.10`, `latest`](https://github.com/alvistack/docker-ansibleg/blob/master/packer/2.10/packer.json)

## Overview

This Docker container makes it easy to get an instance of Ansible up and running.

Based on [Official Ubuntu Docker Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

  - Packaging by Packer Docker builder and Ansible provisioner in single layer
  - Handle `ENTRYPOINT` with [catatonit](https://github.com/openSUSE/catatonit)

### Quick Start

For the `VOLUME` directory that is used to store the repository data (amongst other things) we recommend mounting a host directory as a [data volume](https://docs.docker.com/engine/tutorials/dockervolumes/#/data-volumes), or via a named volume if using a docker version \>= 1.9.

Start Ansible:

    # Pull latest image
    docker pull alvistack/ansible
    
    # Run as detach
    docker run \
        -itd \
        --rm \
        --name ansible \
        alvistack/ansible \
        ansible --version

## Versioning

### `alvistack/ansible:latest`

The `latest` tag matches the most recent [GitHub Release](https://github.com/alvistack/docker-ansible/releases) of this repository. Thus using `alvistack/ansible:latest` or `alvistack/ansible` will ensure you are running the most up to date stable version of this image.

### `alvistack/ansible:<version>`

The version tags are rolling release rebuild by [Travis](https://travis-ci.com/alvistack/docker-ansible) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
