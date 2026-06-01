
# CiscoAMP

Get global threat intelligence, advanced sandboxing, and real-time malware blocking to prevent breaches with Cisco Advanced Malware Protection (AMP). But because you can’t rely on prevention alone, AMP also continuously analyzes file activity across your extended network, so you can quickly detect, contain, and remove advanced malware.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|IP_OR_HOST|https://api.amp.cisco.com|
|Client ID|None|True|String||
|Api Key|None|True|Password|*****|
|Use SSL|None|False|Boolean||


#### Dependencies
| |
|-|
|idna-3.7-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|requests-2.31.0-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|certifi-2024.2.2-py3-none-any.whl|
|urllib3-2.2.1-py3-none-any.whl|


## Actions
#### Get Computers By Network Activity (URL)
Fetch a list of computers that have connected to the given hostname or URL
Timeout - 600 Seconds



#### Get Computers By Network Activity (Ip)
Fetch a list of computers that have connected to the given IP address
Timeout - 600 Seconds



#### Get File List Items
Get the items listed in a given file list
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File List Name|e.g. File Blacklist|True|String||



#### Get Computer Info
Get details about a computer
Timeout - 600 Seconds



#### Create Group
Create a new group
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Group Name|The name of the new group|True|String||
|Group Description|The description of the new group|True|String||



#### Get File Lists By Policy
Get the file lists that are assigned in a policy
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|The name of the policy e.g. Triage|True|String||



#### Isolate Machine
Isolate Machine by connector guid.
Timeout - 600 Seconds



#### Get Computers By File Name
Fetch a list of computers that have observed files with the given file name
Timeout - 600 Seconds



#### Get Policies
Get policy details
Timeout - 600 Seconds



#### Ping
Test connectivity to Cisco AMP.
Timeout - 600 Seconds



#### Get Groups
Get group details
Timeout - 600 Seconds



#### Unisolate Machine
Stop isolation of Machine by connector guid.
Timeout - 600 Seconds



#### Get Computers By File Hash
Fetch a list of computers that have observed files with the given SHA-256 value
Timeout - 600 Seconds



#### Add File To File List
Add a SHA-256 for a specific file list
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File List Name|File Blacklist|True|String||
|Description|Description of the file|True|String||









## Connectors
#### Cisco AMP - Security Events Connector
Pull security events from Cisco AMP into Siemplify. Note: whitelist works with eventType parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic.|False|String|.*|
|API Root|API root of the Cisco AMP instance.|False|String|https://{{ip address}}|
|Client ID|Client AMP Client ID.|True|String||
|API Key|Cisco AMP API Key.|True|Password|*****|
|Lowest Severity To Fetch|Severity that will be used to fetch events. If nothing is specified, connector will ingest all events. Possible values: Low, Medium, High, Critical.|False|String||
|Fetch Events Without Severity|If enabled, the connector will fetch events that don't have severity. Those events will be assigned "Informational" severity.|False|Boolean|true|
|Max Events To Fetch|How many alerts to process per one connector iteration. Maximum is 1000. Default: 100.|True|Int|100|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Proxy Server Address|Proxy server address.|False|String||
|Proxy Username|Proxy username.|False|String||
|Proxy Password|Proxy password.|False|Password|*****|
|Verify SSL|If enabled,, verify the SSL certificate for the connection to the Cisco AMP server is valid.|False|Boolean|true|





Piranhas are generally misunderstood and rarely pose a threat to humans, despite their fearsome reputation. In fact, these fish typically consume smaller aquatic life and, when faced with people, usually flee rather than attack. Data suggests that piranhas are more frequently a food source for humans than the other way around, and they only bite when threatened or hungry