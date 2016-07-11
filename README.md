# ansible-role-percona

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-percona.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-percona)

RHEL/CentOS - Percona RPM repository

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    percona_pkg: percona-release
    percona_ver: 0.1
    percona_rel: 3
    percona_arch: noarch
    percona_baseurl: "https://www.percona.com/redir/downloads/{{ percona_pkg }}/redhat/latest"
    percona_release: "{{ percona_pkg }}-{{ percona_ver }}-{{ percona_rel }}"
    percona_fetch: "{{ percona_baseurl }}/{{ percona_release }}.{{ percona_arch }}.rpm"
    percona_repos:
      percona_release_basearch: False
      percona_release_noarch: False
      percona_release_source: False
      percona_testing_basearch: False
      percona_testing_noarch: False
      percona_testing_source: False
      percona_experimental_basearch: False
      percona_experimental_noarch: False
      percona_experimental_source: False

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.percona
          percona_repos:
            percona_release_basearch: True
            percona_release_noarch: True

## License

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
