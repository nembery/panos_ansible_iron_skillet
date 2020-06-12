# panos_ansible_iron_skillet

A playbook to load IronSkillet on a freshly deployed PAN-OS VM-Series. For more information about IronSkillet, see
the [IronSkillet documentation](https://iron-skillet.readthedocs.io/en/docs_master/overview.html).  

You will need the paloaltonetworks.panos and paloaltonetworks.skillet collections installed

## Requirements

To run this skillet create a virtual environment, install ansible and download the nembery.skillets collection:
 
```bash

apt install python3-venv
python3 -m venv .venv
. ./venv/bin/activate
pip install ansible

ansible-galaxy collection install nembery.skillet

```

## Running

Edit the variables file to customize IronSkillet for your environment, then run the following command:

```bash

ansible-playbook -i inventory.yml -e 'username=admin' -e 'password=Super! Secret!' -e 'ip_address=10.0.1.55' load_iron_skillet.yml 

```

* Note - Any variables passed in via a `-e` switch will override values in the vars/main.yml file.