# Ansible Role: MAS-CLI

[![Build Status](https://travis-ci.org/fubarhouse/ansible-role-macstore.svg?branch=master)](https://travis-ci.org/fubarhouse/ansible-role-macstore)

Install Apple store applications using [MAS-CLI (Mac Apple Store Command Line Interface)](https://github.com/mas-cli/mas) on macOS.

## Requirements

 - Homebrew

## Role Variables

The following variables are ***required*** for this role to do anything of substance - see the example playbook or provide the following variables in order to use the role.
````
app_store_email: you@apple.com
app_store_password: password
````


````
mac_store_apps:
  - name: Microsoft OneDrive
      id: 823766827
````

## Dependencies

None.

## Example Playbook

````
    - hosts: localhost
      vars_prompt:
      - name: app_store_email
        prompt: Mac Apple Store ID
        private: no
        when: app_store_email is undefined
      - name: app_store_password
        prompt: Mac Apple Store Password
        private: yes
        when: app_store_password is undefined
      roles:
        - fubarhouse.macstore
````

## License

MIT / BSD

## Author Information

This role was created in 2016 by [Karl Hepworth](twitter.com/fubarhouse).
