# Debian Uptade Management

Methods of Playbook

##### List Method (Default) : 
Playbook shows only Upgrade list.
Example

```bash
ansible-playbook Debian_Update_Manager.yml
ansible-playbook Debian_Update_Manager.yml --extra-vars "choise=list"
```
 
     
##### Upgrade Method (Default Only List) : 
Playbook upgrade all packages in inculude hosts.
Example

```bash
ansible-playbook Debian_Update_Manager.yml --extra-vars "choise=upgrade"
```
 
##### Reboot Method (Default No)
Sometime required reboot after upgrade. You can use this method. 
Example

```bash
ansible-playbook Debian_Update_Manager.yml --extra-vars "choise=upgrade reboots=Yes" 
ansible-playbook Debian_Update_Manager.yml --extra-vars "choise=upgrade reboots=No"
```
 
##### Hold Packages Method(Default or Empty is Blank)
You can hold packages while system upgrading
Example

```bash
ansible-playbook Debian_Update_Manager.yml --extra-vars "{"holds": [sudo,vim,unzip,xterm]}" --extra-vars "choise=upgrade reboots=Yes" 
ansible-playbook Debian_Update_Manager.yml --extra-vars "{"holds": [sudo,vim,unzip,xterm]}" --extra-vars "choise=upgrade reboots=No"
```
##### Repo Update Method (Default No)
You can update default repo to own repo

Example 
```bash
ansible-playbook Debian_Update_Manager.yml  --extra-vars "chrep=Yes"
```
