# Vagrant Labs: anisble-dev-vagrant-lab

This repository is an part of the Vagrant Labs project that is intendet to deliver Vagrant based labs from various IT technologies. This particular lab is creating Ansible development environment with various virtual machines besed on different Linux OS families to test Ansible playbooks and roles during development process.

## Table of contents

Use for instance <https://github.com/kamikazestar/ansible-dev-vagrant-lab>:

> * [Title / Repository Name](#title--repository-name)
>   * [About / Synopsis](#about--synopsis)
>   * [Table of contents](#table-of-contents)
>   * [Installation](#installation)
>   * [Usage](#usage)
>     * [Screenshots](#screenshots)
>     * [Features](#features)
>   * [Code](#code)
>     * [Content](#content)
>     * [Requirements](#requirements)
>     * [Limitations](#limitations)
>     * [Build](#build)
>     * [Deploy (how to install build product)](#deploy-how-to-install-build-product)
>   * [Resources (Documentation and other links)](#resources-documentation-and-other-links)
>   * [Contributing / Reporting issues](#contributing--reporting-issues)
>   * [License](#license)
>   * [About Nuxeo](#about-nuxeo)

## About

- Why?
- Inspiration
- What I'd achieved thanks to this project?

## Technologies

 - [VirtualBox](https://www.virtualbox.org/)
 - [Vagrant](https://www.vagrantup.com/)
    - [Centos 8](https://app.vagrantup.com/centos/boxes/8)
    - [Centos 7](https://app.vagrantup.com/centos/boxes/7)
    - [Fedora 31](https://app.vagrantup.com/fedora/boxes/31-cloud-base)
    - [Fedora 30](https://app.vagrantup.com/fedora/boxes/30-cloud-base)
    - [Ubuntu 18.04 LTS](https://app.vagrantup.com/ubuntu/boxes/bionic64)
    - [Ubuntu 16.04 LTS](https://app.vagrantup.com/ubuntu/boxes/xenial64)
    - [Debian 10](https://app.vagrantup.com/debian/boxes/buster64)
    - [Debian 9](https://app.vagrantup.com/debian/boxes/stretch64)
 - [Anisble](https://www.ansible.com/)

## Lab setup
---

### Install required software

To run this lab you will need to install all of the software that had been listed in [Technologies]() section. I'm assuming that you have besic IT knoweledge and know how to do that.

### Clone code

Clone this code to your workspace directory using command below: 

```
git clone git@github.com:kamikazestar/ansible-dev-vagrant-lab.git
```

#### Pre-run tasks (Optional)

As an prerequisit I highly recommend to download all of the supported Vagrant boxes, especially if you have poor Internet connection:

- [Centos 8](https://app.vagrantup.com/centos/boxes/8)
- [Centos 7](https://app.vagrantup.com/centos/boxes/7)
- [Fedora 31](https://app.vagrantup.com/fedora/boxes/31-cloud-base)
- [Fedora 30](https://app.vagrantup.com/fedora/boxes/30-cloud-base)
- [Ubuntu 18.04 LTS](https://app.vagrantup.com/ubuntu/boxes/bionic64)
- [Ubuntu 16.04 LTS](https://app.vagrantup.com/ubuntu/boxes/xenial64)
- [Debian 10](https://app.vagrantup.com/debian/boxes/buster64)
- [Debian 9](https://app.vagrantup.com/debian/boxes/stretch64)

You can do that using included file with all Vagrant boxes that are used in this lab:

```
for i in `cat ./vagrant_boxes`; do vagrant box add --provider virtualbox $i; done
```

Boxes can be also updated using command listed below:

```
vagrant box update
```

### Run lab

To provision lab you need to only run this command: 

```
vagrant up
```

### Run playbook / Test the role

Place example playbook and how to exacute role.

### Features

This Vagrant lab is provisioning clean OS instances, but you can also provision pre-configured instances using Ansible provisioner and bootstrap.yml playbook.
To do that you need to add required tasks/roles to bootstrap.yml file and uncomment  sections contains [vm_name].vm.provision.

## Status

Place current status of the project

## Inspiration

- Jeff Geerling website and links to Docker images
- Description of the issue with Ansible hostname role

## Usage

This seems to be an repetitition of the Setup section

### Screenshots

This probably won't be necessary

## Code
---

### Content

Repository contains files listed below:

- [ansible.cfg](): Ansible configuration file.
 
- [bootstrap.yml](): File that can be used to provision addional services on bootspraped instances.

- [inventory](): Predefined Ansible inventory file with instances definition grupped by OS family and type.

- [Vagrantfile](): Main Vagrant lab configuration file contains definitions of all instances that will be provisioned.

- [vagrant_boxes](): File with list of all Vagrant boxes used by this Vagrant lab. This file can be used to install all of them.

### Requirements

### Limitations

### Build

### Deploy (how to install build product)

## Resources (Documentation and other links)

## Contributing / Reporting issues

## License

[GNU General Public License, Version 3](https://github.com/kamikazestar/ansible-dev-vagrant-lab/LICENSE)

## Author Information

* **Marcin Slabonski** - *Initial work* - [kamikazestar](https://github.com/kamikazestar)