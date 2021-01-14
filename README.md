# Docker Image Packaging for Ansible

[![GitLab pipeline status](https://img.shields.io/gitlab/pipeline/alvistack/docker-ansible/master)](https://gitlab.com/alvistack/docker-ansible/-/pipelines)
[![GitHub release](https://img.shields.io/github/release/alvistack/docker-ansible.svg)](https://github.com/alvistack/docker-ansible/releases)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-ansible.svg)](https://github.com/alvistack/docker-ansible/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/ansible-2.10.svg)](https://hub.docker.com/r/alvistack/ansible-2.10/)

Ansible is an open source community project sponsored by Red Hat, it's the simplest way to automate IT.

Learn more about Ansible: <https://www.ansible.com/>

## Supported Tags and Respective Packer Template Links

  - [`alvistack/ansible-2.10`](https://github.com/alvistack/docker-ansible/blob/master/packer/docker-2.10/packer.json)

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

### `YYYYMMDD.Y.Z`

Release tags could be find from [GitHub Release](https://github.com/alvistack/docker-ansible/releases) of this repository. Thus using these tags will ensure you are running the most up to date stable version of this image.

### `YYYYMMDD.0.0`

Version tags ended with `.0.0` are rolling release rebuild by [GitLab pipeline](https://gitlab.com/alvistack/docker-ansible/-/pipelines) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
