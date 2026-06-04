
# CheckPointThreatReputation

Leverage the Check Pointâ€™s threat intelligence to enrich your SIEM and SOAR solutions and to secure your business applications and websites by using simple RESTful APIs.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://rep.checkpoint.com|
|API Key||True|Password|*****|
|Verify SSL||False|Boolean||


#### Dependencies
| |
|-|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|


## Actions
#### Get Host Reputation
Enrich the Siemplify Host entity based on the information from the CheckPoint Threat Reputation service.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if the returned risk value for entity is above a given threshold.|True|String||
|Create Insight?|Specify whether the Siemplify Insight should be created based on the action result.|False|Boolean||



#### Get IP Reputation
Enrich Siemplify IP entity based on the information from the CheckPoint Threat Reputation service.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if the returned risk value for entity is above a given threshold.|True|String||
|Create Insight?|Specify whether the Siemplify Insight should be created based on the action result.|False|Boolean||



#### Get File Hash Reputation
Enrich Siemplify File hash entity based on the information from the CheckPoint Threat Reputation service. Action accepts file hashes in md5, sha1 and sha256 formats.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if the returned risk value for entity is above a given threshold.|True|String||
|Create Insight?|Specify whether the Siemplify Insight should be created based on the action result.|False|Boolean||



#### Ping
Test connectivity to the CheckPoint Threat Reputation service with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds










Readme text