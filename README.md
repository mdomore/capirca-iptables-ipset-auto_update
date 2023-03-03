# Ansible role for creating iptables rules from capirca definition files.

## Features

- Use capirca definition files
- Use Ipset for fqdn
- Generate iptables file to be used with iptables-restore
- Generate python scripts to update ipset continuously
- Generate systemd service files to start python script with systemd

## Installation

### Capirca

Ref : https://github.com/google/capirca

### Capirca ACL Collection for Ansible

Ref : https://github.com/nleiva/capirca_acl

## Usage

Add your policies in input.pol, ouput.pol and forward.pol files.
Add your fqdn access in ipset.yml

Example :

```yaml
---
ipset:
  - name: server1_foo_com
    dst: 192.168.1.10
    dst_port: "443"
    src:
      - test.io
      - server1.test.io
      - server2.test.io
```

Launch the playbook pb.main.yml

Result will be in ~/iptables
