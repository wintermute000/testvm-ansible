configure-yanghosts
=========

Installs Yang Development Kit (YDK) 0.7.1, all dependencies / workaround steps and following models
- IETF
- Openconfig
- Cisco IOS-XE
- Cisco IOS-XR

Documented here: https://github.com/CiscoDevNet/ydk-py

YDK homepage: http://ydk.cisco.com/py/docs/

Requirements
------------

CentOS 7 VM with at least 4Gb RAM. 3.5Gb MAY work but not tested, definitely fails on 2Gb - building the YDK and models takes up large amounts of RAM.
As per documentation, the latest version of YDK does not work in Ubuntu.
The role requires sudo - you're installing stuff via yum.
PIP tasks may be easily amended to utilise virtualenvs.

Role Variables
--------------
requirements.txt - file located in files - as per https://github.com/CiscoDevNet/ydk-gen/blob/master/requirements.txt

Dependencies
------------
Written in Ansible 2.5.1, not tested on any other versions but should work on any 2.x given only standard modules are utilised

Example Playbook
----------------
Use this role in a playbook or adapt code for main playbook run

License
-------

BSD

Author Information
------------------
wintermute000@planetexpress.com.au
