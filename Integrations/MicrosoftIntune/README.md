
# MicrosoftIntune

Microsoft Intune is a cloud-based endpoint management solution. It manages user access and simplifies app and device management across your many devices, including mobile devices, desktop computers, and virtual endpoints.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Azure AD endpoint|Azure AD endpoint to connect to. Can be different for different tenant types.|True|String|https://login.microsoftonline.com|
|Microsoft Graph Endpoint|Microsoft Graph endpoint to connect to. Can be different for different tenant types.|True|String|https://graph.microsoft.com|
|Client ID|Specify the client (Application) ID of the Azure AD app to use for the integration.|True|String||
|Client Secret Value|Specify the client secret value (not secret ID!) of the Azure AD app to use for the integration.|True|Password|*****|
|Azure Active Directory ID|Specify the Azure Active Directory ID (Tenant ID). It can be found on Azure Active Directory page > App Registration > <Application you configured for your integration> > Directory (tenant) ID.|True|String||
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Microsoft Intune server is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.7-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|TIPCommon-1.0.15-py2.py3-none-any.whl|


## Actions
#### Reset Managed Device Passcode
Reset managed device passcode. The action starts the task, to check the current task status, run "Get Managed Device" action and see "deviceActionResults" section for task status.  The host name to run the action on can be provided either as a Siemplify entity or as an action input parameter. If the host name is passed to action both as an entity and input parameter - action will be executed on the input parameter. Host name is case insensitive. Action also can be provided with the host id to run on. If both host id and hostname are provided, action will run on the host id as a priority.  Please refer to our doc portal for more details.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Host Name|Specify a comma-separated list of host names to run the action on. Host name is case insensitive. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||
|Host Id|Specify a comma-separated list of host ids to run the action on. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||



#### Get Managed Device
Get managed device information from the Microsoft Intune service, including information on specific actions, for example locate device ("deviceActionResults" section of the json result). The host name to run the action on can be provided either as a Siemplify entity or as an action input parameter. If the host name is passed to action both as an entity and input parameter - action will be executed on the input parameter. Host name is case insensitive. Action also can be provided with the host id to run on. If both host id and hostname are provided, action will run on the host id as a priority.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Host Name|Specify the host name to run the action on. Host name is case insensitive. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Multiple values can be as a comma-separated string.|False|String||
|Host Id|Specify the host id to run the action on. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Multiple values can be as a comma-separated string.|False|String||



#### Remote Lock Managed Device
Remote lock managed device. The action starts the task, to check the current task status, run "Get Managed Device" action and see "deviceActionResults" section for task status.  The host name to run the action on can be provided either as a Siemplify entity or as an action input parameter. If the host name is passed to action both as an entity and input parameter - action will be executed on the input parameter. Host name is case insensitive. Action also can be provided with the host id to run on. If both host id and hostname are provided, action will run on the host id as a priority.  Please refer to our doc portal for more details.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Host Name|Specify a comma-separated list of host names to run the action on. Host name is case insensitive. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||
|Host Id|Specify a comma-separated list of host ids to run the action on. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||



#### Sync Managed Device
Sync managed device with the Microsoft Intune service. The host name to run the action on can be provided either as a Siemplify entity or as an action input parameter. If the host name is passed to action both as an entity and input parameter - action will be executed on the input parameter. Host name is case insensitive. Action also can be provided with the host id to run on. If both host id and hostname are provided, action will run on the host id as a priority. Please refer to our doc portal for more details.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Host Name|Specify a comma-separated list of host names to run the action on. Host name is case insensitive. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||
|Host Id|Specify a comma-separated list of host ids to run the action on. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||



#### List Managed Devices
List managed devices available in the Microsoft Intune instance based on provided criteria. Note: This action doesn't run on Chronicle SOAR entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Key|Specify the key that needs to be used to filter managed devices.|False|List|Select One|
|Filter Logic|Specify what filter logic should be applied. Filtering logic is working based on the value  provided in the “Filter Key” parameter.|False|List|Not Specified|
|Filter Value|Specify what value should be used in the filter. If “Equal“ is selected, action will try to find the exact match among results and if “Contains“ is selected, action will try to find results that contain that substring. If nothing is provided in this parameter, the filter will not be applied. Filtering logic is working based on the value  provided in the “Filter Key” parameter.|False|String||
|Max Records To Return|Specify how many records to return. If nothing is provided, action will return 50 records. Maximum: 100.|False|String|50|



#### Locate Managed Device
Locate managed device with the Microsoft Intune service. The action starts the task, to check the current task status, run "Get Managed Device" action and see "deviceActionResults" section for task status.  The host name to run the action on can be provided either as a Siemplify entity or as an action input parameter. If the host name is passed to action both as an entity and input parameter - action will be executed on the input parameter. Host name is case insensitive. Action also can be provided with the host id to run on. If both host id and hostname are provided, action will run on the host id as a priority.  Please refer to our doc portal for more details.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Host Name|Specify a comma-separated list of host names to run the action on. Host name is case insensitive. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||
|Host Id|Specify a comma-separated list of host ids to run the action on. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||



#### Wipe Managed Device
Wipe managed device with the Microsoft Intune service. The host name to run the action on can be provided either as a Siemplify entity or as an action input parameter. If the host name is passed to action both as an entity and input parameter - action will be executed on the input parameter. Host name is case insensitive. Action also can be provided with the host id to run on. If both host id and hostname are provided, action will run on the host id as a priority. Please refer to our doc portal for more details.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Host Name|Specify a comma-separated list of host names to run the action on. Host name is case insensitive. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||
|Host Id|Specify a comma-separated list of host ids to run the action on. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||
|Keep Enrollment Data|If enabled, keep enrollment data on the device.|False|Boolean|false|
|Keep User Data|If enabled, keep user data on the device.|False|Boolean|false|
|Persist Esim Data Plan|If enabled, persist esim data plan for the device.|False|Boolean|false|
|Mac OS Unlock Code|Specify if applicable Mac OS unlock code.|False|String||



#### Ping
Test connectivity to the Microsoft Intune service with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









