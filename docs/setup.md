| [Home](https://github.com/fortinet-fortisoar/solution-pack-stolen-credential-leading-to-data-exfiltration/blob/develop/README.md) |
|-----------------------------------------------------------------------------------------------------------------------------------|

# Installation

1. To install a solution pack, click **Content Hub** > **Discover**.
2. From the list of solution pack that appears, search for and select **Stolen Credential Leading to Data Exfiltration**.
3. Click the **Stolen Credential Leading to Data Exfiltration** solution pack card.
4. Click **Install** on the bottom to begin installation.

## Prerequisites

| Solution Pack Name | Purpose                                                  |
|:-------------------|:---------------------------------------------------------|
| SOAR Framework     | Required for Incident Response modules                   |
| SOC Simulator      | Required for Scenario Module and SOC Simulator connector |

# Configuration

For optimal performance of **Stolen Credential Leading to Data Exfiltration** solution pack, you can install and configure:

- A directory service to retrieve information about users, groups, and computers, in an organization
    - To configure and use the Active Directory connector as a directory service, refer to [Configuring Active Directory Connector](https://docs.fortinet.com/document/fortisoar/2.2.0/active-directory/154/active-directory-v2-2-0#Configuration_parameters)
- A SIEM solution
    - To configure and use the Fortinet FortiSIEM connector as a source of data ingestion, refer to [Configuring Fortinet FortiSIEM](https://docs.fortinet.com/document/fortisoar/4.3.2/fortinet-fortisiem/278/fortinet-fortisiem-v4-3-2)
