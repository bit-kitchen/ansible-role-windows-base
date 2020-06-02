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

chocolatey_packages_basic:
- 7zip
- chocolatey
- everything
- firefox
- googlechrome
- linkshellextension
- microsoft-edge
- notepadplusplus
- qttabbar

chocolatey_packages_dev:
- beyondcompare
- bitvise-ssh-client
- cygwin
- git
- git-lfs
- microsoft-windows-terminal
- vscode

chocolatey_packages_custom: []
```


Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: windows
  roles:
  - name: bit_kitchen.windows_base
    # Specify "yes" to upgrade existing packages to latest;
    # Specify "no" to install new packages only.
    chocolatey_latest: no
    # List of additional packages to install
    chocolatey_packages_custom:
    - vlc
```

License
-------

[MIT](LICENSE)

Author Information
------------------

[bit.kitchen](https://github.com/bit-kitchen)
