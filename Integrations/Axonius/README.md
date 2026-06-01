
# Axonius

Axonius is the cybersecurity asset management platform that gives organizations a comprehensive asset inventory, uncovers security solution coverage gaps, and automatically validates and enforces security policies. By seamlessly integrating with over 300 security and management solutions.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|String|https://{root}|
|API Key|None|True|String||
|API Secret|None|True|Password|*****|
|Verify SSL|None|False|Boolean|true|


#### Dependencies
| |
|-|
|certifi-2024.7.4-py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|


## Actions
#### Add Note
Add a note to entities in Axonius. Supported entities: Hostname, IP, Mac Address, User, Email Addresses (User entities that match email regex).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Note|Specify what note needs to be added.|True|String||



#### Add Tags
Add tags to entities in Axonius. Supported entities: Hostname, IP, Mac Address, User, Email Addresses (User entities that match email regex).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tags|Specify the comma-separated list of tags that need to be added to the entities.|True|String||



#### Enrich Entities
Enrich entities using information from Axonius. Supported entities: IP Address, Hostname, Mac Address, User, Email Addresses (User entities that match email regex).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Create Endpoint Insight|If enabled, action will create an insight containing information about the endpoints.|False|Boolean|True|
|Create User Insight|If enabled, action will create an insight containing information about the user.|False|Boolean|True|
|Max Notes To Return|Specify how many notes to show in the case wall table. Default: 50.|False|String|50|



#### Ping
Test connectivity to the Axonius with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Remove Tags
Remove tags from entities in Axonius. Supported entities: Hostname, IP, Mac Address, User, Email Addresses (User entities that match email regex).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tags|Specify the comma-separated list of tags that need to be removed from the entities.|True|String||










Piranhas are generally misunderstood and rarely pose a threat to humans, despite their fearsome reputation. In fact, these fish typically consume smaller aquatic life and, when faced with people, usually flee rather than attack. Data suggests that piranhas are more frequently a food source for humans than the other way around, and they only bite when threatened or hungry