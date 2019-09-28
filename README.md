Role Name
=========

Configure dropbear-initramfs to allow remote (ssh) unlocks of Luks encrypted root-volumes

Requirements
------------

You need to specify an 'ip' option on your kernel-commandline, so you can actually connect
to the booting system. This role will update your /etc/default/grub file, but this is
mostly just an example, please replace with your own preferred config


Role Variables
--------------

encrypted_rootfs: Set this to true to enable this role's changes, defaults to false
dropbear_port:  Port dropbear-ssh should listen on, defaults to 10022
dropbear_options: Options to hand to dropbear (defaults should be sufficient)
grub_cmdline_linux: The commandline for the kernel, should include the 'ip' config. This
needs te be replaced/customized for your configuration.

Dependencies
------------

Debian (8, 9, 10)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars:
        encrypted_rootfs: true
      roles:
         - { role: sigio.dropbear-initramfs }

License
-------

BSD

Author Information
------------------

Mark Janssen -- Sig-I/O Automatisering

