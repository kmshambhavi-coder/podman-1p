
# FireEyeHX

The FireEye HX series is a threat prevention platform that helps drive faster, more accurate decisions about potential security incidents on endpoints.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|URL|https://x.x.x.x:<port>|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean||


#### Dependencies
| |
|-|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|six-1.17.0-py2.py3-none-any.whl|
|types_python_dateutil-2.9.0.20260408-py3-none-any.whl|
|TIPCommon-1.0.11.1-py2.py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Acknowledge Alert Groups
Acknowledge alert groups handled by Siemplify to better sync between HX platform and Siemplify. Note - you can acknowledge alert groups only , not alerts, via the HX API.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert Groups IDs|Specify the Alert Groups IDs you would like to Acknowledge.|True|String||
|Acknowledgment Comment|Specify the acknowledgment comment you would like to add to the relevant alert groups|False|String||
|Acknowledgment|Specify whether you would like to Acknowledge or Un-acknowledge the specified alert groups|True|List|Acknowledge|
|Limit|Specify the maximum amount of alert group listings coming back from the API, in the JSON result.|False|String||



#### Cancel Host Contain
Create a cancel host contain task on the FireEye HX server based on the Siemplify IP or Host Siemplify entities. Note: Action is not supported for Linux hosts by Fireye HX.
Timeout - 600 Seconds



#### Get Alerts in Alert Group
Get all the alerts found in the specified alert group.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert Group ID|Specify a comma-separated list of Alert Group IDs for which you want to retrieve alerts.|True|String||
|Limit|Specify the maximum amount of alerts listings coming back from the API, for the alert group. Default is 50.|False|String|50|



#### Get Host Alert Groups
List alert groups related to a host in FireEye HX. Supported entities: Hostname, IP Address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Acknowledgment Filter|Specify whether you want to return all of the alert groups or only acknowledged/unacknowledged.|False|List|ALL|
|Max Alert Groups To Return|Specify how many Alert Groups to return per entity. Default: 20.|False|String|20|



#### Get List of File Acquisitions For Host
Get list of file acquisitions requested for host from FireEye HX server. Action works on Host or IP Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Search Term|Searches all file acquisitions for hosts connected to the FireEye HX server. The search_term can be any condition value.|False|String|None|
|Limit|How many records action should return, for example, 100.|False|String|None|
|Filter Field|Lists only results with the specified field value, results can be filtered by external correlation identifier (external_id).|False|String|None|



#### Is Contain Malware Alerts
Check if malware alerts are listed for provided Siemplify Host or IP entities on FireEye HX server.
Timeout - 600 Seconds



#### Get Alert Group Details
Get full alert group details for provided Alert Group by it’s ID.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert Group ID|Specify a comma-separated list of Alert Group IDs for which you want to retrieve details.|True|String||



#### Get Host Info
Enrich Siemplify Host or IP entities based on the information from the FireEye HX.
Timeout - 600 Seconds



#### Get Indicator
Get information on specific Indicator from FireEye HX server.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Indicator Category|Specify indicator category uri_name value. uri_name can be found by running “Get Indicators” action. |True|String|None|
|Indicator Name|Specify indicator uri_name value. uri_name can be found by running “Get Indicators” action. |True|String|None|



#### Contain Host
Create contain host task on the FireEye HX server based on the Siemplify IP or Host Siemplify entities. Note: Action is not supported for Linux hosts by Fireye HX.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Approve Containment|Specify if containment request for host should be automatically approved to create contain host task on FireEye HX server. If not approved automatically, containment request can be approved in FireEye HX web console.|False|Boolean|false|



#### Get Indicators
Get information on indicators of compromise (IOC) from FireEye HX server based on provided search parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Indicator Category|The indicator category.|False|String|None|
|Search Term|The search term can be any name, category, signature, source, or condition value.|False|String|None|
|Limit|How many indicators action should return, for example, 100.|False|String|None|
|Share Mode|Filter indicators based on specific share mode. Available values: any, restricted, unrestricted, visible.|False|List|any|
|Sort By Field|Sorts the results by the specified field in ascending order.|False|String|None|
|Created by|Filter indicators based on author.|False|String|None|
|Has associated alerts|Specify if only indicators, which have associated alerts should be returned.|False|Boolean|None|



#### Get Alerts
Get FireEye HX alerts based on provided Siemplify entity and search conditions. Action works on Host or IP Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Limit|How many alerts action should return, for example, 100.|False|String||
|Has Share Mode|Filter alerts that were triggered from indicators with specific share mode. Available values: any, restricted, unrestricted.|False|List|any|
|Alert Resolution Status|Filter alerts based on alert resolution status. Available values: any, active_threat, alert, block, partial_block.|False|List|any|
|Alert reported in last x hours|Filter alerts reported in last x hours, for example last 4 hours.|False|String|None|
|Alert Source|Source of alert. Available values: any, exd (exploit detection), mal (malware alert), ioc (indicator of compromise).|False|List|any|
|Alert ID|Return specific alert by alert identifier.|False|String|None|



#### Ping
Test connectivity to the FireEye HX server with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### FireEye HX Alerts Connector
FireEye HX Alerts Connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|FireEye HX Server API Root URL.|True|String|https://x.x.x.x:<port>|
|Username|FireEye HX user to authenticate with.|True|String||
|Password|FireEye HX user password to authenticate with.|True|Password|*****|
|Offset time in hours|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|Int|24|
|Max Alerts Per Cycle|How many alerts should be processed during one connector run.|True|Int|25|
|Alert Type|Specify what FireEye HX alert types to ingest.  By default its set to active_threat to return alerts in ALERT and QUARANTINED/partial_block state. Other valid parameter is ALERT, which will return open alerts only.|False|String|active_threat|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If specified, connector will check if FireEye HX is configured with valid SSL certificate. If certificate is not valid, connector will return error.|False|Boolean|true|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|





Piranhas are generally misunderstood and rarely pose a threat to humans, despite their fearsome reputation. In fact, these fish typically consume smaller aquatic life and, when faced with people, usually flee rather than attack. Data suggests that piranhas are more frequently a food source for humans than the other way around, and they only bite when threatened or hungry