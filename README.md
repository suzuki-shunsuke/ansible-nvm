# ansible-nvm

[![Build Status](https://travis-ci.org/suzuki-shunsuke/ansible-nvm.svg?branch=master)](https://travis-ci.org/suzuki-shunsuke/ansible-nvm)

ansible role to install nvm

https://galaxy.ansible.com/suzuki-shunsuke/nvm/

Requirements
------------

* git

Role Variables
--------------

name | required | default | description
--- | --- | --- | ---
nvm_dir | no | $NVM_DIR >> $HOME/.nvm |
nvm_rc_path | no | "NOT ADD" | By default configuration is not added

Dependencies
------------

Nothing.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.nvm
    nvm_dir: "{{ ansible_env.HOME }}/.ghq/github.com/creationx/nvm"
    nvm_rc_path: "{{ ansible_env.HOME }}/.bashrc"
```

License
-------

MIT
