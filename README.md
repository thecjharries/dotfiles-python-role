# `dotfiles-python-role`

[![Build Status](https://travis-ci.org/thecjharries/dotfiles-python-role.svg?branch=master)](https://travis-ci.org/thecjharries/dotfiles-python-role)


## Requirements

Fedora 27 is recommended.

## Role Variables

Defaults are below.

```yml
---
owning_user: "{{ ansible_user }}"
owning_group: "{{ ansible_user }}"
root_dir: "/home/{{ ansible_user }}"
config_dir: "{{ root_dir }}/.config"

desired_state: "latest"
```

Additionally, these `vars` are set:

```yml
---
needed_packages:
  - python2
  - python2-devel
  - python2-pip
  - python3
  - python3-devel
  - python3-pip

python_packages:
  - ansible
  - asciinema
  - docker
  - docker-compose
  - virtualenv
```

## Dependencies

```yml
---
- src: git+https://github.com/thecjharries/dotfiles-common-software-role.git
- src: git+https://github.com/thecjharries/dotfiles-package-installer-role.git
```

## Example Playbook

## License

ISC
