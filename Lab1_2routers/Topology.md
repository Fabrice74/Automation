## LAB Topology
The lab will be done on EVE-NG
Lab name: Automation-lab1-2routers.unl

### Network diagram
'''
[VM Ansible]
192.168.65.x
     |
     |        vrf mgt
     |--------OOB-net-------|
192.168.65.101        192.168.65.102
    [R1]                   [R2]
  10.0.0.1              10.0.0.2/24
     |----------------------|
'''
