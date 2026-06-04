
# Mandiant

Mandiant is on a mission to make every organization secure from cyber threats and confident in their readiness. Mandiant delivers dynamic cyber defense solutions powered by industry-leading expertise, intelligence and innovative technology.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|UI Root|None|True|String|https://advantage.mandiant.com|
|API Root|None|True|String|https://api.intelligence.mandiant.com|
|Client ID|None|True|String||
|Client Secret|None|True|Password|*****|
|Verify SSL|None|False|Boolean|True|


#### Dependencies
| |
|-|
|requests-2.32.3-py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|idna-3.8-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Get Malware Details
Get information about malware from Mandiant.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Malware Names|Specify a comma-separated list of malware names that need to be enriched.|True|String||
|Create Insight|If enabled, action will create an insight containing information about the malware.|False|Boolean|true|
|Fetch Related IOCs|If enabled, action will fetch indicators that are related to the provided malware.|False|Boolean|true|
|Max Related IOCs To Return|Specify how many indicators action needs to process per malware. Default: 100.|False|String|100|



#### Get Related Entities
Get information about ioc related to entities using information from Mandiant. Supported entities: Hostname, IP Address, URL, File Hash, Threat Actor.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Lowest Severity Score|Specify the lowest severity score that will be used to return related indicators. Maximum: 100.|True|String|50|
|Max IOCs To Return|Specify how many indicators action needs to process per entity. Default: 100.|False|String|100|



#### Enrich IOCs
Get information about ioc related from Mandiant.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|IOC Identifiers|Specify a comma-separated list of IOCs that need to be enriched|True|String||



#### Enrich Entities
Enrich entities using information from Mandiant. Supported entities: Hostname, IP Address, URL, File Hash, Threat Actor, Vulnerability. Note: only MD5, SHA-1 and SHA-256 are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Severity Score Threshold|Specify the lowest severity score that will be used to mark the entity as suspicious. Note: only indicators (hostname, IP address, file hash, url) can be marked as suspicious. Maximum: 100.|True|String|50|
|Create Insight|If enabled, action will create an insight containing all of the retrieved information about the entity.|False|Boolean|true|
|Only Suspicious Entity Insight|If enabled, action will only create an insight for suspicious entities. Note: parameter "Create Insight" should be enabled. Insights for "Threat Actor" and "Vulnerability" entities will also be created even though they are not marked as suspicious.|False|Boolean|false|



#### Ping
Test connectivity to the Mandiant with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









