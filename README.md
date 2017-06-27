# ansible-nvm

ansible role to install nvm

https://galaxy.ansible.com/suzuki-shunsuke/nvm/

Requirements
------------

* git

Role Variables
--------------

* nvm_dir: By default, if the environment variable NVM_DIR is set this value is set, and otherwise $HOME/.nvm is set
* nvm_rc_path: By default, lines aren't added

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
