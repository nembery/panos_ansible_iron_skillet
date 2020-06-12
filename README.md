# panos_ansible_iron_skillet

A playbook to load IronSkillet on a freshly deployed PAN-OS VM-Series. For more information about IronSkillet, see
the [IronSkillet documentation](https://iron-skillet.readthedocs.io/en/docs_master/overview.html).  

You will need the paloaltonetworks.panos and paloaltonetworks.skillet collections installed

## Running

```bash

ansible-playbook -i inventory.yml -e 'username=admin' -e 'password=Super! Secret!' -e 'ip_address=10.0.1.55' load_iron_skillet.yml 

```