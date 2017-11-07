# idm-server
Build a new idm server or replica for a Red Hat POC environment. Use this role to build an IdM Server that will provide the basic users, groups, host groups, sudo rules, and hbac rules necessary to evaluate Red Hat products including: Red Hat Satellite, Red CloudForms, Red Hat Ansible Tower, Red Hat OpenShift Container Platform and others. 

## Status
Currently only the IdM Server build is implemented.

## Suggested use

1. Build an @base Red Hat Enterprise Linux 7 system. 
2. If you are going to run directly from the IdM server
   a) Enable the rhel-7-server-extras-rpms repo
   b) Install ansible and git
3. Clone this repo to the server with ansible on it
4. Edit the hosts file to include your host
5. Edit the main.yml file to configure your variables.
6. Run the playbook.
7. Enjoy!


## What does it do?

This role will install and configure the IdM server, it will also:
- configure firewalld for use with IdM
- add a set of basic users to the IdM environment for standard demonstrations and use cases
- set up the groups used to provide standard roles in Satellite
- set up the groups used to provide standard roles in CloudForms 
- set up the groups used to provide standard roles in Tower
- set up the groups used to provide standard roles in Openshift Container Platform
- set up sample sudo rules and add the appropriate users, groups and hostgroups to the rules
- set up sample hbac rules and add the appropriate users, groups and hostgroups to the rules

Pull requests are welcome if you want to enhance any of the above or add additional config for more products.

Cheers,

Paul
