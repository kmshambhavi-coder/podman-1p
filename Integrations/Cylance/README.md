
# Cylance

BlackBerry Cylance is an advanced threat protection platform that, unlike other traditional endpoint protection software, makes no use of malware signatures. Instead, it employs techniques such as machine learning and artificial intelligence, which allows the identification of malicious code based on its behavior. This ensures protection even against zero-day codes, malware that has never been seen before. Among its key features, Cylance includes: True zero-day prevention, AI-driven malware prevention, Script management, Device usage policy enforcement, Memory exploitation detection and prevention, Application control for fixed-function devices

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address||True|String|https://<server-address>|
|Application ID||True|String||
|Application Secret||True|Password|*****|
|Tenant Identifier||True|String||


#### Dependencies
| |
|-|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|pytz-2022.1-py2.py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|PyJWT-2.8.0-py3-none-any.whl|


## Actions
#### Change Policy
Change the policy of an endpoint to an existing policy
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|The new policy name|True|String||



#### Add To Global List
Add a hash to one of the two global lists: GlobalSafe or GlobalQuarantine
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Type|The list to add the hash to. e.g. GlobalSafe|True|String|GlobalSafe|
|Category|The category of the hash|False|String|None|
|Reason|The reason for adding the hash to the list|False|String||



#### Delete From Global List
Remove a hash for the specified global list (GlobalSafe or GlobalQuarantine)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Type|The list to delete the hash from. e.g. GlobalSafe|True|String||



#### Get Threat
Enrich a hash with data from Cylance
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if the threat Cylance score pass the given threshold. e.g. 3|True|String|0|



#### Get Threats
Retrieve a list of all available threats in the system
Timeout - 600 Seconds



#### Get Threat Devices
Get threats associated to a particular hostname or an IP address
Timeout - 600 Seconds



#### Enrich Entities
Enrich hostnames and IP addresses with additional data from Cylance
Timeout - 600 Seconds



#### Get Threat Download Link
Action fetches The URL you can use to download the file. The action only provides the URL, it does not download the file for you.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat SHA256 Hash|Threat SHA256 hashes, in a comma separated list. Note - if parameter value will be left empty, action will use file hash entities as input.|False|String||



#### Change Zone
Change zone for an endpoint (group of endpoints)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Zones to Add|The new Zone to add. Comma separated.|False|String||
|Zones to Remove|The Zone to be removed. Comma separated.|False|String||



#### Get Global List
Retrieve a list of all hashes in the specified global list (GlobalSafe or GlobalQuarantine)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Type|Name of the global list. e.g. GlobalSafe|True|String||



#### Ping
Test connectivity to Cylance
Timeout - 600 Seconds









## Connectors
#### Cylance connector
Cylance connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|https://<instance>.cylance.com|True|String||
|Application Secret| Used to sign the Application ID|True|Password|*****|
|Application ID|Used to indicate the token requested|True|String||
|Tenant Identifier|ID number of tenant information being queried|True|String||
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




