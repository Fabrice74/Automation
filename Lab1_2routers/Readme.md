## LAB1 - objectif
This lab is a first simple lab composed of 2 routers reachable by my Ansible VM.
Objectif of the lab is to push the first ansible commands.

## LAB description
The lab will be done on EVE-NG. EVE-NG is running on VM.
Ansible is running on VM Ububtu 14.04.5.
osboxes@osboxes:/$ ansible-playbook --version
ansible-playbook 2.4.3.0
  config file = None
  configured module search path = [u'/home/osboxes/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/local/lib/python2.7/dist-packages/ansible
  executable location = /usr/local/bin/ansible-playbook
  python version = 2.7.6 (default, Nov 23 2017, 15:49:48) [GCC 4.8.4]


## LAB Topology
Lab name: Automation-lab1-2routers.unl

### Network diagram
```
[VM Ansible]
192.168.65.x
     |
     |        vrf mgt
     |--------OOB-net-------|
192.168.65.101        192.168.65.102
    [R1]                   [R2]
  10.0.0.1              10.0.0.2/24
     |----------------------|
```

## Runned commands
I runned some ansible simple commands with raw module:
$ ansible ios -i hosts -m raw -a "show arp"
$ ansible ios -i hosts -m raw -a "show ip arp"

One result is in the file:
