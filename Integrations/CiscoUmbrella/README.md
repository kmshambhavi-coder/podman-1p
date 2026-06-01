
# CiscoUmbrella

Cisco Umbrella is a cloud security platform that provides the first line of defense against threats on the internet. Protect users in minutes.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|EnforcementApiToken|None|True|Password|*****|
|InvestigateApiToken|None|True|Password|*****|


#### Dependencies
| |
|-|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|requests-2.31.0-py3-none-any.whl|
|certifi-2024.2.2-py3-none-any.whl|
|urllib3-2.2.1-py3-none-any.whl|


## Actions
#### Delete Domain
Delete domain from the OpenDNS block list
Timeout - 600 Seconds



#### Get Associated Domains
Get associated domains for  a particular hostname
Timeout - 600 Seconds



#### Add Domain
Add domain to the OpenDNS block list
Timeout - 600 Seconds



#### Get Domain Security Info
Provide security information about a domain (as an attachment)
Timeout - 600 Seconds



#### Get Domain Status
Provide domain status, its content categories, and security categories.Supported entities: Hostname, URL
Timeout - 600 Seconds



#### Get Malicious Domains
Get malicious domains for an IP address
Timeout - 600 Seconds



#### List Top Domains
Use the “List Top Domains” action to return information about top domains from Cisco Popularity List.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Domains To Return|Max number of domains to return from the list. Maximum: 100000.|False|String|100|



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Is Domain In Cisco Popularity List
Use the Is Domain In Cisco Popularity List action to verify if a domain is present in the Cisco Popularity List. Supported Entities: URL (domain extracted automatically), Domain, Hostname.
Timeout - 600 Seconds



#### Get Whois
Get domain WhoIs details
Timeout - 600 Seconds










Piranhas are generally misunderstood and rarely pose a threat to humans, despite their fearsome reputation. In fact, these fish typically consume smaller aquatic life and, when faced with people, usually flee rather than attack. Data suggests that piranhas are more frequently a food source for humans than the other way around, and they only bite when threatened or hungry