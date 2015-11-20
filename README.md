Ansible role: HoneySAP
======================

An Ansible role that installs [HoneySAP](https://github.com/CoreSecurity/HoneySAP) on Debian/Ubuntu.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values:

    # Path to the configuration file to use. If no configuration file is
    # provided, the configuration would be build using the next options
    honeysap_source_config: honeysap.yml

    # Top level configuration options for HoneySAP
    honeysap_configuration
    
    # Service level configuration options for HoneySAP
    honeysap_services
    
    # Feed level configuration options for HoneySAP
    honeysap_feeds


Dependencies
------------

None.

Example Playbook
----------------

The following example playbook installs HoneySAP configured for running it
using the default external profile:

    - hosts: servers
      roles:
         - martingalloar.honeysap

The following example playbook installs HoneySAP with an standard internal
profile and using a custom database for logging attack session data:

    - hosts: servers
      roles:
         - { role: martingalloar.honeysap,
             honeysap_configuration:
                XXX
             honeysap_services:
                XXX
             honeysap_feeds:
                XXX
           }


License
-------

GPL2+


Author Information
------------------

This role was created by Martin Gallo.
