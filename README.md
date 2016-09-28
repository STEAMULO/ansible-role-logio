
# Ansible Role: Log.io

This role will assume the setup of log.io

It's part of the ELAO [Ansible stack](http://ansible.elao.com) but can be used as a stand alone component.

## Requirements

- Ansible 1.7.2+

## Dependencies

None.

## Installation

Using ansible galaxy:

```bash
ansible-galaxy install elao.logio
```
You can add this role as a dependency for other roles by adding the role to the meta/main.yml file of your own role:

```yaml
dependencies:
  - { role: elao.logio }
```

## Example playbook

    - hosts: servers
      vars:
        elao_logio_config_harvester:
            - nodeName: NodeXXX
            - logStreams:
              - syslog:
                - "/var/log/auth.log"
                - "/var/log/kern.log"
      roles:
         - { role: elao.logio }

# Licence

MIT

# Author information

