beats
=====

[![Build Status](https://travis-ci.org/andrelohmann/ansible-role-beats.svg?branch=master)](https://travis-ci.org/andrelohmann/ansible-role-beats)

Simple role to install all selected beats to your machine.

!!! This role doesn't take security into account. Shipping of data should be secured by iptables. !!!

!!! This role builds the counterpart to https://galaxy.ansible.com/andrelohmann/elasticstack !!!

Role Variables
--------------

    elasticsearch_listen_ip: "localhost" # ip address to which beats should connect to
    elasticsearch_release: 7.1.1

    elasticsearch_install_auditbeat: True
    elasticsearch_install_filebeat: True
    elasticsearch_install_heartbeat: False
    elasticsearch_install_metricbeat: True
    elasticsearch_install_packetbeat: True

Example Playbook
----------------

    - hosts: beats
      roles:
         - { role: andrelohmann.beats }

License
-------

MIT

Author Information
------------------

https://github.com/andrelohmann
