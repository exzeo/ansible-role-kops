Ansible Role Kops
=========

Installs Helm Command Line on Debian/Ubuntu servers. 
Releases: https://github.com/kubernetes/kops/releases

Role Variables
--------------

```
# Version of 'kops' to install, defaults to latest version
kops_version: ""

# Toggling this will uninstall from the server
uninstall: false
```

```

Example Playbooks
----------------

Minimal:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.kops
```

Specific Version:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.kops
      vars:
        kops_version: "1.22.4"
```

Uninstall:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.kops
      vars:
        uninstall: true
```