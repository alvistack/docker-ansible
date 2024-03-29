# Docker Image Packaging for Ansible

<a href="https://alvistack.com" title="AlviStack" target="_blank"><img src="/alvistack.svg" height="75" alt="AlviStack"></a>

[![GitLab pipeline status](https://img.shields.io/gitlab/pipeline/alvistack/docker-ansible/master)](https://gitlab.com/alvistack/docker-ansible/-/pipelines)
[![GitHub tag](https://img.shields.io/github/tag/alvistack/docker-ansible.svg)](https://github.com/alvistack/docker-ansible/tags)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-ansible.svg)](https://github.com/alvistack/docker-ansible/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/ansible-6.4.svg)](https://hub.docker.com/r/alvistack/ansible-6.4)

Ansible is an open source community project sponsored by Red Hat, it's the simplest way to automate IT.

Learn more about Ansible: <https://www.ansible.com/>

## Supported Tags and Respective Packer Template Links

  - [`alvistack/ansible-6.4`](https://hub.docker.com/r/alvistack/ansible-6.4)
      - [`packer/docker-6.4/packer.json`](https://github.com/alvistack/docker-ansible/blob/master/packer/docker-6.4/packer.json)
  - [`alvistack/ansible-6.3`](https://hub.docker.com/r/alvistack/ansible-6.3)
      - [`packer/docker-6.3/packer.json`](https://github.com/alvistack/docker-ansible/blob/master/packer/docker-6.3/packer.json)
  - [`alvistack/ansible-5.10`](https://hub.docker.com/r/alvistack/ansible-5.10)
      - [`packer/docker-5.10/packer.json`](https://github.com/alvistack/docker-ansible/blob/master/packer/docker-5.10/packer.json)
  - [`alvistack/ansible-5.9`](https://hub.docker.com/r/alvistack/ansible-5.9)
      - [`packer/docker-5.9/packer.json`](https://github.com/alvistack/docker-ansible/blob/master/packer/docker-5.9/packer.json)
  - [`alvistack/ansible-4.10`](https://hub.docker.com/r/alvistack/ansible-4.10)
      - [`packer/docker-4.10/packer.json`](https://github.com/alvistack/docker-ansible/blob/master/packer/docker-4.10/packer.json)
  - [`alvistack/ansible-4.9`](https://hub.docker.com/r/alvistack/ansible-4.9)
      - [`packer/docker-4.9/packer.json`](https://github.com/alvistack/docker-ansible/blob/master/packer/docker-4.9/packer.json)

## Overview

This Docker container makes it easy to get an instance of Ansible up and running.

Based on [Official Ubuntu Docker Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

  - Packaging by Packer Docker builder and Ansible provisioner in single layer
  - Handle `ENTRYPOINT` with [catatonit](https://github.com/openSUSE/catatonit)

### Quick Start

For the `VOLUME` directory that is used to store the repository data (amongst other things) we recommend mounting a host directory as a [data volume](https://docs.docker.com/engine/tutorials/dockervolumes/#/data-volumes), or via a named volume if using a docker version \>= 1.9.

Start Ansible:

    # Pull latest image
    docker pull alvistack/ansible-6.4
    
    # Run as detach
    docker run \
        -itd \
        --rm \
        --name ansible \
        alvistack/ansible-6.4 \
        ansible --version

## Versioning

### `YYYYMMDD.Y.Z`

Release tags could be find from [GitHub Release](https://github.com/alvistack/docker-ansible/tags) of this repository. Thus using these tags will ensure you are running the most up to date stable version of this image.

### `YYYYMMDD.0.0`

Version tags ended with `.0.0` are rolling release rebuild by [GitLab pipeline](https://gitlab.com/alvistack/docker-ansible/-/pipelines) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
