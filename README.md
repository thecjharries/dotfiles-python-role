# `dotfiles-role-python`

[![Build Status](https://travis-ci.org/thecjharries/dotfiles-role-python.svg?branch=master)](https://travis-ci.org/thecjharries/dotfiles-role-python)
[![GitHub tag](https://img.shields.io/github/tag/thecjharries/dotfiles-role-python.svg)](https://github.com/thecjharries/dotfiles-role-python)


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
- src: git+https://github.com/thecjharries/dotfiles-role-common-software.git
- src: git+https://github.com/thecjharries/dotfiles-role-package-installer.git
```

## Example Playbook

## License

ISC
