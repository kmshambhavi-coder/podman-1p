
# PaloAltoPrismaCloud

Prisma Cloud is a Cloud Native Security Platform (CNSP) with broad security and compliance coverage – for applications, data, and the entire cloud native technology stack – throughout the development lifecycle and across multi- and hybrid-cloud environments.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the Palo Alto Prisma Cloud instance.|True|String|https://api3.prismacloud.io|
|Access Key ID|Access Key ID of the Palo Alto Prisma Cloud account.|True|String||
|Secret Access Key|Secret Access Key of the Palo Alto Prisma Cloud account.|True|Password|*****|
|Verify SSL|If checked, verifies that the SSL certificate for the connection to the Palo Alto Prisma Cloud server is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|requests-2.32.3-py3-none-any.whl|
|google_auth-2.35.0-py2.py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|TIPCommon-1.1.3.2-py2.py3-none-any.whl|
|pyasn1_modules-0.4.1-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|urllib3-2.2.3-py3-none-any.whl|
|cachetools-5.5.0-py3-none-any.whl|


## Actions
#### Respond To Alert
Respond to an alert in Palo Alto Prisma Cloud.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|ID of the response alert.|True|String||
|Response Type|Alert status. If the Snooze value is selected, the Snooze Time parameter is required. Possible values: Dismiss Snooze Reopen Remediate|False|List|Select One|
|Snooze Time|Snooze time in hours.|False|String||
|Dismiss Note|Note for a dismissal.|False|String||



#### Enrich Assets
Enrich information about a resource using Palo Alto Prisma Cloud.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Asset Identifiers|Comma-separated list of asset identifiers  which you want to fetch the details for. An asset identifier is either an Asset ID or Asset RRN.|True|String||



#### Ping
Test connectivity to the Palo Alto Prisma Cloud with parameters provided at the integration configuration page in the Chronicle Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### Palo Alto Prisma Cloud - Alerts Connector
Pull alerts from Palo Alto Prisma Cloud. Dynamic List works with the “policy.name” parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored.If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.Default is .* to catch all and return the value unchanged.Used to allow the user to manipulate the environment field via regex logic.If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of the Palo Alto Prisma Cloud instance.|True|String|https://api3.prismacloud.io|
|Access Key ID|Access key ID of the Palo Alto Prisma Cloud account.|True|String||
|Secret Access Key|Secret access key of the Palo Alto Prisma Cloud account.|True|Password|*****|
|Lowest Severity To Fetch|Lowest severity of the alerts to fetch. If no value is provided, the connector ingests alerts with all severities.Possible values: Critical, High, Medium, Low, Informational|False|String||
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Alerts To Fetch|Number of alerts to process per one connector iteration. Max value is 1000. Default value is 100.|False|Int|100|
|Use dynamic list as a blocklist|If checked, the dynamic list is used as a blocklist.|False|Boolean|false|
|Verify SSL|If checked, verifies that the SSL certificate for the connection to the Palo Alto Prisma Cloud server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




