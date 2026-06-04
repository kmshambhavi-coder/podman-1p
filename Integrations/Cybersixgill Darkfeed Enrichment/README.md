
# Cybersixgill Darkfeed Enrichment

The most comprehensive IOC enrichment solution on the market. By enriching Google SecOps IOCs with Darkfeed, customers gain unparalleled context and essential explanations in order to accelerate their incident prevention and response. Block threats, enrich endpoint protection in real-time from the Google SecOps dashboard.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Client Id|description|True|String|clientid|
|Client Secret|description|True|Password|*****|


#### Dependencies
| |
|-|
|sixgill_clients-0.2.26-py2.py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Enrich IP
Enrich an IP using Sixgill Information (C&C server IP addresses for most prevalent malware and for servers involved in botnets, DDoS attacks, proxy anonymization, compromised RDP addresses and more.)
Timeout - 600 Seconds



#### Enrich Hash
Enrich a Hash using Sixgill information (Proactively analyze and investigate hashes of malware as they emerge on the dark web, including malware undetected by AV vendors)
Timeout - 600 Seconds



#### Enrich Domain
Enrich a Domain using Sixgill Information (Compromised site to which access is sold on the dark web. Suspicious domains that are for sale on the dark web.)
Timeout - 600 Seconds



#### Enrich Actor
Enrich a Threat Actor using Sixgill Information (Unpack a threat actor’s activity in the underground by seeing all IOCs they shared in the last 90 days. Understand their areas of activity, choice of targets and techniques.)
Timeout - 600 Seconds



#### Enrich URL
Enrich a URL using Sixgill Information (Identify, investigate, and download malware shared on the hosted on underground file-sharing/paste sites)
Timeout - 600 Seconds



#### Ping
Test Connectivity
Timeout - 600 Seconds









