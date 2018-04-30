# pa-fuel-example

# Synopsis

A quick example showing how to utilize Ansible to automate the creation of dynamic ip and port style NAT policies in PANOS.

Ansible version: 2.4.2.0
# Installation

This assumes that you are using Linux or a Mac and you have Git already installed.

1. Check out the Git repository
```
$ git clone https://github.com/danlowe/pa-fuel-example.git
```

2. Install Ansible using pip:
```
$ sudo easy_install pip
$ sudo pip install ansible
```
# Example playbook run

```
daniel.lowe@USDR00216 pa-fuel-example (master) $ ansible-playbook playbooks/paloalto-add-multiple-objects.yaml

PLAY [pa] ******************************************************************************************************************************************************************

TASK [Gathering Facts] *****************************************************************************************************************************************************
ok: [pa-50]

TASK [Add 4.1.1.0/24 IP Address Objects] ***********************************************************************************************************************************
changed: [pa-50] => (item=5)
changed: [pa-50] => (item=6)
changed: [pa-50] => (item=7)
changed: [pa-50] => (item=8)
changed: [pa-50] => (item=9)
changed: [pa-50] => (item=10)

TASK [Add 10.252 /24 Network Address Objects] ******************************************************************************************************************************
changed: [pa-50] => (item=5)
---
changed: [pa-50] => (item=6)
changed: [pa-50] => (item=7)
changed: [pa-50] => (item=8)
changed: [pa-50] => (item=9)
changed: [pa-50] => (item=10)

TASK [Add NAT Objects] *****************************************************************************************************************************************************
changed: [pa-50] => (item=5)
changed: [pa-50] => (item=6)
changed: [pa-50] => (item=7)
changed: [pa-50] => (item=8)
changed: [pa-50] => (item=9)
changed: [pa-50] => (item=10)

PLAY RECAP *****************************************************************************************************************************************************************
pa-50                      : ok=4    changed=3    unreachable=0    failed=0

daniel.lowe@USDR00216 pa-fuel-example (master) $
```
