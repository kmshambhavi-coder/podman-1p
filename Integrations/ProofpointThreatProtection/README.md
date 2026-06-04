
# ProofpointThreatProtection

Proofpoint Threat Protection is an email gateway that scans and classifies messages to block malware, BEC, and other cyber threats.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|The API Root of the Proofpoint Threat Protection instance.|True|String||
|Client ID|The client ID associated with your Proofpoint Threat Protection API credentials.|True|String||
|Client Secret|The client secret associated with your Proofpoint Threat Protection API credentials.|True|Password|*****|
|Cluster ID|The cluster ID associated with your Proofpoint Threat Protection API instance.|True|String||
|Verify SSL|If selected, the integration validates the SSL certificate when connecting to the Proofpoint Threat Protection server. Enabled by default.|False|Boolean|true|


#### Dependencies
| |
|-|
|typing_extensions-4.15.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|httpcore-1.0.9-py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|google_auth_httplib2-0.3.0-py3-none-any.whl|
|proto_plus-1.27.1-py3-none-any.whl|
|anyio-4.12.1-py3-none-any.whl|
|pyasn1-0.6.2-py3-none-any.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|cryptography-46.0.4-cp311-abi3-manylinux_2_34_x86_64.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|google_auth-2.47.0-py3-none-any.whl|
|EnvironmentCommon-1.0.3-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|TIPCommon-2.3.0-py3-none-any.whl|
|charset_normalizer-3.4.4-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|googleapis_common_protos-1.72.0-py3-none-any.whl|
|idna-3.11-py3-none-any.whl|
|protobuf-6.33.5-cp39-abi3-manylinux2014_x86_64.whl|
|google_api_core-2.29.0-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|google_api_python_client-2.188.0-py3-none-any.whl|
|certifi-2026.1.4-py3-none-any.whl|


## Actions
#### Add Entry To Block List
Use the "Add Entry To Block List" action to add a new entry to the block list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Cluster ID|The cluster ID of the block list. If no value is provided, the action uses the cluster ID from the integration configuration.|False|String||
|Blocklist Item|The JSON object representing the block list item to add.|True|String|{
    "action": "add",
    "attribute": "",
    "operator": "",
    "value": "",
    "comment": ""
}|



#### Add IOC To Allow List
Use the "Add IOC To Allow List" action to add specific IOCs to the Proofpoint Threat Protection allow list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Cluster ID|The cluster ID of the allow list. If no value is provided, the action uses the cluster ID from the integration configuration.|False|String||
|Recipient Email Address|A comma-separated list of recipient email addresses to add to the allow list.|False|String||
|Sender Email Address|A comma-separated list of sender email addresses to add to the allow list.|False|String||
|Sender IP Address|A comma-separated list of sender IP addresses to add to the allow list.|False|String||
|Sender Hostname|A comma-separated list of sender hostnames to add to the allow list.|False|String||
|Sender HELO Domain Name|A comma-separated list of HELO domain names to add to the allow list.|False|String||
|Message Header From (Address Only)|A comma-separated list of "Message Header From" entries to add to the allow list.|False|String||
|Comment|A description or justification associated with the allow list entries.|False|String||



#### Get Block List Entries
Use the "Get Block List Entries" action to get entries from the block list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Cluster ID|The cluster ID of the block list. If no value is provided, the action uses the Cluster ID from the integration configuration.|False|String||
|IOC Type To Return|The types of IOCs to return. If All is selected, the action returns all entries.|False|List|All|
|Max IOCs To Return|The number of IOCs to return. Maximum: 1000.|False|String|100|



#### Add IOC To Block List
Use the "Add IOC To Block List" action to add specific IOCs to the Proofpoint Threat Protection block list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Cluster ID|The cluster ID of the block list. If no value is provided, the action uses the cluster ID from the integration configuration.|False|String||
|Recipient Email Address|A comma-separated list of recipient email addresses to add to the block list.|False|String||
|Sender Email Address|A comma-separated list of sender email addresses to add to the block list.|False|String||
|Sender IP Address|A comma-separated list of sender IP addresses to add to the block list.|False|String||
|Sender Hostname|A comma-separated list of sender hostnames to add to the block list.|False|String||
|Sender HELO Domain Name|A comma-separated list of HELO domain names to add to the block list.|False|String||
|Message Header From (Address Only)|A comma-separated list of "Message Header From" entries to add to the block list.|False|String||
|Comment|A description or justification associated with the block list entries.|False|String||



#### Add Entry To Allow List
Use the "Add Entry To Allow List" action to add a new entry to the allow list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Cluster ID|The cluster ID of the allow list. If no value is provided, the action uses the cluster ID from the integration configuration.|False|String||
|Allowlist Item|The JSON object representing the allow list item to add.|True|String|{
    "action": "add",
    "attribute": "",
    "operator": "",
    "value": "",
    "comment": ""
}|



#### Remove Entry From Allow List
Use the "Remove Entry From Allow List" action to remove entry from the allow list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Cluster ID|The cluster ID of the allow list. If no value is provided, the action uses the cluster ID from the integration configuration.|False|String||
|IOC Type To Search|The types of IOCs to search for. If All is selected, the action removes all entries matching the value.|False|List|All|
|Value|The value to remove from the allow list.|True|String||
|Case Insensitive Search|If selected, the action performs a case-insensitive search to identify and remove all matching entries.|True|List|True|



#### Get Allow List Entries
Use the "Get Allow List Entries" action to get entries from the allow list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Cluster ID|The cluster ID of the allow list. If no value is provided, the action uses the cluster ID from the integration configuration.|False|String||
|IOC Type To Return|The types of IOCs to return. If All is selected, the action returns all entries.|False|List|All|
|Max IOCs To Return|The number of IOCs to return. Maximum: 1000.|False|String|100|



#### Ping
Use the Ping action to test the connectivity to Proofpoint Threat Protection.
Timeout - 600 Seconds



#### Remove Entry From Block List
Use the "Remove Entry From Block List" action to remove entry from the block list.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Cluster ID|The cluster ID of the block list. If no value is provided, the action uses the cluster ID from the integration configuration.|False|String||
|IOC Type To Search|The types of IOCs to search for. If All is selected, the action removes all entries matching the value.|False|List|All|
|Value|The value to remove from the block list.|True|String||
|Case Insensitive Search|If selected, the action performs a case-insensitive search to identify and remove all matching entries.|True|List|True|









