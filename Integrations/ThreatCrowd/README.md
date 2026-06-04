
# ThreatCrowd

ThreatCrowd is a system for finding and researching artifacts relating to cyber threats.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Use SSL|None|False|Boolean||



## Actions
#### Ping
Test Connectivity
Timeout - 600 Seconds



#### EnrichEntities
Quickly identify related infrastructure and malware
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"permalink": "https: //www.threatcrowd.org/ip.php?ip=1.1.1.1", "response_code": "1", "votes": -1, "references": ["http: //www.talosintelligence.com/feeds/ip-filter.blf", "https: //check.torproject.org/exit-addresses", "https: //otx.alienvault.com/pulse/56714a2867db8c3f8a46fe95/"], "hashes": [], "resolutions": [{"domain": "afplink.net", "last_resolved": "2016-06-24"}, {"domain": "jabber.zwiebeltoralf.de", "last_resolved": "2016-12-28"}]}, "Entity": "1.1.1.1"}]
```









