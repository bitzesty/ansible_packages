## Bit Zesty's Ansible Packages Role

**For recent changes please refer to [the changelog](https://github.com/bitzesty/ansible_packages/blob/master/CHANGELOG.md)**.

Installs bunch of general packages on Debian/Ubuntu servers.

#### Default list of packages

```
- curl
- build-essential
- git
- git-core
- python-software-properties
- python-pip
- libpq-dev
- zlib1g-dev
- nodejs
- imagemagick
- libmagickwand-dev
- sqlite3
- libsqlite3-dev
- libxslt1-dev
- libxml2-dev
- libcurl4-openssl-dev
- libffi-dev
- libreadline-dev
- libssl-dev
- runit
- htop
- httplib2
```

#### Role Variables

List of default packages:
```
default_packages:
  - curl
  - build-essential
```

List of advanced packages:
```
advanced_packages:
  - nano
  - htop
```

#### Example Playbook

```
- hosts: ci-server
  vars:
    advanced_packages:
      - nano
      - vim
  roles:
    - { role: bitzesty.packages }
```

#### License

MIT / BSD

#### Author Information

This role was created in 2014 by developers from (Bitzesty LTD)[https://github.com/bitzesty].
