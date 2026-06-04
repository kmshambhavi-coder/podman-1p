
# CBLiveResponse

The VMware Carbon Black Endpoint Standard Live Response feature allows security operators to collect information and take action on remote endpoints with Carbon Black agents in real time.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|IP_OR_HOST|https://defense-<environment>.conferdeploy.net/|
|Organization Key||True|String||
|Carbon Black Cloud API ID||True|String||
|Carbon Black Cloud API Secret Key||True|Password|*****|
|Live Response API ID||False|String||
|Live Response API Secret Key||False|Password|*****|
|Use Live Response V6 API||False|Boolean|false|


#### Dependencies
| |
|-|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|


## Actions
#### Execute File
Execute file on a host running VMware CB Cloud Agent based on the Siemplify Host or IP entity. Note: The File name can be provided either as a Siemplify File entity (artifact) or as an action input parameter. If the File name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name is case insensitive. File name will be appended to Remote Directory Path to get the resulting file paths that CB Cloud API accepts. File Name also can be specified as a "full path" having both path and a file name, or having file name and file path as separate parameters
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Name|Specify the file name to execute. File name is case insensitive. File Name can be specified as a "full path" having both path and a file name, in that case Remote Directory Path parameter will not be used.|False|String||
|Remote Directory Path|Specify the remote directory path for the file to execute. Example: C:\TMP\|False|String||
|Output Log File on Remote Host|Specify the output log file action should save the redirected output to. Example: C:\TMP\cmdoutput.log|False|String||
|Command Arguments to Pass to File|Specify the command arguments to pass for executing the file. Example, here we specify "/C whoami" to execute whoami command with cmd: C:\Windows\system32\cmd.exe /C whoami|False|String||
|Wait for the Result|If enabled, action will wait for the command to complete.|False|Boolean|false|
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



#### List Files in Cloud Storage
List files in the VMware Carbon Black Cloud file storage for an existing live response session based on the Siemplify Host or IP entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Rows to Return|Specify how many rows action should return.|False|String|50|
|Start from Row|Specify from which row action should start to return data.|False|String|0|
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



#### Delete File
Delete a file from a host running VMware CB Cloud Agent based on the Siemplify Host or IP entity. Note: The File name can be provided either as a Siemplify File entity (artifact) or as an action input parameter. If the File name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name is case insensitive. File name will be appended to Remote Directory Path to get the resulting file paths that CB Cloud API accepts. File Name also can be specified as a "full path" having both path and a file name, or having file name and file path as separate parameters
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Remote Directory Path|Specify the remote directory path to file to delete. Example: C:\TMP\|False|String||
|File Name|Specify the file name to delete. File name is case insensitive. File Name can be specified as a "full path" having both path and a file name, in that case Remote Directory Path parameter will not be used.|False|String||
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



#### Create Memdump
Create memdump on a host running VMware CB Cloud Agent based on the Siemplify Host or IP entity. Note: The File name for the memdump to create can be provided either as a Siemplify File entity (artifact) or as an action input parameter. If the File name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name is case insensitive. File name will be appended to Remote Directory Path to get the resulting file paths that CB Cloud API accepts. Additionally, note that VMware CB API does not provide an error message if an unvalid Remote Directory Path is provided for the created memory dump.  File Name also can be specified as a "full path" having both path and a file name, or having file name and file path as separate parameters
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Name|Specify the file name for memdump creation. File name is case insensitive. File Name can be specified as a "full path" having both path and a file name, in that case Remote Directory Path parameter will not be used.|False|String||
|Remote Directory Path|Specify the directory file path to store the memdump. Example: C:\TMP\|False|String||
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



#### List Files
List files on a host running VMware CB Cloud Agent based on the Siemplify Host or IP entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Remote Directory Path|Specify the target directory path action should list. Example: C:\TMP\ or /tmp/|True|String||
|Max Rows to Return|Specify how many rows action should return.|False|String|50|
|Start from Row|Specify from which row action should start to return data.|False|String|0|
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



#### Put File
Put a file on a host running VMware CB Cloud Agent based on the Siemplify Host or IP entity. Note: The File name can be provided either as a Siemplify File entity (artifact) or as an action input parameter. If the File name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name is case insensitive. File name will be appended to both Source Directory Path and Destination Directory Path to get the resulting file paths that CB Cloud API accepts. File Name also can be specified as a "full path" having both path and a file name, or having file name and file path as separate parameters
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Name|Specify the file name to upload. File name is case insensitive. File Name can be specified as a "full path" having both path and a file name, in that case Source Directory Path parameter will not be used.|False|String||
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|
|Source Directory Path|Specify the source directory path action should take to get the file to upload. Example: /tmp/|False|String||
|Destination Directory Path|Specify the target directory path action should upload the file to. Example: C:\TMP\|True|String||



#### Kill Process
Kill process on a host based on the Siemplify Host or IP entity. Note: The Process name can be provided either as a Siemplify entity (artifact) or as an action input parameter. If the Process name is passed to action both as an entity (process) and input parameter - action will be executed on the input parameter.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Process Name|Process name to search PID for.|False|String||
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



#### Download File
Download a file from a host running VMware CB Cloud Agent based on the Siemplify Host or IP entity. Note: The File name can be provided either as a Siemplify File entity (artifact) or as an action input parameter. If the File name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name is case insensitive. File name will be appended to both Local Directory Path and Remote Directory Path to get the resulting file paths that CB Cloud API accepts. If action is executed against multiple Host or IP entities, to not overwrite the file downloaded from multiple entities, the downloaded file name is appended with Hostname or IP address, example format: hostname_filename. File Name also can be specified as a "full path" having both path and a file name, or having file name and file path as separate parameters
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Name|Specify the file name to download. File name is case insensitive. File Name can be specified as a "full path" having both path and a file name, in that case Remote Directory Path parameter will not be used.|False|String||
|Remote Directory Path|Specify the remote directory path action should take to download the file. Example: C:\TMP\|False|String||
|Local Directory Path|Specify the local directory path action should save the file to. Example: /tmp/|True|String||
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



#### List Processes
List processes running on endpoint based on the provided Siemplify Host or IP entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Process Name|Process name to search for on the host.|False|String||
|How Many Records To Return|How many records per entity action should return.|False|String|25|
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



#### Delete File from Cloud Storage
Delete a file from the VMware Carbon Black Cloud file storage for an existing live response session based on the Siemplify Host or IP entity. Note: This action is not supported in Carbon Black Live Response API v3, API v6 should be used to run this action. The File name can be provided either as a Siemplify File entity (artifact) or as an action input parameter. If the File name is passed to action both as an entity and input parameter - action will be executed on the input parameter. File name is case insensitive.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Name|Specify the file name to delete. File name is case insensitive.|False|String||
|Check for active session x times|How many attempts action should make to get active session for the entity. Check is made every 2 seconds.|True|String|20|



#### Ping
Test connectivity to the VMware Carbon Black Endpoint Standard Live Response with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds










Readme text