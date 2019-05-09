Bareos VMware plugin
=========

This role installs the VMware plugin and creates respected config and jobs.
Basically this plugin takes VM snapshots using vCenter API.

Requirements
------------
 
 ansible minimum version 2.4


Role Variables
--------------

In order to backup the VMs you need to define the `vm_backups` variable with the following values:

* **name**: is the VM's name and is used to define Job and FileSet names as well
* **folder**: is the vcenter folder where the vm is located
* **dc**: is the vcenter datacenter where the folder is located

Dependencies
------------

You need to have a running bareos server in order to use this plugin. 

So these are the dependency roles:

* bareos-basic
* bareos-database
* bareos-director

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: bareos-vmware-plugin }

License
-------

BSD

Author Information
------------------

Hamidreza Joshaghani