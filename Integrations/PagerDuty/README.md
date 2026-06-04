
# PagerDuty

PagerDuty helps developers, ITOps, DevOps and teams across the business  provide a perfect digital experience to their customers, every time.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|api_key||True|Password|*****|
|Services||True|String|service|


#### Dependencies
| |
|-|
|protobuf-6.31.1-py3-none-any.whl|
|google_api_python_client-2.174.0-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|TIPCommon-2.2.7-py2.py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|google_api_core-2.25.1-py3-none-any.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|googleapis_common_protos-1.70.0-py3-none-any.whl|
|typing_extensions-4.14.0-py3-none-any.whl|
|pdpyras-5.4.0-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|google_auth-2.40.3-py2.py3-none-any.whl|
|anyio-4.9.0-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|


## Actions
#### List Users
Get the list of all the Users associated with the hostname Parameters.
Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Get Incident By ID
Get The incident details by providing the incident ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident Key|Incident Key|True|String|Incident Key|
|Email|Email|True|String|Email|



##### JSON Results
```json
{"incident_number": 1, "title": "TEST TEST server under attack", "description": "TEST TEST server under attack", "created_at": "2023-04-03T09:33:53Z", "status": "triggered", "incident_key": "8000bac7203042e0a569093a39d39b27", "service": {"id": "PE2WRHD", "type": "service_reference", "summary": "CommunityOnCall", "self": "https: //api.eu.pagerduty.com/services/PE2WRHD", "html_url": "https://google-com-2.eu.pagerduty.com/service-directory/PE2WRHD"}, "assignments": [{"at": "2023-04-03T09:33:53Z", "assignee": {"id": "PCRYIVB", "type": "user_reference", "summary": "Gal Pk", "self": "https://api.eu.pagerduty.com/users/PCRYIVB", "html_url": "https://google-com-2.eu.pagerduty.com/users/PCRYIVB"}}], "assigned_via": "escalation_policy", "last_status_change_at": "2023-04-03T09:33:53Z", "first_trigger_log_entry": {"id": "R3KU978DGL23224A6HDL9W2P47", "type": "trigger_log_entry_reference", "summary": "Triggered through the website.", "self": "https://api.eu.pagerduty.com/log_entries/R3KU978DGL23224A6HDL9W2P47", "html_url": "https://google-com-2.eu.pagerduty.com/incidents/Q1C5WQ0U8TSCXE/log_entries/R3KU978DGL23224A6HDL9W2P47"}, "alert_counts": {"all": 0, "triggered": 0, "resolved": 0}, "is_mergeable": true, "escalation_policy": {"id": "PMTZZA8", "type": "escalation_policy_reference", "summary": "Community OnCall-ep", "self": "https://api.eu.pagerduty.com/escalation_policies/PMTZZA8", "html_url": "https://google-com-2.eu.pagerduty.com/escalation_policies/PMTZZA8"}, "teams": [], "pending_actions": [], "acknowledgements": [], "basic_alert_grouping": null, "alert_grouping": null, "last_status_change_by": {"id": "PE2WRHD", "type": "service_reference", "summary": "Community OnCall", "self": "https://api.eu.pagerduty.com/services/PE2WRHD", "html_url": "https://google-com-2.eu.pagerduty.com/service-directory/PE2WRHD"}, "priority": null, "incidents_responders": [], "responder_requests": [], "subscriber_requests": [], "urgency": "high", "id": "Q1C5WQ0U8TSCXE", "type": "incident", "summary": "[#1] TEST TEST server under attack", "self": "https://api.eu.pagerduty.com/incidents/Q1C5WQ0U8TSCXE", "html_url": "https://google-com-2.eu.pagerduty.com/incidents/Q1C5WQ0U8TSCXE"}
```



#### Create Incident
Create a new incident with the given parameters.

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Details||True|String|A disk is getting full on this machine. You should investigate what is causing the disk to fill, and ensure that there is an automated process in place for ensuring data is rotated (eg. logs should have logrotate around them). If data is expected to stay on this disk forever, you should start planning to scale up to a larger disk.|
|Title||True|String|The server is on fire.|
|Email||True|String|tcondello@siemplify.co|
|Urgency||True|String|high|



##### JSON Results
```json
{"incident": {"incident_number": 5, "title": "TEST TEST 3", "description": "TEST TEST 3", "created_at": "2023-04-03T09:42:54Z", "status": "triggered", "incident_key": "4e529b3b3494498bba65e6f58e3ae8d7", "service": {"id": "PE2WRHD", "type": "service_reference", "summary": "Community OnCall", "self": "https://api.eu.pagerduty.com/services/PE2WRHD", "html_url": "https://google-com-2.eu.pagerduty.com/service-directory/PE2WRHD"}, "assignments": [{"at": "2023-04-03T09:42:54Z", "assignee": {"id": "PCRYIVB", "type": "user_reference", "summary": "Gal Pk", "self": "https://api.eu.pagerduty.com/users/PCRYIVB", "html_url": "https://google-com-2.eu.pagerduty.com/users/PCRYIVB"}}], "assigned_via": "escalation_policy", "last_status_change_at": "2023-04-03T09:42:54Z", "first_trigger_log_entry": {"id": "RS4E640MOTRXX7NN2STVY3C35D", "type": "trigger_log_entry_reference", "summary": "Triggered through the website.", "self": "https://api.eu.pagerduty.com/log_entries/RS4E640MOTRXX7NN2STVY3C35D", "html_url": "https://google-com-2.eu.pagerduty.com/incidents/Q1NJENORB5TPAU/log_entries/RS4E640MOTRXX7NN2STVY3C35D"}, "alert_counts": {"all": 0, "triggered": 0, "resolved": 0}, "is_mergeable": true, "escalation_policy": {"id": "PMTZZA8", "type": "escalation_policy_reference", "summary": "Community OnCall-ep", "self": "https://api.eu.pagerduty.com/escalation_policies/PMTZZA8", "html_url": "https://google-com-2.eu.pagerduty.com/escalation_policies/PMTZZA8"}, "teams": [], "impacted_services": [{"id": "PE2WRHD", "type": "service_reference", "summary": "Community OnCall", "self": "https://api.eu.pagerduty.com/services/PE2WRHD", "html_url": "https://google-com-2.eu.pagerduty.com/service-directory/PE2WRHD"}], "pending_actions": [], "acknowledgements": [], "basic_alert_grouping": null, "alert_grouping": null, "last_status_change_by": {"id": "PE2WRHD", "type": "service_reference", "summary": "Community OnCall", "self": "https://api.eu.pagerduty.com/services/PE2WRHD", "html_url": "https://google-com-2.eu.pagerduty.com/service-directory/PE2WRHD"}, "priority": null, "incidents_responders": [], "responder_requests": [], "subscriber_requests": [], "urgency": "low", "id": "Q1NJENORB5TPAU", "type": "incident", "summary": "[#5] TEST TEST 3", "self": "https://api.eu.pagerduty.com/incidents/Q1NJENORB5TPAU", "html_url": "https://google-com-2.eu.pagerduty.com/incidents/Q1NJENORB5TPAU", "body": {"details": "TEST TEST  3"}}}
```



#### Get User By Email
Get The user details by providing the user Email.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email||True|String|test@example.com|



##### JSON Results
```json
{}
```



#### Ping
Test connectivity to the PagerDuty API.
Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Filtered Incident List
Use filters to found a specific incident.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Additional_Data|Additional details to include.|False|None||
|sort_by|Pick one of the Four options and decide in which order asc or desc|False|None||
|Urgencies|Urgencies|False|None||
|User_IDS|it can be more than one|False|String|None|
|Team_IDS|it can be more than one|False|String||
|Incident_Key|Incident_Key|False|String|None|
|Incidents_Statuses|Incidents_Statuses|False|None||
|Data_Range|Data_Range|False|String||
|Until|Date format YYYY-MM-DD|False|String||
|Since|Date format YYYY-MM-DDMaximum range is 6 months|False|String||
|Email|Email|True|String|Email|
|Service_IDS|Service_IDS|False|String|None|



##### JSON Results
```json
{}
```



#### Run Response Play
Run a specified response play on a given incident - Deprecated.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email||True|String|test@example.com|
|Response ID||True|String|test|
|Incident_ID|Incident ID|True|String|Default|



##### JSON Results
```json
{}
```



#### List Incidents
Get the list of all Incidents associated with the hostname Parameters.
Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Get User By ID
Get The user details by providing the user ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|UserID||True|String|test|



##### JSON Results
```json
{}
```



#### List All OnCall
Get the list of OnCalls associated with the hostname Parameters.

Timeout - 600 Seconds



##### JSON Results
```json
{}
```



#### Snooze Incident
Snooze an incident from the providing ID and returns info about the incident.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email||True|String|tcondello@siemplify.co|
|IncidentID|IncidentID|True|String|IncidentID|



##### JSON Results
```json
{}
```









## Connectors
#### PagerDutyConnector
The connector pulls events from the Pagerduty API https://developer.pagerduty.com/api-reference/9d0b4b12e36f9-list-incidents.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|acknowledge|Boolean flag to enable acknowledging the incident in PagerDuty. NOTE: The apikey must have permissions to modify incidents or the connector will fail.|False|Boolean|true|
|apiKey|API Key to interact with PagerDuty API|True|String|null|
|DeviceProductField|The field name used to determine the device product|True|String|device_product|
|EventClassId|The field name used to determine the event name (sub-type)|True|String|event_name|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|30|




