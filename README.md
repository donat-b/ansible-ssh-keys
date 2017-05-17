Ansible Role: SSH keys
========

Helps manage SSH authentication across machines using keys.

Requirements
------------

None

Role Variables
--------------

```yaml
ssh_auth_keys:
  - left_host: 'machine2'  # The client
    right_host: 'machine1' # The remote
    user: root             # The username on the remote host
    key_name: id_rsa
    key_options: 'from="{{ hostvars["machine2"].ansible_eth1.ipv4.address }}"'
    overwrite_key: false
```

Dependencies
------------

None

Example Usage
-----

```yaml
- hosts: all
  roles:
    - ssh-keys
```

License
-------

BSD
