# Create a simple device uptime report
based on https://github.com/ipspace/ansible-examples/tree/master/Sample-Summary-Report

- 3 collect playbooks collect facts from ansible, napalm and snmp (snmp not working in my environment).
- the create-report playbook reuse the napalm facts to obtain the uptime and write it in a file
