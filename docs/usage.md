| [Home](https://github.com/fortinet-fortisoar/solution-pack-stolen-credential-leading-to-data-exfiltration/blob/develop/README.md) |
|-----------------------------------------------------------------------------------------------------------------------------------|

# Usage

Refer to [Simulate Scenario documentation](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/docs/solution-pack-guide.md) to understand how to simulate and reset scenarios. 
 
To understand the process FortiSOAR follows to respond to stolen credentials threat, we have included a scenario &mdash; **Stolen Credential Leading to Data Exfiltration** with this solution pack. Refer to the section *Stolen Credential Leading to Data Exfiltration* to understand how this solution pack's automation addresses your needs. 

## Stolen Credential Leading to Data Exfiltration

This scenario generates example alerts of following types in FortiSOAR's **Alerts** module. 

- Firewall Configuration Change
- Domain User Created
- User Group Changed
- Schedule Task Created
- Data Exfiltration
- Password Reset

Navigate to the example alerts and observe the following:

1. An attacker has gained access to the Firewall using a leaked credential.
2. The attacker then modifies the firewall configuration to allow RDP Access and laterally moves to a Windows box.
3. The attacker creates a new domain account as a backdoor for subsequent access and also exfiltrates data.

Click to open the alert *Password Reset*. This alert is usually considered benign, however, a closer look indicates possible malicious intent.

1. Click to open **Comments** tab under **Workspace** pane and observe multiple comments highlighting hostile indicators (`jack` and `10.0.1.11`)
2. Click to open **Recommendations** tab under **Workspace** pane and observe that &ndash; because of common indicators &ndash; alerts suggest firewall configuration change .
3. Select all suggested alerts and click **Escalate** to escalate them to an **Incident**.
    - Navigate to **Incident Response** > **Incidents** and click to open the newly-created incident.
    - Scroll down and click to open the **Correlations** tab. The graph shows the outbound data transfer.

![Select Scenario](https://github.com/fortinet-fortisoar/solution-pack-stolen-credential-leading-to-data-exfiltration/raw/develop/docs/res/attackFlow.png)
