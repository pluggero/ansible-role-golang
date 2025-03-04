# Ansible Role: golang

[![CI](https://github.com/pluggero/ansible-role-golang/actions/workflows/ci.yml/badge.svg)](https://github.com/pluggero/ansible-role-golang/actions/workflows/ci.yml) [![Ansible Galaxy downloads](https://img.shields.io/ansible/role/d/pluggero/golang?label=Galaxy%20downloads&logo=ansible&color=%23096598)](https://galaxy.ansible.com/ui/standalone/roles/pluggero/golang)

An Ansible Role that installs a basic configuration of golang.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
golang_version: "x.x"
```

The version of golang to install can be defined in the variable `golang_version`.

```yaml
golang_install_method: "dynamic"
```

The method used to install golang can be defined in the variable `golang_install_method`.
The following methods are available:

- `source`: Installs golang from source
- `package`: Installs golang from the package manager of the distribution
  - **NOTE**: This method installs the latest version available in the package manager and not the version defined in `golang_version`.
- `dynamic`: Installs golang from package manager if available in the correct version, otherwise installs from source

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  roles:
    - pluggero.golang
```

## License

MIT / BSD

## Author Information

This role was created in 2025 by Robin Plugge.
