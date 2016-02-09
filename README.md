# Ansible Role: Dotfiles

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-dotfiles.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-dotfiles)

Installs a set of dotfiles from a given Git repository. By default, it will install my (geerlingguy's) [dotfiles](https://github.com/geerlingguy/dotfiles), but you can use any set of dotfiles you'd like, as long as they follow a conventional format.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    dotfiles_repo: "https://github.com/geerlingguy/dotfiles.git"

The git repository to use for retrieving dotfiles. Dotfiles should generally be laid out within the root directory of the repository.

    dotfiles_repo_local_destination: "~/Documents/dotfiles"

The local path where the `dotfiles_repo` will be cloned.

    dotfiles_home: "~"

The home directory where dotfiles will be linked. Generally, the default should work, but in some circumstances, or when running the role as sudo on behalf of another user, you may want to specify the full path.

    dotfiles_files:
      - .bash_profile
      - .gitignore
      - .inputrc
      - .vimrc

Which files from the dotfiles repository should be linked to the `dotfiles_home`.

Add the hostkey for the repo url if not already added. If ssh_opts contains "-o StrictHostKeyChecking=no", this parameter is ignored. Defaults to `No`

    dotfiles_repo_accept_hostkey: yes

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
