# panos_ansible_iron_skillet

A playbook to load iron skillet on a freshly deployed PAN-OS VM-Series

You will need the paloaltonetworks.panos and paloaltonetworks.skillet collections installed

## Running

```bash

ansible-playbook -i inventory.yml -e 'username=admin' -e 'password=Super! Secret!' -e 'ip_address=10.0.1.55' load_iron_skillet.yml 

```