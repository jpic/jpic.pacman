Role Name
=========

Setup configuration for Arch Linux package manager: pacman.

Requirements
------------

Arch Linux and/or pacman.

Role Variables
--------------

- archlinux_mirrors: a list of prefered mirrors that will be at the top of
  mirrorlist.

Example Playbook
----------------


Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: jpic.archlinux
           archlinux_mirrors:
           - http://arch.yourlabs.org/
           archlinux_repositories:
           - name: repo-ck
             url: http://repo-ck.com/$arch
           archlinux_keys:
           - 5EE46C4C

License
-------

BSD
