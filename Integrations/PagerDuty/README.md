
# PagerDuty

PagerDuty helps developers, ITOps, DevOps and teams across the business  provide a perfect digital experience to their customers, every time.

Python Version - V3_11
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
#### Get Incident By ID
Get The incident details by providing the incident ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident Key|Incident Key|True|String|Incident Key|
|Email|Email|True|String|Email|



#### Get User By ID
Get The user details by providing the user ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|UserID||True|String|test|



#### Snooze Incident
Snooze an incident from the providing ID and returns info about the incident.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email||True|String|tcondello@siemplify.co|
|IncidentID|IncidentID|True|String|IncidentID|



#### Run Response Play
Run a specified response play on a given incident - Deprecated.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email||True|String|test@example.com|
|Response ID||True|String|test|
|Incident_ID|Incident ID|True|String|Default|



#### List Users
Get the list of all the Users associated with the hostname Parameters.
Timeout - 600 Seconds



#### List Incidents
Get the list of all Incidents associated with the hostname Parameters.
Timeout - 600 Seconds



#### Get User By Email
Get The user details by providing the user Email.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Email||True|String|test@example.com|



#### Create Incident
Create a new incident with the given parameters.

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Details||True|String|A disk is getting full on this machine. You should investigate what is causing the disk to fill, and ensure that there is an automated process in place for ensuring data is rotated (eg. logs should have logrotate around them). If data is expected to stay on this disk forever, you should start planning to scale up to a larger disk.|
|Title||True|String|The server is on fire.|
|Email||True|String|tcondello@siemplify.co|
|Urgency||True|String|high|



#### List All OnCall
Get the list of OnCalls associated with the hostname Parameters.

Timeout - 600 Seconds



#### Filtered Incident List
Use filters to found a specific incident.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Additional_Data|Additional details to include.|False|MultipleChoiceParameter||
|sort_by|Pick one of the Four options and decide in which order asc or desc|False|MultipleChoiceParameter||
|Urgencies|Urgencies|False|MultipleChoiceParameter||
|User_IDS|it can be more than one|False|String|None|
|Team_IDS|it can be more than one|False|String||
|Incident_Key|Incident_Key|False|String|None|
|Incidents_Statuses|Incidents_Statuses|False|MultipleChoiceParameter||
|Data_Range|Data_Range|False|String||
|Until|Date format YYYY-MM-DD|False|String||
|Since|Date format YYYY-MM-DDMaximum range is 6 months|False|String||
|Email|Email|True|String|Email|
|Service_IDS|Service_IDS|False|String|None|



#### Ping
Test connectivity to the PagerDuty API.
Timeout - 600 Seconds









## Connectors
#### PagerDutyConnector
The connector pulls events from the Pagerduty API https://developer.pagerduty.com/api-reference/9d0b4b12e36f9-list-incidents.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|acknowledge|Boolean flag to enable acknowledging the incident in PagerDuty. NOTE: The apikey must have permissions to modify incidents or the connector will fail.|False|Boolean|true|
|apiKey|API Key to interact with PagerDuty API|True|String|null|




