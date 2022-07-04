| [Home](https://github.com/fortinet-fortisoar/solution-pack-stolen-credential-leading-to-data-exfiltration/blob/develop/README.md) |
|-----------------------------------------------------------------------------------------------------------------------------------|

# Contents

## Connectors

| Connector                  | Description                                                                                                                                                       |
|:---------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft Active Directory | Helps directly query AD to retrieve information about users, groups, and computers, in an organization, by using the Lightweight Directory Access Protocol (LDAP) |
| Fortinet FortiSIEM         | FortiSIEM provides integrations that allow you to query and make changes to the CMDB, query events, and send incident notifications.                              |

>**Warning:** After deployment, this Solution Pack will install or upgrade the stated connectors list.

## Playbook Collection

| 02 - Use Case - Stolen Credential Leading to Data Exfiltration |
|:---------------------------------------------------------------|

| Playbook Name                                                     | Description                                                                                                                                                         |
|:------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Generate Alert for Exfiltration(File Transfer)                    | Generates alert from FortiSIEM incident where an attacker performs outbound file transfer.                                                                          |
| Generate Alert for Firewall Configuration Change(Policy Change)   | Generates alert from FortiSIEM incident where an attacker gains initial access to the network and makes firewall configuration change by changing firewall policy   |
| Generate Alert for Firewall Configuration Change(Port Forwarding) | Generates alert from FortiSIEM incident where an attacker gains initial access to the network and makes firewall configuration change by performing port forwarding |
| Generate Alert for Persistence(Domain User Created)               | Generates alert from FortiSIEM incident where an attacker once gains access to the network and creates a domain user.                                               |
| Generate Alert for Persistence(Schedule Task)                     | Generates alert from FortiSIEM incident where an attacker creates Windows scheduled task.                                                                           |
| Generate Alert for Persistence(User Added to Administrator Group) | Generates alert from FortiSIEM incident where the user is added to the Windows Administrator Group.                                                                 |
| Generate Alert for Persistence(User Password Reset)               | Generates alert from FortiSIEM incident where user created by attacker changes the administrator user password.                                                     |

>**Warning:** It is recommended to clone these Playbooks before any customizations to avoid loss of information while upgrading the Solution Pack.
