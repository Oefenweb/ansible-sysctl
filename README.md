## sysctl

[![CI](https://github.com/Oefenweb/ansible-sysfs/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-sysfs/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-sysctl-blue.svg)](https://galaxy.ansible.com/Oefenweb/sysctl)

Manage `sysctl` settings.

#### Requirements

* `procps` (will be installed)

#### Variables

* `sysctl_settings`: [default: `[]`]: List of `sysctl` settings
* `sysctl_settings.{n}.name`: [required]: Name of the setting
* `sysctl_settings.{n}.value`: [required]: Value of the setting
* `sysctl_settings.{n}.state`: [default: `present`]: Whether to ensure the setting is present or absent

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - oefenweb.sysctl
  vars:
    sysctl_settings:
      - name: net.ipv4.tcp_fin_timeout
        value: 10
```

#### License

MIT

#### Author Information

* Mark van Driel
* Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-sysctl/issues)!
