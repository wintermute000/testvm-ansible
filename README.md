TESTVM-ANSIBLE
=========

A provisioning script to provision 4 classes of (existing) servers
- generic centos test hosts
- a host running the YANG devkit for NETCONF/YANG (https://developer.cisco.com/site/ydk/)
- ubuntu SD-WAN test hosts (i.e. 'branch' desktops)
- a ZScaler Private Access connector

Requirements
------------
Tested in Ansible 2.9, older versions should work but not tested

Role Variables
--------------
There are 5 roles corresponding to groupings in hosts file
- servers (all hosts) - the only action performed is yum update
- testhosts - the only action performed is to capture 'id' and output (to demonstrate sudo escalation)
- yanghosts - installs YDK and all dependencies as per https://github.com/CiscoDevNet/ydk-py
- sdwantesthosts - installs a bunch of network utilities, creates a cisco:cisco user, configures and restarts vsftpd
- zpahosts - installs the ZPA repo, updates yum cache and then installs the ZPA connector RPM

Utilises ansible-vault, sudo PW is stored in "all" in group_vars - pass in vault credentials using your chosen method

---
ansible_become_pass: XXXXX

Dependencies
------------
None

License
-------

BSD

Author Information
------------------
wintermute000

# testvm-ansible
