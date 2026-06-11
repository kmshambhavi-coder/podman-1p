
# CBProtection

Cb Protection delivers application control and critical infrastructure protection to lock down servers, critical systems and fixed-function devices in highly regulated environments.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|None|https://x.x.x.x|
|Api Key||True|String||


#### Dependencies
| |
|-|
|solrq-1.1.2-py2.py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|pyyaml-6.0.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|validators-0.35.0-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|
|types_python_dateutil-2.9.0.20260518-py3-none-any.whl|
|six-1.17.0-py2.py3-none-any.whl|
|idna-3.15-py3-none-any.whl|
|cachetools-7.1.3-py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|pygments-2.20.0-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|protobuf-7.35.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|pika-1.4.0-py3-none-any.whl|
|packaging-26.2-py3-none-any.whl|
|wcwidth-0.7.0-py3-none-any.whl|
|prompt_toolkit-3.0.52-py3-none-any.whl|
|cbapi-1.7.10-py2.py3-none-any.whl|


## Actions
#### Analyze File
Analyze a file
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Connector Name|The name of the analyzing connector. e.g. Palo Alto Networks|True|String||
|Priority|The priority of the analysis (-2 to 2)|True|String||
|Timeout|Wait timeout. e.g. 120|True|String||



##### JSON Results
```json
[{"EntityResult": {"computerId": 1, "connectorId": 2, "analysisStatus": 0, "dateCreated": "2019-01-17T09:17:41.663Z", "priority": 0, "createdByUserId": 0, "is_malicious": "True", "pathName": "c:\\\\temp\\\\test.conf", "fileCatalogId": 12345, "createdBy": "admin", "analysisResult": 0, "dateModified": "2019-01-17T09:30:28.053Z", "fileName": "test.exe", "id": 1, "analysisTarget": ""}, "Entity": "FSFSD213CGJK3423423FCFS33dFSV123"}]
```



#### Block Hash
Block a hash on specific policies or globally
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Names|e.g. Default Policy,Local Approval Policy|False|String||



#### Change Computer Policy
Move a computer to a new policy
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|The new policy name. e.g. Default Policy|True|String||



#### Find File
Find a file instance on multiple computers
Timeout - 600 Seconds



##### JSON Results
```json
[{"executed": "true", "fileName": "test.exe", "computerId": 1, "unifiedSource": "null", "policyId": 1, "detailedLocalState": 3, "dateCreated": "2018-05-29T10:09:27Z", "topLevel": "false", "certificateId": 0, "pathName": "c:\\\\test", "localState": 3, "initialized": "true", "detachedCertificateId": 33, "detachedPublisherId": 8, "fileInstanceGroupId": 1, "id": 12345, "fileCatalogId": 12345}]
```



#### Get Computers By File
Get the computers on which a file with the given SHA-256 value exists
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": "00:50:56:11:22:33", "Entity": "macAddress"}, {"EntityResult": 0, "Entity": "systemMemoryDumps"}, {"EntityResult": "Agent did not receive all the rules yet", "Entity": "policyStatusDetails"}, {"EntityResult": "False", "Entity": "prioritized"}, {"EntityResult": 1, "Entity": "platformId"}, {"EntityResult": "None", "Entity": "upgradeErrorTime"}, {"EntityResult": 0, "Entity": "tdCount"}, {"EntityResult": "False", "Entity": "hasDuplicates"}, {"EntityResult": 60, "Entity": "disconnectedEnforcementLevel"}, {"EntityResult": "False", "Entity": "hasHealthCheckErrors"}, {"EntityResult": 100, "Entity": "syncPercent"}, {"EntityResult": 0, "Entity": "agentQueueSize"}, {"EntityResult": "1.1.1.1", "Entity": "agentVersion"}, {"EntityResult": 0, "Entity": "activeDebugLevel"}, {"EntityResult": "True", "Entity": "tamperProtectionActive"}, {"EntityResult": 0, "Entity": "refreshFlags"}, {"EntityResult": 0, "Entity": "cbSensorFlags"}, {"EntityResult": "None", "Entity": "templateCloneCleanupMode"}, {"EntityResult": 2, "Entity": "activeKernelDebugLevel"}, {"EntityResult": "None", "Entity": "description"}, {"EntityResult": "Default Policy", "Entity": "policyName"}, {"EntityResult": 60, "Entity": "enforcementLevel"}, {"EntityResult": "None", "Entity": "templateDate"}, {"EntityResult": 6, "Entity": "previousPolicyId"}, {"EntityResult": 8192, "Entity": "memorySize"}, {"EntityResult": 1212, "Entity": "clVersion"}, {"EntityResult": 1, "Entity": "id"}, {"EntityResult": "Approvals out of date", "Entity": "policyStatus"}, {"EntityResult": 2200.0, "Entity": "processorSpeed"}, {"EntityResult": 0, "Entity": "ccFlags"}, {"EntityResult": "False", "Entity": "template"}, {"EntityResult": "False", "Entity": "initializing"}, {"EntityResult": "False", "Entity": "uninstalled"}, {"EntityResult": 0, "Entity": "upgradeErrorCount"}, {"EntityResult": 0, "Entity": "templateComputerId"}, {"EntityResult": 55, "Entity": "daysOffline"}, {"EntityResult": "None", "Entity": "upgradeError"}, {"EntityResult": "False", "Entity": "automaticPolicy"}, {"EntityResult": "WORKGROUP\\\\TEST$,Window Manager\\\\TEST-4", "Entity": "users"}, {"EntityResult": "Windows Server 2012", "Entity": "osShortName"}, {"EntityResult": "False", "Entity": "deleted"}, {"EntityResult": 100, "Entity": "initPercent"}, {"EntityResult": "False", "Entity": "templateTrackModsOnly"}, {"EntityResult": 16, "Entity": "activeDebugFlags"}, {"EntityResult": "TEST-TEST-TEST-TEST", "Entity": "CLIPassword"}, {"EntityResult": "2018-05-29T10:10:19.26Z", "Entity": "dateCreated"}, {"EntityResult": "Yes", "Entity": "virtualized"}, {"EntityResult": 0, "Entity": "agentMemoryDumps"}, {"EntityResult": "False", "Entity": "connected"}, {"EntityResult": -1, "Entity": "debugLevel"}, {"EntityResult": "None", "Entity": "cbSensorVersion"}, {"EntityResult": "Up to date", "Entity": "upgradeStatus"}, {"EntityResult": "False", "Entity": "localApproval"}, {"EntityResult": "False", "Entity": "isActive"}, {"EntityResult": "WORKGROUP\\\\TEST", "Entity": "name"}, {"EntityResult": 0, "Entity": "debugFlags"}, {"EntityResult": "VMware", "Entity": "virtualPlatform"}, {"EntityResult": "None", "Entity": "computerTag"}, {"EntityResult": "2018-11-22T10:49:41.583Z", "Entity": "lastRegisterDate"}, {"EntityResult": 0, "Entity": "debugDuration"}, {"EntityResult": 0, "Entity": "cbSensorId"}, {"EntityResult": 0, "Entity": "SCEPStatus"}, {"EntityResult": 43432, "Entity": "agentCacheSize"}, {"EntityResult": 4, "Entity": "processorCount"}, {"EntityResult": "VMware Virtual Platform", "Entity": "machineModel"}, {"EntityResult": "Microsoft Windows Server 2012 R2 x64 Server Standard (Evaluation) (6.3.9600)", "Entity": "osName"}, {"EntityResult": "None", "Entity": "templateCloneCleanupTimeScale"}, {"EntityResult": 1, "Entity": "policyId"}, {"EntityResult": "False", "Entity": "forceUpgrade"}, {"EntityResult": "2018-11-23T21:59:12.613Z", "Entity": "lastPollDate"}, {"EntityResult": "None", "Entity": "templateCloneCleanupTime"}, {"EntityResult": "True", "Entity": "supportedKernel"}, {"EntityResult": 0, "Entity": "kernelDebugLevel"}, {"EntityResult": 0, "Entity": "ccLevel"}, {"EntityResult": "1.1.1.1", "Entity": "ipAddress"}, {"EntityResult": "Intel(R) Xeon(R) CPU E5-2630 v4 @ 2.20GHz", "Entity": "processorModel"}, {"EntityResult": 8, "Entity": "syncFlags"}]
```



#### Get System Info
Get information about a computer
Timeout - 600 Seconds



##### JSON Results
```json
{"macAddress": "00:50:56:11:22:33", "systemMemoryDumps": 0, "policyStatusDetails": "Agent did not receive all the rules yet", "prioritized": "False", "platformId": 1, "upgradeErrorTime": "None", "tdCount": 0, "hasDuplicates": "False", "disconnectedEnforcementLevel": 60, "hasHealthCheckErrors": "False", "syncPercent": 100, "agentVersion": "8.0.0.2562", "activeDebugLevel": 0, "templateCloneCleanupMode": "None", "processorCount": 4, "kernelDebugLevel": 0, "refreshFlags": 0, "activeKernelDebugLevel": 2, "users": "WORKGROUP\\\\TEST$,Window Manager\\\\TEST-4", "policyName": "Default Policy", "enforcementLevel": 60, "templateDate": "None", "previousPolicyId": 6, "memorySize": 8192, "machineModel": "VMware Virtual Platform", "id": 1, "policyStatus": "Approvals out of date", "processorSpeed": 2200.0, "ccFlags": 0, "template": "False", "initializing": "False", "initPercent": 100, "uninstalled": "False", "computerTag": "None", "templateComputerId": 0, "daysOffline": 55, "upgradeError": "None", "automaticPolicy": "False", "description": "None", "osShortName": "Windows Server 2012", "deleted": "False", "localApproval": "False", "tamperProtectionActive": "True", "lastPollDate": "2018-11-23T21:59:12.613Z", "activeDebugFlags": 16, "CLIPassword": "TEST-TEST-TEST-TEST", "dateCreated": "2018-05-29T10:10:19.26Z", "virtualPlatform": "VMware", "connected": "False", "supportedKernel": "True", "debugLevel": -1, "cbSensorVersion": "None", "upgradeStatus": "Up to date", "upgradeErrorCount": 0, "isActive": "False", "debugFlags": 0, "agentMemoryDumps": 0, "name": "WORKGROUP\\\\TEST", "lastRegisterDate": "2018-11-22T10:49:41.583Z", "ipAddress": "1.1.1.1", "cbSensorId": 0, "SCEPStatus": 0, "agentCacheSize": 43432, "cbSensorFlags": 0, "clVersion": 1212, "osName": "Microsoft Windows Server 2012 R2 x64 Server Standard (Evaluation) (6.3.9600)", "templateCloneCleanupTimeScale": "None", "policyId": 1, "forceUpgrade": "False", "templateTrackModsOnly": "False", "templateCloneCleanupTime": "None", "agentQueueSize": 0, "virtualized": "Yes", "ccLevel": 0, "debugDuration": 0, "processorModel": "Intel(R) Xeon(R) CPU E5-2630 v4 @ 2.20GHz", "syncFlags": 8}
```



#### Ping
Test connectivity
Timeout - 600 Seconds



#### Unblock Hash
Unblock a hash on specific policies or globally.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Names|Separated by comma. e.g. Default Policy,Local Approval Policy|False|String||










Readme text