ansible-role-windows-base
=========================

[![Ansible Role: bit_kitchen.windows_base](https://img.shields.io/ansible/role/49029.svg)](https://galaxy.ansible.com/bit_kitchen/windows_base)
[![Build Status](https://travis-ci.org/bit-kitchen/ansible-role-windows-base.svg?branch=master)](https://travis-ci.org/bit-kitchen/ansible-role-windows-base)

Install base packages for Windows.

This role will do nothing on Linux, so that it can be depended on by roles compatible with both Linux and Windows.

    ansible-galaxy install bit_kitchen.windows_base

Requirements
------------

None.

Role Variables
--------------

```yml
chocolatey_latest: yes

chocolatey_packages:
- 7zip
- beyondcompare
- chocolatey
- everything
- firefox
- googlechrome
- gsudo
- linkshellextension
- microsoft-windows-terminal
- mouse-jiggler
- notepadplusplus
- powershell-core
- qttabbar
- sysinternals
```


Dependencies
------------

None.

Example Playbook
----------------

```yml
- name: Install base packages for Windows
  hosts: windows
  roles:
  - name: bit_kitchen.windows_base
    # Specify "yes" to upgrade base packages to latest;
    # Specify "no" to install them if not already.
    chocolatey_latest: no
```


```yml
- name: Install/Upgrade custom packages for Windows
  hosts: windows
  roles:
  - name: bit_kitchen.windows_base
    # Specify "yes" to upgrade specified packages to latest;
    # Specify "no" to install them if not already.
    chocolatey_latest: yes
    # List of packages to install
    chocolatey_packages:
    - vlc
```

License
-------

[MIT](LICENSE)

Author Information
------------------

[bit.kitchen](https://github.com/bit-kitchen)
