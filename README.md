# ansible-nvm

[![Build Status](https://travis-ci.org/suzuki-shunsuke/ansible-nvm.svg?branch=master)](https://travis-ci.org/suzuki-shunsuke/ansible-nvm)

ansible role to install [nvm](https://github.com/creationix/nvm)

https://galaxy.ansible.com/suzuki-shunsuke/nvm/

## Requirements

* git

## Role Variables

name | required | default | description
--- | --- | --- | ---
nvm_dir | no | $NVM_DIR >> $HOME/.nvm |
nvm_rc_path | no | "NOT ADD" | By default configuration is not added
nvm_repo | no | https://github.com/creationix/nvm |
nvm_version | no | HEAD |
nvm_update | no | yes |

## Dependencies

Nothing.

## Example Playbook

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.nvm
    nvm_dir: "{{ ansible_env.HOME }}/.ghq/github.com/creationx/nvm"
    nvm_rc_path: "{{ ansible_env.HOME }}/.bashrc"
    nvm_update: no
    nvm_version: v0.33.2
  # install as the other user
  - role: suzuki-shunsuke.nvm
    nvm_dir: /home/foo/.nvm
    nvm_rc_path: /home/foo/.bashrc"
    become: yes
    become_user: foo
```

## License

[MIT](LICENSE)
