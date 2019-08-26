Role Name
=========

LAMP

default settings

Requirements
------------

For installation on Ubuntu 16.04
For installation on other platforms need change parameters  "when: ansible_distribution_release == 'xenial'" in all files and change package version in php.yml

Role Variables
--------------

Some variables are defined in /vars/main.yml


Structure
------------


	- [roles]
		-[LAMP]
			-[files]
				*info.php
			-[handlers]
				*main.yml
			-[tasks]
				*apache.yml
				*main.yml
				*mysql.yml
				*php.yml
				*test.yml
			-[templates]
				-[etc]
					-[apache2]
						*apache2.conf.j2
					-[mysql]
						-[mysql.conf.d]
							*mysqld.cnf.j2
					-[php]
			-[vars]
				*main.yml


Example Playbook
----------------

    - hosts: servers
      roles:
         - LAMP

Author Information
------------------

Dmitry Lysov
