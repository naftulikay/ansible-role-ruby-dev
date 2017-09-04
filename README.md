# ansible-role-ruby-dev [![Build Status][travis.svg]][travis]

Installs and configures a Ruby development environment for a given user using [`rbenv`][rbenv].

Available on Ansible Galaxy at [`naftulikay.ruby-dev`][galaxy].

## Requirements

Officially tested operating systems are listed in the Galaxy manifest.

## Role Variables

<dl>
  <dt><code>ruby_user</code></dt>
  <dd>User to install Ruby tools for. Required.</dd>
  <dt><code>ruby_version</code></dt>
  <dd>Version of Ruby to install. Defaults to 2.4.1.</dd>
<dl>

## Dependencies

None.

## Example Playbook

Here are some example playbooks to get started with.

### Defaults

Simply get a Ruby development environment installed:

```yaml
---
- name: install
  hosts: all
  become: true
  roles:
    - role: ruby-dev
      ruby_user: vagrant
```

### Install a Specific Version

Install a specific version of Ruby:

```yaml
---
  - name: install
    hosts: all
    become: true
    roles:
      - role: ruby-dev
        ruby_user: vagrant
        ruby_version: '2.4.3'
```

## License

MIT

 [travis]: https://travis-ci.org/naftulikay/ansible-role-ruby-dev
 [travis.svg]: https://travis-ci.org/naftulikay/ansible-role-ruby-dev.svg?branch=master
 [galaxy]: https://galaxy.ansible.com/naftulikay/ruby-dev/
 [rbenv]: https://github.com/rbenv/rbenv
