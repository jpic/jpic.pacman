Role Name
=========

Setup configuration for Arch Linux package manager: pacman.

Requirements
------------

Arch Linux and/or pacman.

Role Variables
--------------

- pacman_mirrors: a list of prefered mirrors that will be at the top of
  mirrorlist.

Example Playbook
----------------

This example will setup XferCommand in pacman.conf, upload and import your
local verified and trusted pacman-keys, place http://arch.yourlabs.org/$arch at
the top of mirrorlist, add the repo-ck repository and sync pacman if anything
changed::

    - hosts: servers
      roles:
         - role: jpic.pacman
           pacman_mirrors:
           - http://arch.yourlabs.org/
           pacman_repositories:
           - name: repo-ck
             url: http://repo-ck.com/$arch
           pacman_options:
             XferCommand: /usr/bin/wget --passive-ftp -c -O %o %u

License
-------

BSD
