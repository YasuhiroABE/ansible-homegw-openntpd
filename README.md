YasuhiroABE.homegw-opnntpd
=========

This role sets up openntpd package for my gateway router.

Requirements
------------

This role is tested on the following platforms.

### Ansible
- Version 2.4

### Distributions
- Ubuntu 16.04
- Debian 9

Role Variables
--------------

### Default
	# local network address to listen
	homegw_openntpd_listenon_address: ''

	# external ntp server address
	homegw_openntpd_server_addresses: []

Dependencies
------------

N/A

Example Playbook
----------------

    - hosts: all
	  vars:
		# local network address to listen
    	homegw_openntpd_listenon_address: 0.0.0.0

    	# external ntp server address
    	homegw_openntpd_server_addresses:
	      - ntp.nict.jp
          - ntp1.jst.mfeed.ad.jp
          - ntp2.jst.mfeed.ad.jp
          - ntp3.jst.mfeed.ad.jp
      roles:
         - YasuhiroABE.homegw-openntpd

License
-------

Apache License 2.0

Author Information
------------------

[Yasuhiro ABE](http://www.yasundial.org/foaf.xml)

