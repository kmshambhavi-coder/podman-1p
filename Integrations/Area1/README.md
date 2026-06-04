
# Area1

Area 1 Horizon, a cloud-based service that stops phishing attacks across all traffic vectors—email, web, or network. Protects users against phishing emails using a cloud-based MTA or cloud APIs/connectors. Protects users against web-based phishing campaigns through a globally distributed, recursive DNS service. Shut downs phishing attacks at your network edge.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|String|https://api.area1security.com/|
|Username|None|True|String||
|Password|None|True|Password|*****|
|Verify SSL|None|False|Boolean||



## Actions
#### Get Recent Indicators
Get recent malicious indicators from Area1.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Seconds Back|Seconds Back|True|String||



#### Search Indicator
Search indicator on Area 1 by hash, URL, domain, IP, email.
Timeout - 600 Seconds



#### Ping
Test Area1 connectivity.
Timeout - 600 Seconds









