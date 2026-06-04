
# Bandura Cyber

Bandura delivers the threat intelligence automation and control needed for companies of all sizes to block known threats at massive scale, operationalize threat intelligence, and get more out of your existing security resources.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API Root|True|String|https://gmc.banduracyber.com/api/v1|
|Username|Username|True|String|danield@siemplify.co|
|Password|Password|True|Password|*****|
|Verify SSL|verify SSL|False|Boolean|true|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|DateTime-5.5-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|zope.interface-7.2-cp311-cp311-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|setuptools-80.9.0-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|pytz-2025.2-py2.py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|


## Actions
#### Get Denied IP Lists
Get a list of IPs in Denied IPv4 List
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Name|Name of the list to add the IP. (The List Name is Case Sensitive)|False|String|List Name|



#### Get Allowed Domain Lists
Get a list of Domains in an Allowed Domain List
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Name|Name of the list to add the IP. (The List Name is Case Sensitive)|False|String|List Name|



#### Add Domain to Allowed Lists
Add URL to Domain Allowed List in Bandura
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Name|Name of Allowed List to add the entity. (The List Name is Case Sensitive)|True|String|list|
|Description|Allowed List Entity Description|False|String|None|
|Expiration Date|Date you would like this entity to be removed from the list. Example Format: 2020-01-01T12:00:00.000+00:00|False|String|None|



#### Add IP to Denied Lists
Add IP to IPv4 Allowed List in Bandura
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Name|Name of Denied List to add the entity. (The List Name is Case Sensitive)|True|String|List Name|
|Description|Denied List Entity Description|False|String|None|
|Maskbit|Defined the range of ip addresses that you would like to add to the list.|False|String|32|
|Expiration Date|Date you would like this entity to be removed from the list. Example Format: 2020-01-01T12:00:00.000+00:00|False|String|None|



#### Add Domain to Denied Lists
Add URL to Domain Denied List in Bandura
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Name|Name of Denied List to add the entity. (The List Name is Case Sensitive)|True|String|List|
|Description|Denied List Entity Description|False|String|None|
|Expiration Date|Date you would like this entity to be removed from the list. Example Format: 2020-01-01T12:00:00.000+00:00|False|String|None|



#### Add IP to Allowed Lists
Add IP to IPv4 Allowed List in Bandura
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Name|Name of Allowed List to add the entity. (The List Name is Case Sensitive)|True|String|List Name|
|Description|Allowed List Entity Description|False|String|None|
|Maskbit|Defined the range of ip addresses that you would like to add to the list.|False|String|32|
|Expiration Date|Date you would like this entity to be removed from the list. Example Format: 2020-01-01T12:00:00.000+00:00|False|String|None|



#### Get Denied Domain Lists
Get a list of Domains in Denied Domain List
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Name|Name of the list to add the IP. (The List Name is Case Sensitive)|False|String|List Name|



#### Get Allowed IP Lists
Get a list of IPs in an Allowed IPv4 List
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Name|Name of the list to add the IP. (The List Name is Case Sensitive)|False|String|List Name|



#### Ping
Tests Connectivity to Bandura Cyber
Timeout - 600 Seconds









