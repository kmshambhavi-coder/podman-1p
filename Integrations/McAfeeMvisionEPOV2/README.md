
# McAfeeMvisionEPOV2

McAfee MVISION ePO reduces incident response times, strengthens protection, and simplifies risk and security management using automation and end-to-end security visibility. McAfeeÂ® manages the platform infrastructure, upgrades, and maintenance.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|None|https://api.mvision.mcafee.com|
|Client ID|None|True|String||
|Client Secret|None|True|Password|*****|
|API Key|None|True|Password|*****|
|Scopes|None|True|String|epo.device.r epo.device.w epo.evt.r epo.taggroup.r epo.taggroup.w epo.tags.r epo.tags.w mi.user.investigate soc.inv.ade|
|IAM Root|None|False|None|https://iam.mcafee-cloud.com|
|Verify SSL|None|False|Boolean|True|


#### Dependencies
| |
|-|
|certifi-2024.7.4-py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|EnvironmentCommon-1.0.0-py3-none-any.whl|
|charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|


## Actions
#### Add Tag To Device
Add tag to the device in McAfee Mvision ePO V2.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tag Name|Specify what tag you want to add to endpoint.|True|String||



#### Enrich Endpoint
Fetch device's system information by its hostname or IP address.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity": "172.30.202.6", "EntityResult": {"id": "1022660", "type": "devices", "links": {"self": "https://api.mvision.mcafee.com/epo/v2/devices/1022660"}, "attributes": {"name": "TIP-HW-H038", "parentId": 1001021, "agentGuid": "935CDA39-88B5-4E33-A253-80F33241BFDD", "lastUpdate": "2020-11-10T13:49:53.803+00:00", "agentState": 0, "nodePath": null, "agentPlatform": "Windows 10:10:0:0", "agentVersion": "5.6.6.317", "nodeCreatedDate": "2020-11-10T11:20:50.750+00:00", "managed": "1", "tenantId": 11526, "tags": "Escalated, Server, Workstation", "excludedTags": "", "managedState": 1, "computerName": "TIP-HW-H038", "domainName": "WORKGROUP", "ipAddress": "172.30.202.6", "osType": "Windows 10", "osVersion": "10.0", "cpuType": "Intel(R) Xeon(R) CPU E5-2698 v3 @ 2.30GHz", "cpuSpeed": 2300, "numOfCpu": 2, "totalPhysicalMemory": 4294430720, "macAddress": "005056A2667F", "userName": "Admin", "osPlatform": "Workstation", "ipHostName": "TIP-HW-H038", "isPortable": "non-portable"}, "relationships": {"assignedTags": {"links": {"self": "https://api.mvision.mcafee.com/epo/v2/devices/1022660/relationships/assignedTags", "related": "https://api.mvision.mcafee.com/epo/v2/devices/1022660/assignedTags"}}, "installedProducts": {"links": {"self": "https://api.mvision.mcafee.com/epo/v2/devices/1022660/relationships/installedProducts", "related": "https://api.mvision.mcafee.com/epo/v2/devices/1022660/installedProducts"}}}}}]
```



#### List Devices
List devices that are available in McAfee Mvision ePO V2.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Devices to Return|Specify how many devices to return.|False|String|100|



##### JSON Results
```json
[{"id": "1022656", "type": "devices", "links": {"self": "https://api.mvision.mcafee.com/epo/v2/devices/1022656"}, "attributes": {"name": "CLDBGQAEO0777", "parentId": 1001022, "agentGuid": "D8E8F120-6C25-4BEF-9F15-01080BFFCBFA", "lastUpdate": "2020-11-10T14:16:42.027+00:00", "agentState": 0, "nodePath": null, "agentPlatform": "Windows Server 2016:10:0:0", "agentVersion": "5.6.6.317", "nodeCreatedDate": "2020-11-10T11:13:11.567+00:00", "managed": "1", "tenantId": 11526, "tags": "Escalated, Server", "excludedTags": "", "managedState": 1, "computerName": "CLDBGQAEO0777", "domainName": "WORKGROUP", "ipAddress": "10.254.47.44", "osType": "Windows Server 2016", "osVersion": "10.0", "cpuType": "Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz", "cpuSpeed": 2594, "numOfCpu": 6, "totalPhysicalMemory": 25874055168, "macAddress": "005056AF3F4E", "userName": "Cloudadmin", "osPlatform": "Server", "ipHostName": "CLDBGQAEO0777", "isPortable": "non-portable"}, "relationships": {"assignedTags": {"links": {"self": "https://api.mvision.mcafee.com/epo/v2/devices/1022656/relationships/assignedTags", "related": "https://api.mvision.mcafee.com/epo/v2/devices/1022656/assignedTags"}}, "installedProducts": {"links": {"self": "https://api.mvision.mcafee.com/epo/v2/devices/1022656/relationships/installedProducts", "related": "https://api.mvision.mcafee.com/epo/v2/devices/1022656/installedProducts"}}}}]
```



#### List Tags
List tags that are available in McAfee Mvision ePO V2.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Tags to Return|Specify how many tags to return.|False|String|100|



##### JSON Results
```json
[{"id": "295127", "type": "tags", "links": {"self": "https://api.mvision.mcafee.com/epo/v2/tags/295127"}, "attributes": {"uniqueKey": "epo.tag.server", "name": "Server", "family": "EPO", "notes": "Default tag for systems identified as a Server", "criteria": "( where ( eq EPOComputerProperties.OSPlatform \"Server\" ) )", "whereClause": "where ( [EPOComputerProperties].[OSPlatform] = 'Server' )", "executeOnAsci": "1", "createdBy": "system", "createdOn": "2020-11-10T10:15:10.710+00:00", "modifiedBy": "system", "modifiedOn": "2020-11-10T10:15:10.710+00:00", "tagGroupId": 23533}, "relationships": {"tagGroup": {"links": {"self": "https://api.mvision.mcafee.com/epo/v2/tags/295127/relationships/tagGroup", "related": "https://api.mvision.mcafee.com/epo/v2/tags/295127/tagGroup"}}, "devices": {"links": {"self": "https://api.mvision.mcafee.com/epo/v2/tags/295127/relationships/devices", "related": "https://api.mvision.mcafee.com/epo/v2/tags/295127/devices"}}}}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Remove Tag From Device
Remove tag from the device in McAfee Mvision ePO V2.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tag Name|Specify what tag  you want to remove from endpoint.|True|String||









## Connectors
#### McAfee Mvision EPO V2 - Events Connector
Pull events from McAfee Mvision EPO V2.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|threattype|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Root|API Root of the McAfee Mvision EPO V2 account.|True|String|https://api.mvision.mcafee.com|
|IAM Root|IAM Root of the McAfee Mvision EPO V2 API.|True|String|https://iam.mcafee-cloud.com|
|Client ID|Client ID of the McAfee Mvision EPO V2 account.|True|String||
|Client Secret|Client Secret of the McAfee Mvision EPO V2 account.|True|Password|*****|
|API Key|API Key of the McAfee Mvision EPO V2 account.|True|Password|*****|
|Scopes|Scopes of the McAfee Mvision EPO V2 account.|False|String|epo.device.r epo.device.w epo.evt.r epo.taggroup.r epo.taggroup.w epo.tags.r epo.tags.w mi.user.investigate soc.inv.ade|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration.|True|Integer|50|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the CheckPoint Cloud Guard server is valid.|False|Boolean|true|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




