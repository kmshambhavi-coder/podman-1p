
# CheckPointFirewall

VPN-1 is a firewall and VPN product developed by Check Point Software Technologies Ltd. VPN-1 is a stateful firewall which also filters traffic by inspecting the application layer.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address||True|IP|xx.xx.xx.xx:443|
|Username||True|String||
|Domain||False|String||
|Password||True|Password|*****|
|Policy Name||True|String|standard|
|Verify SSL||False|Boolean|None|


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
#### Add a SAM Rule
Add a SAM (suspicious activity monitoring) rule for Checkpoint Firewall. Please refer to the Checkpoint fw_sam command criteria section documentation for available ip, netmask, port and protocol combinations - https://sc1.checkpoint.com/documents/R80.40/WebAdminGuides/EN/CP_R80.40_CLI_ReferenceGuide/Content/Topics-CLIG/MDSG/fw-sam.htm
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Security Gateway to Create SAM Rule on|Specify the name of Security Gateway to create a rule for.|True|String||
|Source IP|Specify the source IP to be added to the rule.|False|String||
|Source Netmask|Specify the source netmask to be added to the rule.|False|String||
|Destination IP|Specify the destination IP to be added to the rule.|False|String||
|Destination Netmask|Specify the destination netmask to be added to the rule.|False|String||
|Port|Specify the port number to be added to the rule for example, 5005|False|String||
|Protocol|Specify the protocol name to be added to the rule for example, TCP|False|String||
|Expiration|Specify how long in seconds the newly added SAM rule should be active for example, 4. If nothing is specified - then the rule never expires.|False|String||
|Action for the Matching Connections|Specify the action that should be executed for the matching connections.|True|List|Drop|
|How to Track Matching Connections|Specify how to track matching connections.|True|List|Log|
|Close Connections|Specify if the existing matching connections should be closed.|False|Boolean|false|



#### List Layers On Site
Retrieve all of the available Access Control and Threat Prevention layers
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Layers To Return|Specify how many layers to return in the response. Default: 50.|False|String|50|



#### Remove IP From Group
Remove IP from the Checkpoint FireWall Group
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Blacklist Group Name|Specify the name of the group from which you want to remove IP address.|True|String||



#### Add Url To Group
Add Url to the Checkpoint FireWall Group
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|URLs Group Name|Specify the name of the group to which you want to add URL.|True|String||



#### Show Logs
Retrieve logs from CheckPoint FireWall based on the filter.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query Filter|Specify the query filter that will be used to return logs.|False|String||
|Time Frame|Specify what time frame should be used for log retrieval.|True|List|Last Hour|
|Log Type|Specify what type of logs should be returned.|True|List|Log|
|Max Logs To Return|Specify how many logs to return. Maximum is 100. This is Checkpoint FireWall limitation.|False|String|50|



#### Run Script
Run arbitrary script with CheckPoint run-script API call. Note: action is not using Siemplify entities to operate.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Script text|Script to execute. For example, fw sam command: fw sam -t 600 -I src 8.9.10.12|True|String||
|Target|Specify CheckPoint device to execute script on, for example: gaia80.10. Parameter accepts multiple values as a comma separated list.|True|String||



#### List Policies On Site
Retrieve all existing policies
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Policies To Return|Specify how many policies to return in the response. Default: 50.|False|String|50|



#### Remove SAM Rule
Remove a SAM (suspicious activity monitoring) rule from Checkpoint Firewall. Note: you need to match the current rule in order to remove it. Please refer to the Checkpoint fw_sam command criteria section documentation for available ip, netmask, port and protocol combinations - https://sc1.checkpoint.com/documents/R81/WebAdminGuides/EN/CP_R81_CLI_ReferenceGuide/Topics-CLIG/MDSG/fw-sam.htm
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Security Gateway|Specify the name of Security Gateway from where to remove SAM Rule|True|String||
|Source IP|Specify the source IP to be added to the rule.|False|String||
|Source Netmask|Specify the source netmask to be added to the rule.|False|String||
|Destination IP|Specify the destination IP to be added to the rule.|False|String||
|Destination Netmask|Specify the destination netmask to be added to the rule.|False|String||
|Port|Specify the port number to be added to the rule for example, 5005|False|String||
|Protocol|Specify the protocol name to be added to the rule for example, TCP|False|String||
|Action for the Matching Connections|Specify the action that should be executed for the matching connections.|True|List|Drop|
|How to Track Matching Connections|Specify how to track matching connections.|True|List|Log|
|Close Connections|Specify if the existing matching connections should be closed.|False|Boolean|false|



#### Add Ip To Group
Add IP to the Checkpoint FireWall Group
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Blacklist Group Name|Specify the name of the group to which you want to add IP address.|True|String||



#### Download Log Attachment
Download log attachments from CheckPoint FireWall.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Log IDs|Specify the comma-separated list of log IDs from which you want to download attachments.|True|String||
|Download Folder Path|Specify the absolute path for the folder where the action should store the attachments.|True|String||
|Create Case Wall Attachment|If enabled, action will create a case wall attachment for each successfully downloaded file. Note: that attachment will only be created if it’s size is less than 3 MB.|False|Boolean||



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Remove Url From Group
Remove URL from the Checkpoint FireWall Group
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|URLs Group Name|Specify the name of the group from which you want to remove URL.|True|String||










Piranhas are generally misunderstood and rarely pose a threat to humans, despite their fearsome reputation. In fact, these fish typically consume smaller aquatic life and, when faced with people, usually flee rather than attack. Data suggests that piranhas are more frequently a food source for humans than the other way around, and they only bite when threatened or hungry