# Create simple summary reports (with modules)
based on https://github.com/ipspace/ansible-examples/tree/master/Summary-Reports

In this example, in order to generalize the solution:
- creation of "Collect" modules
- creation of "Create reports" modules
- CLI parameters used for flexibility (include one read and one create module)

'''
$ ansible-playbook framework-uptime.yml
    => OK (default collect:napalm ; default report:text)

$ ansible-playbook framework-uptime.yml --extra-vars "src=vars"
    => OK, but need the napalm facts files

$ ansible-playbook framework-uptime.yml --extra-vars "dst=template"
    => OK, but need the napalm facts files
    > Note: the Jinja2 template loops correctly into the devices facts.

$ ansible-playbook framework-uptime.yml --extra-vars "src=vars dst=template"
    => KO, the Jinja2 template doesn't loop correctly into the devices file facts. The report give 3 times the uptime of R1
'''
