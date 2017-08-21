# Ansible Role : Device Manager for the Linux Kernel.

An Ansible Role that manages udev

## Role Variables:

Available variables are listed below, along with the default values (see `defaults/main.yml`):

    sysctl:
      key:
        value:
        state

    ie: sysctl:
          vm.swappiness:
            value: 1
            state: present

## Dependencies

None.

## Example Playbook

    - hosts: kubernetes-nodes
      var_files:
      - vars/main.yaml
      roles:
      - 'sysctl'
