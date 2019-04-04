# ansible-role-percona

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-percona.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-percona)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-percona-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/percona)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

RHEL/CentOS - Percona RPM repository

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    percona_arch: noarch
    percona_baseurl: "https://repo.percona.com/yum"
    percona_disablerepo: []
    percona_enablerepo: []
    percona_fetch: >-
      {{ percona_baseurl }}/{{ percona_release }}.{{ percona_arch }}.rpm
    percona_packages: []
    percona_pkg: percona-release
    percona_rel: 9
    percona_release: "{{ percona_pkg }}-{{ percona_ver }}-{{ percona_rel }}"
    percona_repository_experimental_basearch: false
    percona_repository_experimental_noarch: false
    percona_repository_experimental_source: false
    percona_repository_release_basearch: false
    percona_repository_release_noarch: false
    percona_repository_release_source: false
    percona_repository_testing_basearch: false
    percona_repository_testing_noarch: false
    percona_repository_testing_source: false
    percona_ver: 1.0

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.percona
          percona_repository_release_basearch: true
          percona_repository_release_noarch: true

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
