ansible-role-xubuntu-core 
========= 

Xubuntu-core is an open source desktop environment for 
detecting for Ubuntu and other Linux distributions.

This role is especially designed for a modern and lightweight 
desktop experience and contains nothing more than the minimum
of applications.

This role is fully customizable for different purposes 
and can be used for:
- Thinclients.
- Desktops.
- Linux based RDS servers.
- Servers.

etc.....


Requirements
------------

* Ubuntu server 18.04
* Ansible control server

* administrator account with sudo rights needed.


Role Variables
--------------

To many options to describe here, please look at
the " default/main.yml" for all options and documentation.

Dependencies
------------


Example Playbook
----------------

    - hosts: thinclients
      become: true

      vars:

        # -- xubuntu-core override (default settings) --
        
        # Bootscreen
        xbc_splash_type        : 'url'
        xbc_splash_image_url   : 'http://172.16.2.20/resource/greenfoodos/greenlogo.png'

        # Login 
        xbc_loginwp_type       : 'url'
        xbc_loginwp_url        : 'http://nl-bel-cmd01/resource/greenfoodos/wallpaper.jpg'
        xbc_loginwp_name       : 'wallpaper.jpg'

        # Desktop
        xbc_desktop_type       : 'url'
        xbc_desktop_url        : 'http://nl-bel-cmd01/resource/greenfoodos/wallpaper.jpg'
        xbc_desktop_name       : 'wallpaper.jpg'

        # Kiosk mode
        xbc_kiosk_state        : 'enabled'
      

        # -- End xubuntu-core override --

      roles:
         - ansible-role-xubuntu-core


License
-------

GPLv3

Author Information
------------------

E: lrutten@bitfinity.nl

I: https://www.bitfinity.nl
