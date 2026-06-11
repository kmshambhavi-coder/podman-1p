
# McAfeeNSM

McAfee Network Security Platform is a next-generation intrusion prevention system (IPS) that redefines how organizations block advanced threats.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|None|https://x.x.x.x/sdkapi/|
|Username||True|String||
|Password||True|Password|*****|
|Domain ID||True|String||
|Siemplify Policy Name||True|String||
|Sensors Names List Comma Separated||True|String|sensor_name1,sensor_name2,sensor_name3|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.6-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|idna-3.11-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|certifi-2026.2.25-py3-none-any.whl|


## Actions
#### Block IP
Block IP address
Timeout - 600 Seconds



#### Get Alert Info Data
Get alert data by id.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Alert ID|True|String|None|
|Sensor Name|Sensor Name|True|String|None|



##### JSON Results
```json
{"name": "MALWARE: Blacklisted File Detected", "assignTo": "---", "description": {"definition": "A McAfee-maintained blacklist that is dynamically updated with Callback Detectors updates.", "signatures": [{"conditions": "null"}], "componentAttacks": "null", "target": "ServerOrClient", "reference": {"cveId": "[]", "certId": "null", "bugtraqId": "[]", "nspId": "0x4840c300", "microsoftId": "[]", "additionInfo": "null", "arachNidsId": "[]"}, "protocals": "[smtp, ftp, http]", "comments": {"availabeToChildDomains": "true", "parentDomainComments": "null", "comments": ""}, "rfSB": "No", "attackCategory": "Malware", "attackSubCategory": "---", "protectionCategory": "[Malware/Bot]", "httpResponseAttack": "No", "btf": "Medium"}, "summary": {"destination": "null", "zoombie": "null", "target": {"ipAddrs": "1.1.1.1", "risk": "N/A", "country": "India", "networkObject": "---", "hostName": "null", "vmName": "null", "proxyIP": "1.1.1.1", "user": "Unknown", "os": "---", "port": 41128}, "attacker": {"ipAddrs": "1.1.1.1", "risk": "N/A", "country": "India", "networkObject": "---", "hostName": "null", "vmName": "null", "proxyIP": "1.1.1.1", "user": "Unknown", "os": "---", "port": 80}, "cAndcServer": "null", "source": "null", "compromisedEndpoint": "null", "attackedHIPEndpoint": {"ipAddrs": "1.1.1.1", "risk": "N/A", "country": "India", "networkObject": "---", "hostName": "null", "vmName": "null", "proxyIP": "1.1.1.1", "user": "Unknown", "os": "---", "port": 41128}, "fastFluxAgent": "null", "event": {"domain": "My Company", "protocol": "http", "zone": "null", "alertId": "2246015847757997493", "attackCount": 1, "vlan": "-11", "direction": "Inbound", "detection": "Signature", "application": "HTTP", "device": "NS9100-50", "result": "Inconclusive", "time": "Jan 04, 2016 09:50:39", "relevance": "Unknown", "matchedPolicy": "CustomFP_Engine_With_AlertOnly", "interface": "G3/1-G3/2"}}, "details": {"malwareFile": {"engine": "Manager Blacklist", "fileHash": "3f3f7c3b9722912ddeddf006cff9d9d0", "malwareConfidence": "Very High", "malwareName": "null", "fileName": "/Firewall.cpl", "size": "6144 bytes"}, "exceededThreshold": "null", "callbackDetectors": "null", "layer7": {"httpReturnCode": 200, "httpURI": "/Firewall.cpl", "httpRequestMethod": "GET", "httpServerType": "Apache/2.2.13 (Fedora) Last - Modified: Wed, 10 Oct 2012 05: 19: 15 GMT ", "httpHostHeader": "null", "httpUserAgent": "Wget/1.11.4 (Red Hat modified)"}, "portScan": "null", "sqlInjection": "null", "triggeredComponentAttacks": "null", "hostSweep": "null", "matchedSignature": "null", "communicationRuleMatch": "null", "fastFlux": "null"}, "alertState": "UnAcknowledged", "uniqueAlertId": "6245941293374080682"}
```



#### Is IP Blocked
Check if an IP address is blocked
Timeout - 600 Seconds



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Quarantine IP
Quarantine a particular IP address
Timeout - 600 Seconds



#### Unblock IP
Unblock a particular IP address
Timeout - 600 Seconds









