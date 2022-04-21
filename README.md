# Stolen Credential Leading to Data Exfiltration  Solution Pack

## Release Information

- Solution Pack Version: 1.0.0
- Minimum Compatible FortiSOAR™ Version: 7.2.0
- Authored By: Fortinet
- Certified: No

## Overview

### Introduction

*Stolen Credential Leading to Data Exfiltration* solution pack demonstrates the scenarios and use cases around leaked credentials leading to attacks gaining access to the environment and creating a backdoor to exfiltrate data.

### Usage

This Solution Pack ships with the following simulation scenarios. [Refer](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/docs/solution-pack-guide.md) to Simulate Scenario documentation to understand how to Simulate and Reset Scenario.

#### 1. Scenario - Stolen Credential Leading to Data Exfiltration

The scenario demonstrates and generates a demo alert for the Alert Type

- Firewall Configuration Change
- Domain User Created
- User Group Changed
- Schedule Task Created
- Data Exfiltration
- Password Reset

Go to generated alert and observe the following:

- An attacker gains access to the Firewall using a leaked credential.
- The attacker then modifies the firewall configuration to allow RDP Access and laterally moves to a windows box.
- Creates a new domain account as a backdoor for subsequent access and also exfiltrates data.
- Observe the following in this scenario:
  - **Password Changed Alert:** Select the password change alert (typically assumed to be benign), but in this case, the collaboration panel has multiple comments indicating the indicator (jack and 10.0.1.11)
  - **Recommendations Panel:** Open the Recommendation Panel, and observe that there are alerts such as firewall configuration change suggested as related to this alert (that's because of common indicators).
  - **Escalate to Incident:** Select all suggested alerts and Escalate them to Incident. Observe Incident's correlation graph, and how it further shows Outbound data transfer as well
  ![Select Scenario](https://github.com/fortinet-fortisoar/solution-pack-stolen-credential-leading-to-data-exfiltration/raw/develop/docs/media/attackFlow.png)

## Prerequisite

Ensure that the below solution packs are deployed:

|**Solution Pack**|**Purpose**|**Doc Link**|
| :- | :- | :- |
|SOAR Framework 1.0.0|Require for Incident Response modules and Action playbooks|[Click here](https://github.com/fortinet-fortisoar/solution-pack-soar-framework/blob/develop/README.md)|
|SOC Simulator 1.0.1|Require for Scenario Module and SOC Simulator connector| [Click here](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/README.md)|

## Contents

1. Connector(s)

    |**Sr.No.**|**Connector**|
    | :- | :- |
    |1|Active Directory|
    |2|Fortinet FortiSIEM|

    **Warning:** After deployment, this Solution Pack will install or upgrade the stated connectors list.

2. Playbook Collection(s)

    - 02 - Use Case - Stolen Credential Leading to Data Exfiltration (2):
Following is a list of playbooks under “02 - Use Case - Stolen Credential Leading to Data Exfiltration”

    |**Playbook Name**|**Description**
    | :- | :- |
    |Generate Alert for Exfiltration(File Transfer)|Generates alert from FortiSIEM incident where an attacker performs outbound file transfer.|
    |Generate Alert for Firewall Configuration Change(Policy Change)|Generates alert from FortiSIEM incident where an attacker gains initial access to the network and makes firewall configuration change by changing firewall policy|
    |Generate Alert for Firewall Configuration Change(Port Forwarding)|Generates alert from FortiSIEM incident where an attacker gains initial access to the network and makes firewall configuration change by performing port forwarding|
    |Generate Alert for Persistence(Domain User Created)|Generates alert from FortiSIEM incident where an attacker once gains access to the network and creates a domain user.|
    |Generate Alert for Persistence(Schedule Task)|Generates alert from FortiSIEM incident where an attacker creates Windows scheduled task.|
    |Generate Alert for Persistence(User Added to Administrator Group)|Generates alert from FortiSIEM incident where the user is added to the Windows Administrator Group.|
    |Generate Alert for Persistence(User Password Reset)|Generates alert from FortiSIEM incident where user created by attacker changes the administrator user password.|

     **Warning:** It is recommended to clone these Playbooks before any customizations to avoid loss of information while upgrading the Solution Pack.
