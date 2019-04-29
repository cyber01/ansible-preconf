# Ansible Role: Preconf

Can be used for preconf all RHEL-based servers

Upgrades all packages, install EPEL, start apps, change hostname, init firewalld, disable ipv6.

## Requirements

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    upgrade_all: true

Upgrades all available packages if `true`.

    install_epel: true

Installs EPEL repo in system if `true`.

    start_soft: true   

Installs start software in system (vim,net-tools,bind-utils,rsync,wget,pwgen,screen,git,zip,unzip,iotop,jnettop,psmisc) if `true` and if `install_epel` is `true`.

    init_firewalld: true

Installs and autostart firewalld if `true`, by default allows only 22 port (SSH).

    change_hostname: true
    hostname: "localhost.localdomain"

If `true`, changes hostname to `hostname`. Changes

    disable_ipv6: true

If `true`, disable IPv6 support on system. Needs reboot.

## Dependencies


## Example Playbook

    - hosts: servers
      roles:
        - preconf_centos


## License

MIT / BSD

## Author Information

This role was created in 2019 by [Sergey Brovko](http://cyber01.ru/).
