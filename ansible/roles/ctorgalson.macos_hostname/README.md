# Ansible Role macOS Hostname

[![Build Status](https://travis-ci.com/ctorgalson/ansible-role-macos-hostname.svg?branch=master)](https://travis-ci.com/ctorgalson/ansible-role-macos-hostname)

A simple Ansible role to set HostName, LocalHostName, and ComputerName on macOS.

## Requirements

No special requirements.

## Role Variables

| Variable name      | Default value     | Description               |
|--------------------|-------------------|---------------------------|
| `mh_hostname`      | `''`              | The HostName to set.      |
| `mh_localhostname` | `MhLocalHostName` | The LocalHostName to set. |
| `mh_computername`  | `MhComputerName`  | The ComputerName to set.  |

- The properties `HostName`, `LocalHostName`, and `ComputerName` referred to in the table are keywords used with the `scutil` command on macOS.
- Setting a value for `HostName` may have unpredictable or confusing results. See the answers to this [Stack Overflow question](https://apple.stackexchange.com/questions/30552/os-x-computer-name-not-matching-what-shows-on-terminal) for more information.

## Example Playbook

    - hosts: servers
      roles:
         - role: ansible-role-macos-hostname

## License

GPLv3

## Author Information

Christopher Torgalson
