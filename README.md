# Ansible Role: Dotfiles

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-dotfiles.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-dotfiles)

Installs a set of dotfiles from a given Git repository. By default, it will install my (geerlingguy's) [dotfiles](https://github.com/geerlingguy/dotfiles), but you can use any set of dotfiles you'd like, as long as they follow a conventional format.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    TODO

## Dependencies

None

## Example Playbook

    - hosts: localhost
      roles:
        - { role: geerlingguy.dotfiles }

## License

MIT / BSD

## Author Information

This role was created in 2015 by [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/).
