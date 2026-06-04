
# PaloAltoPanorama

Panorama network security management simplifies management tasks while delivering comprehensive controls and deep visibility into network-wide traffic and security threats

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|String|https://x.x.x.x/api|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean|True|


#### Dependencies
| |
|-|
|six-1.17.0-py2.py3-none-any.whl|
|defusedxml-0.7.1-py2.py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|xmltodict-0.13.0-py2.py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|bs4-0.0.2-py2.py3-none-any.whl|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|python_dateutil-2.8.2-py2.py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|soupsieve-2.8.3-py3-none-any.whl|


## Actions
#### Unblock ips in policy
Unblock IP addresses in a given policy
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|Specify name of the device. The default device name for Palo Alto Panorama is localhost.localdomain. Visit action documentation to get more insights on where you can find this value.|True|String||
|Device Group Name|Specify name of the device group. Visit action documentation to get more insights on where you can find this value.|True|String||
|Policy Name|Specify name of the policy.|True|String||
|Target|Specify what should be the target. Possible values: source, destination.|True|String||



#### Commit Changes
Action commits changes in Palo Alto Panorama. Note: In order to use "Only My Changes" option, the user must be an admin.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Only My Changes|If enabled, action will only commit changes that were done by the current user.|False|Boolean|true|



#### Push Changes
Push commits of a device group in Palo Alto Panorama. Note: It can take several minutes before changes are pushed. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Group Name|The device group in which the rule is located, e.g: LCaas. For viewing the available device group names in a given device, please refer to https://<PANORAMA IP>/php/rest/browse.php/config::devices::entry[@name='<DEVICE_NAME>']::device-group.|True|String||



#### Remove Ips from group
Remove IP addresses from an address group
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|Specify name of the device. The default device name for Palo Alto Panorama is localhost.localdomain. Visit action documentation to get more insights on where you can find this value.|True|String||
|Device Group Name|Specify name of the device group. Visit action documentation to get more insights on where you can find this value.|True|String|LCaaS|
|Address Group Name|Specify name of the address group.|True|String||



#### Edit Blocked Applications
Block and unblock applications. Each application is added to or removed from a given policy
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Applications To Block|Specify what kind of application should be blocked. Example: apple-siri,windows-azure.|False|String||
|Applications To UnBlock|Specify what kind of application should be unblocked. Example: apple-siri,windows-azure.|False|String||
|Device Name|Specify name of the device. The default device name for Palo Alto Panorama is localhost.localdomain. Visit action documentation to get more insights on where you can find this value.|True|String||
|Device Group Name|Specify name of the device group. Visit action documentation to get more insights on where you can find this value.|True|String||
|Policy Name|Specify name of the policy.|True|String||



#### Unblock Urls
Remove URLs from a given URL category.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|Specify name of the device. The default device name for Palo Alto Panorama is localhost.localdomain. Visit action documentation to get more insights on where you can find this value.|True|String||
|Device Group Name|Specify name of the device group. Visit action documentation to get more insights on where you can find this value.|True|String||
|URL Category Name|Specify name of the URL Category.|True|String||



#### Search logs
Search logs in Palo Alto Panorama based on the query.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Log Type|Specify which log type should be returned.|True|List|Traffic|
|Query|Specify what query filter should be used to return logs.|False|String||
|Max Hours Backwards|Specify the amount of hours from where to fetch logs.|False|String||
|Max Logs to Return|Specify how many logs to return. Maximum is 1000.|False|String|50|



#### Get Correlated Traffic Between IPs
Action returns correlated network traffic logs from Palo Alto Panorama between Source IP Address and Destination IP Address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Source IP|Specify source IP that will be used to get traffic.|True|String||
|Destination IP|Specify destination IP that will be used to get traffic.|True|String||
|Max Hours Backwards|Specify the amount of hours from where to fetch logs.|False|String||
|Max Logs to Return|Specify how many logs to return. Maximum is 1000.|False|String|50|



#### Add Ips to group
Add IP addresses to an address group
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|Specify name of the device. The default device name for Palo Alto Panorama is localhost.localdomain. Visit action documentation to get more insights on where you can find this value.|True|String||
|Device Group Name|Specify name of the device group. Visit action documentation to get more insights on where you can find this value.|True|String||
|Address Group Name|Specify name of the address group.|True|String||



#### Block ips in policy
Block IP addresses in a given policy
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|Specify name of the device. The default device name for Palo Alto Panorama is localhost.localdomain. Visit action documentation to get more insights on where you can find this value.|True|String||
|Device Group Name|Specify name of the device group. Visit action documentation to get more insights on where you can find this value.|True|String||
|Policy Name|Specify name of the policy.|True|String||
|Target|Specify what should be the target. Possible values: source, destination.|True|String||



#### Get Blocked Applications
List all blocked applications in a given policy
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|Specify name of the policy.|True|String||
|Device Name|Specify name of the device. The default device name for Palo Alto Panorama is localhost.localdomain. Visit action documentation to get more insights on where you can find this value.|True|String|localhost.localdomain|
|Device Group Name|Specify name of the device group. Visit action documentation to get more insights on where you can find this value.|True|String||



#### Block Urls
Add URLs to a given URL category. Note:  You need to create a policy and add desired URL category to that policy in order to block the URL
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|Specify name of the device. The default device name for Palo Alto Panorama is localhost.localdomain. Visit action documentation to get more insights on where you can find this value.|True|String||
|Device Group Name|Specify name of the device group. Visit action documentation to get more insights on where you can find this value.|True|String||
|URL Category Name|Specify name of the URL Category.|True|String||



#### Ping
Test connectivity to Panorama
Timeout - 600 Seconds









## Connectors
#### Palo Alto Panorama - Threat Log Connector
Connector ingests threat logs based on the specified query filter and connector parameters.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of Palo Alto Panorama instance.|True|String|https://x.x.x.x:x/api|
|Username|Username of the Palo Alto Panorama account.|True|String||
|Password|Password of the Palo Alto Panorama account.|True|Password|*****|
|Query Filter|Specify additional filters in the query. Please refer to connector documentation to get additional information.|False|String||
|Lowest Severity To Fetch|Lowest severity that will be used to fetch threat logs. Possible values: Informational, Low, Medium, High, Critical.|True|String||
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve logs from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Logs To Fetch|How many logs to process per one connector iteration.|False|Int|25|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Palo Alto Panorama server is valid.|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use|False|String||
|Proxy Username|The proxy username to authenticate with|False|String||
|Proxy Password|The proxy password to authenticate with|False|Password|*****|




