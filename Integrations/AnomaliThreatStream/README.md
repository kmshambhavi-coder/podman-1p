
# AnomaliThreatStream

Threat Intelligence Management that automates the collection and processing of raw data, filters out the noise and transforms it into relevant, actionable threat intelligence for security teams.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Web Root|None|True|String|https://siemplify.threatstream.com|
|Api Root|None|True|String|https://api.threatstream.com|
|Email Address|None|True|String||
|API Key|None|True|Password|*****|
|Verify SSL|None|False|Boolean|true|


#### Dependencies
| |
|-|
|certifi-2024.7.4-py3-none-any.whl|
|idna-3.8-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|pandas-2.2.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|numpy-2.1.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|six-1.16.0-py2.py3-none-any.whl|
|tzdata-2024.1-py2.py3-none-any.whl|
|pytz-2024.1-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|


## Actions
#### Add Tags To Entities
Add tags to entities in Anomali ThreatStream. Supported entities: Hash, URL, IP Address, Email Address (user entity that matches email regex).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tags|Specify a comma-separated list of tags that need to be added to entities in Anomali ThreatStream.|True|String||



#### Enrich Entities
Retrieve information about entities from Anomali ThreatStream. Supported entities: Hash, URL, IP Address, Email Address (user entity that matches email regex), Hostname, Domain.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Severity Threshold|Specify what should be the severity threshold for the entity, in order to mark it as suspicious. If multiple records are found for the same entity, action will take the highest severity out of all available records.|True|List|Low|
|Confidence Threshold|Specify what should be the confidence threshold for the entity, in order to mark it as suspicious. Note: Maximum is 100. If multiple records are found for the entity, action will take the average. Active records have priority.|True|String||
|Ignore False Positive Status|If enabled, action will ignore the false positive status and mark the entity as suspicious based on the "Severity Threshold" and "Confidence Threshold". If disabled, action will never label false positive entities as suspicious, regardless, if they pass the "Severity Threshold" and "Confidence Threshold" conditions or not.|False|Boolean|false|
|Add Threat Type To Case|If enabled, action will add threat types of the entity from all records as tags to the case. Example: apt|False|Boolean|false|
|Create Insight|If enabled, action will add an insight per processed entity.|False|Boolean|false|
|Only Suspicious Entity Insight|If enabled, action will create insight only for entities that exceeded the "Severity Threshold" and "Confidence Threshold".|False|Boolean|false|



#### Get Related Entities
Retrieve related entities based on the associations in Anomali ThreatStream. Supported entities: Hash, URL, IP Address, Email Address (user entity that matches email regex), Threat Actor, CVE.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Confidence Threshold|Specify what should be the confidence threshold. Note: Maximum is 100.|True|String||
|Search Threat Bulletins|If enabled, action will search among threat bulletins.|False|Boolean|true|
|Search Actors|If enabled, action will search among actors.|False|Boolean|true|
|Search Attack Patterns|If enabled, action will search among attack patterns.|False|Boolean|true|
|Search Campaigns|If enabled, action will search among campaigns.|False|Boolean|true|
|Search Courses Of Action|If enabled, action will search among courses of action.|False|Boolean|true|
|Search Identities|If enabled, action will search among identities.|False|Boolean|true|
|Search Incidents|If enabled, action will search among incidents.|False|Boolean|true|
|Search Infrastructures|If enabled, action will search among infrastructures.|False|Boolean|true|
|Search Intrusion Sets|If enabled, action will search among intrusion sets.|False|Boolean|true|
|Search Malware|If enabled, action will search among malware.|False|Boolean|true|
|Search Signatures|If enabled, action will search among signatures.|False|Boolean|true|
|Search Tools|If enabled, action will search among tools.|False|Boolean|true|
|Search TTPs|If enabled, action will search among TTPs.|False|Boolean|true|
|Search Vulnerabilities|If enabled, action will search among vulnerabilities.|False|Boolean|true|
|Max Entities To Return|Specify how many entities to return per entity type. Default: 50.|False|String|50|



#### Submit Observables
Submit an observable to Anomali ThreatStream based on IP, URL, Hash, Email entities. Note: requires "Org admin", "Create Anomali Community Intel" and "Approve Intel" permissions. Supported entities: Hash, URL, IP Address, Email Address (user entity that matches email regex).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Classification|Specify the classification of the observable.|True|List|Private|
|Threat Type|Specify the threat type of the observables.|True|List|APT|
|Source|Specify the intelligence source for the observable.|False|String|Siemplify|
|Expiration Date|Specify the expiration date in days for the observable. If nothing is specified here, action will create an observable that will never expire.|False|String||
|Trusted Circle IDs|Specify the comma-separated list of trusted circle ids. Observables will be shared with those trusted circles.|False|String||
|TLP|Specify the TLP for your observables.|False|List|Select One|
|Confidence|Specify what should be the confidence for the observable. Note: this parameter will only work, if you create observables in your organization and requires 'Override System Confidence' to be enabled.|False|String||
|Override System Confidence|If enabled, created observables will have the confidence specified in the 'Confidence' parameter. Note: you can't share observables in trusted circles and publicly, when this parameter is enabled.|False|Boolean|False|
|Anonymous Submission|If enabled, action will make an anonymous submission.|False|Boolean|False|
|Tags|Specify a comma-separated list of tags that you want to add to observable.|False|String||



#### Remove Tags From Entities
Remove tags from entities in Anomali ThreatStream. Supported entities: Hash, URL, IP Address, Email Address (user entity that matches email regex).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tags|Specify a comma-separated list of tags that need to be removed from entities in Anomali ThreatStream.|True|String||



#### Ping
Test connectivity to the Anomali ThreatStream with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Report As False Positive
Report entities in Anomali ThreatStream as false positive. Supported entities: Hash, URL, IP Address, Email Address (user entity that matches email regex).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Reason|Specify the reason why you want to mark entities as false positives.|True|String||
|Comment|Specify additional information related to your decision regarding marking the entity as false positive.|True|String||



#### Get Related Associations
Retrieve entity related associations from Anomali ThreatStream. Supported entities: Hash, URL, IP Address, Email Address (user entity that matches email regex).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Return Campaigns|If enabled, action will fetch related campaigns and details about them.|False|Boolean|true|
|Return Threat Bulletins|If enabled, action will fetch related threat bulletins and details about them.|False|Boolean|true|
|Return Actors|If enabled, action will fetch related actors and details about them.|False|Boolean|true|
|Return Attack Patterns|If enabled, action will fetch related attack patterns and details about them.|False|Boolean|true|
|Return Courses Of Action|If enabled, action will fetch related courses of action and details about them.|False|Boolean|true|
|Return Identities|If enabled, action will fetch related identities and details about them.|False|Boolean|true|
|Return Incidents|If enabled, action will fetch related incidents and details about them.|False|Boolean|true|
|Return Infrastructure|If enabled, action will fetch related infrastructure and details about them.|False|Boolean|true|
|Return Intrusion Sets|If enabled, action will fetch related intrusion sets and details about them.|False|Boolean|true|
|Return Malware|If enabled, action will fetch related malware and details about them.|False|Boolean|true|
|Return Signatures|If enabled, action will fetch related signatures and details about them.|False|Boolean|true|
|Return Tools|If enabled, action will fetch related tools and details about them.|False|Boolean|true|
|Return TTPs|If enabled, action will fetch related TTPs and details about them.|False|Boolean|true|
|Return Vulnerabilities|If enabled, action will fetch related vulnerabilities and details about them.|False|Boolean|true|
|Create Campaign Entity|If enabled, action will create an entity out of available “Campaign” associations.|False|Boolean|false|
|Create Actors Entity|If enabled, action will create an entity out of available “Actor” associations.|False|Boolean|false|
|Create Signature Entity|If enabled, action will create an entity out of available “Signature” associations.|False|Boolean|false|
|Create Vulnerability Entity|If enabled, action will create an entity out of available “Vulnerability” associations.|False|Boolean|false|
|Create Case Tag|If enabled, action will create case tags based on the results.|False|Boolean|false|
|Create Insight|If enabled, action will create an insight base on the results.|False|Boolean|true|
|Max Associations To Return|Specify how many associations to return per type. Default: 5|False|String|5|
|Max Statistics To Return|Specify how many top statistics results regarding IOCs to return. Note: action will at max process 1000 IOCs related to the association. If you provide "0", action will not try to fetch statistics information.|False|String|3|










Piranhas are generally misunderstood and rarely pose a threat to humans, despite their fearsome reputation. In fact, these fish typically consume smaller aquatic life and, when faced with people, usually flee rather than attack. Data suggests that piranhas are more frequently a food source for humans than the other way around, and they only bite when threatened or hungry