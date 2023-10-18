# Ansible Role: networking

[![CI](https://github.com/msltwtf/ansible-role.networking/actions/workflows/ci.yml/badge.svg)](https://github.com/msltwtf/ansible-role.networking/actions/workflows/ci.yml)

Setup basic networking for cloud vm on hetzner running debian.

# Requirements

None.

# Role Variables

Available variables are listed below, along with default values from `defaults/main.yml`

## networking_interface

```yaml
networking_interface: "{{ ansible_default_ipv4.interface }}"
```

The interface to set up. Defaults to the default ipv4 interface detected by ansible.

## networking_gateway

**WARNING: Required variable without a default value!!!**

```yaml
networking_gateway:
```

## networking_dns
```yaml
networking_dns: 1.1.1.1
```

The dns server to use. Defaults to cloudflare.

# Dependencies

None.

# Example Playbook

```yaml
- hosts: all
  roles:
    - msltwtf.networking
```

# License

MIT
