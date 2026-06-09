# ans_server_misc_playbooks

These are a collection of playbooks for automating "standard" processes relating to server builds and administration.


## Playbooks
### Bootstrap
These playbooks handle tasks pertaining to the initial setup of servers
- bootstrap_day1
- bootstrap_day2
- bootstrap_day3

### Domain

These playbooks handle servers joining and leaving the TU domain

### Patching
Playbook to install updates and reboot servers

#### Compatibility
| OS               | Works               |
| ---------------- | ------------------- |
| Linux / RHEL     | :heavy_check_mark:  |
| Linux / Ubuntu   | :heavy_check_mark:  |
| Windows          | :x:                 |


#### Dependencies
- [toweragent]()
- [ans_server_patching_role]()


### Server Access
These playbooks handle creation server access groups along with managing the membership of said groups
- serveraccess_group_create | creates server access group in AD under mydomain.net/AD Administration/Roles/Computer-Administration/Server-Administration/Local-Groups
- serveraccess_group_members | adds an AD object, group preferrably, to a server access group (i.e. AD-ServerAccess-(SERVERNAME)-LocalGroups-Administrators)
