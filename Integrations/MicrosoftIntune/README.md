
# MicrosoftIntune

Microsoft Intune is a cloud-based endpoint management solution. It manages user access and simplifies app and device management across your many devices, including mobile devices, desktop computers, and virtual endpoints.

Python Version - 3
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
#### Sync Managed Device
Sync managed device with the Microsoft Intune service. The host name to run the action on can be provided either as a Siemplify entity or as an action input parameter. If the host name is passed to action both as an entity and input parameter - action will be executed on the input parameter. Host name is case insensitive. Action also can be provided with the host id to run on. If both host id and hostname are provided, action will run on the host id as a priority. Please refer to our doc portal for more details.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Host Name|Specify a comma-separated list of host names to run the action on. Host name is case insensitive. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||
|Host Id|Specify a comma-separated list of host ids to run the action on. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||



#### Remote Lock Managed Device
Remote lock managed device. The action starts the task, to check the current task status, run "Get Managed Device" action and see "deviceActionResults" section for task status.  The host name to run the action on can be provided either as a Siemplify entity or as an action input parameter. If the host name is passed to action both as an entity and input parameter - action will be executed on the input parameter. Host name is case insensitive. Action also can be provided with the host id to run on. If both host id and hostname are provided, action will run on the host id as a priority.  Please refer to our doc portal for more details.
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



#### Get Managed Device
Get managed device information from the Microsoft Intune service, including information on specific actions, for example locate device ("deviceActionResults" section of the json result). The host name to run the action on can be provided either as a Siemplify entity or as an action input parameter. If the host name is passed to action both as an entity and input parameter - action will be executed on the input parameter. Host name is case insensitive. Action also can be provided with the host id to run on. If both host id and hostname are provided, action will run on the host id as a priority.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Host Name|Specify the host name to run the action on. Host name is case insensitive. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Multiple values can be as a comma-separated string.|False|String||
|Host Id|Specify the host id to run the action on. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Multiple values can be as a comma-separated string.|False|String||



##### JSON Results
```json
[{"Entity": "CROWDSTRIKEV2", "EntityResult": {"id": "a80a77c5-c26f-4def-b350-2", "userId": "", "deviceName": "Demo", "managedDeviceOwnerType": "personal", "enrolledDateTime": "2022-03-01T20:42:04Z", "lastSyncDateTime": "2022-03-04T04:42:03Z", "operatingSystem": "Windows", "complianceState": "noncompliant", "jailBroken": "Unknown", "managementAgent": "mdm", "osVersion": "10.0.19043.1526", "easActivated": false, "easDeviceId": "", "easActivationDateTime": "0001-01-01T00:00:00Z", "azureADRegistered": null, "deviceEnrollmentType": "windowsAutoEnrollment", "activationLockBypassCode": null, "emailAddress": "", "azureADDeviceId": "a80a77c5-c26f-4def-b350-2b80ae9b5e00", "deviceRegistrationState": "registered", "deviceCategoryDisplayName": "Unknown", "isSupervised": false, "exchangeLastSuccessfulSyncDateTime": "0001-01-01T00:00:00Z", "exchangeAccessState": "none", "exchangeAccessStateReason": "none", "remoteAssistanceSessionUrl": null, "remoteAssistanceSessionErrorDetails": null, "isEncrypted": false, "userPrincipalName": "", "model": "VMware7,1", "manufacturer": "VMware, Inc.", "imei": "", "complianceGracePeriodExpirationDateTime": "2022-10-16T16:36:51Z", "serialNumber": "VMware-422238ba4acad659-63a1867ec4889b06", "phoneNumber": "", "androidSecurityPatchLevel": "", "userDisplayName": "", "configurationManagerClientEnabledFeatures": null, "wiFiMacAddress": "", "deviceHealthAttestationState": null, "subscriberCarrier": "", "meid": "", "totalStorageSpaceInBytes": 63766003712, "freeStorageSpaceInBytes": 38917898240, "managedDeviceName": "", "partnerReportedThreatState": "unknown", "requireUserEnrollmentApproval": null, "managementCertificateExpirationDate": "2023-02-27T08:10:12Z", "iccid": null, "udid": null, "notes": null, "ethernetMacAddress": null, "physicalMemoryInBytes": 0, "deviceActionResults": []}}, {"Entity": "Deeksha’s iPhone", "EntityResult": {"id": "8f198977-a53d-426a-8600-", "userId": "1a4a8aaf-257f-49de-ab8b-bd82d428a371", "deviceName": "Deeksha", "managedDeviceOwnerType": "personal", "enrolledDateTime": "2023-06-27T08:15:54Z", "lastSyncDateTime": "2023-06-27T09:05:05Z", "operatingSystem": "iOS", "complianceState": "compliant", "jailBroken": "false", "managementAgent": "mdm", "osVersion": "16.5.1", "easActivated": true, "easDeviceId": "GIJ5DV30AT6MD874GKBDBB590O", "easActivationDateTime": "0001-01-01T00:00:00Z", "azureADRegistered": true, "deviceEnrollmentType": "userEnrollment", "activationLockBypassCode": null, "emailAddress": "exchange_online_test@siemplifycyarx.onmicrosoft.com", "azureADDeviceId": "98619e4e-63dd-4508-9a92-ef8f9d8545ba", "deviceRegistrationState": "registered", "deviceCategoryDisplayName": "Unknown", "isSupervised": false, "exchangeLastSuccessfulSyncDateTime": "0001-01-01T00:00:00Z", "exchangeAccessState": "none", "exchangeAccessStateReason": "none", "remoteAssistanceSessionUrl": null, "remoteAssistanceSessionErrorDetails": null, "isEncrypted": false, "userPrincipalName": "exchange_online_test@siemplifycyarx.onmicrosoft.com", "model": "iPhone 11", "manufacturer": "Apple", "imei": "352986114316684", "complianceGracePeriodExpirationDateTime": "9999-12-31T23:59:59Z", "serialNumber": "GV4D807ZN73C", "phoneNumber": "", "androidSecurityPatchLevel": "", "userDisplayName": "exchange_online_test", "configurationManagerClientEnabledFeatures": null, "wiFiMacAddress": "20698078b17a", "deviceHealthAttestationState": null, "subscriberCarrier": "", "meid": "35298611431668", "totalStorageSpaceInBytes": 68719476736, "freeStorageSpaceInBytes": 56470011904, "managedDeviceName": "exchange_online_test_IPhone_6/27/2023_8:15 AM", "partnerReportedThreatState": "unknown", "requireUserEnrollmentApproval": null, "managementCertificateExpirationDate": "2024-06-25T16:52:09Z", "iccid": null, "udid": null, "notes": null, "ethernetMacAddress": null, "physicalMemoryInBytes": 0, "deviceActionResults": []}}]
```



#### List Managed Devices
List managed devices available in the Microsoft Intune instance based on provided criteria. Note: This action doesn't run on Chronicle SOAR entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Key|Specify the key that needs to be used to filter managed devices.|False|List|Select One|
|Filter Logic|Specify what filter logic should be applied. Filtering logic is working based on the value  provided in the “Filter Key” parameter.|False|List|Not Specified|
|Filter Value|Specify what value should be used in the filter. If “Equal“ is selected, action will try to find the exact match among results and if “Contains“ is selected, action will try to find results that contain that substring. If nothing is provided in this parameter, the filter will not be applied. Filtering logic is working based on the value  provided in the “Filter Key” parameter.|False|String||
|Max Records To Return|Specify how many records to return. If nothing is provided, action will return 50 records. Maximum: 100.|False|String|50|



##### JSON Results
```json
[{"id": "a80a77c5-c26f", "userId": "", "deviceName": "Demo", "managedDeviceOwnerType": "personal", "enrolledDateTime": "2022-03-01T20:42:04Z", "lastSyncDateTime": "2022-03-04T04:42:03Z", "operatingSystem": "Windows", "complianceState": "noncompliant", "jailBroken": "Unknown", "managementAgent": "mdm", "osVersion": "10.0.19043.1526", "easActivated": false, "easDeviceId": "", "easActivationDateTime": "0001-01-01T00:00:00Z", "azureADRegistered": null, "deviceEnrollmentType": "windowsAutoEnrollment", "activationLockBypassCode": null, "emailAddress": "", "azureADDeviceId": "a80a77c5-c26f-ae9b5e00", "deviceRegistrationState": "registered", "deviceCategoryDisplayName": "Unknown", "isSupervised": false, "exchangeLastSuccessfulSyncDateTime": "0001-01-01T00:00:00Z", "exchangeAccessState": "null", "exchangeAccessStateReason": "null", "remoteAssistanceSessionUrl": null, "remoteAssistanceSessionErrorDetails": null, "isEncrypted": false, "userPrincipalName": "", "model": "VMware7,1", "manufacturer": "VMware, Inc.", "imei": "", "complianceGracePeriodExpirationDateTime": "2022-10-16T16:36:51Z", "serialNumber": "VMware-422238ba4acad659-63a1867ec4889b06", "phoneNumber": "", "androidSecurityPatchLevel": "", "userDisplayName": "", "configurationManagerClientEnabledFeatures": null, "wiFiMacAddress": "", "deviceHealthAttestationState": null, "subscriberCarrier": "", "meid": "", "totalStorageSpaceInBytes": 63766003712, "freeStorageSpaceInBytes": 38917898240, "managedDeviceName": "", "partnerReportedThreatState": "unknown", "requireUserEnrollmentApproval": null, "managementCertificateExpirationDate": "2023-02-27T08:10:12Z", "iccid": null, "udid": null, "notes": null, "ethernetMacAddress": null, "physicalMemoryInBytes": 0, "deviceActionResults": []}, {"id": "8f198977-a53d-426a-8600-", "userId": "1a4a8aaf-257f-49de-ab8b-", "deviceName": "Deeksha", "managedDeviceOwnerType": "personal", "enrolledDateTime": "2023-06-27T08:15:54Z", "lastSyncDateTime": "2023-06-29T05:17:54Z", "operatingSystem": "iOS", "complianceState": "compliant", "jailBroken": "false", "managementAgent": "mdm", "osVersion": "16.5.1", "easActivated": true, "easDeviceId": "GIJ5DV30AT6MD874GKBDBB590O", "easActivationDateTime": "0001-01-01T00:00:00Z", "azureADRegistered": true, "deviceEnrollmentType": "userEnrollment", "activationLockBypassCode": null, "emailAddress": "exchange_online_test@siemplifycyarx.onmicrosoft.com", "azureADDeviceId": "98619e4e-63dd-4508-9a92-ef8f9d8545ba", "deviceRegistrationState": "registered", "deviceCategoryDisplayName": "Unknown", "isSupervised": false, "exchangeLastSuccessfulSyncDateTime": "0001-01-01T00:00:00Z", "exchangeAccessState": "null", "exchangeAccessStateReason": "null", "remoteAssistanceSessionUrl": null, "remoteAssistanceSessionErrorDetails": null, "isEncrypted": false, "userPrincipalName": "exchange_online_test@siemplifycyarx.onmicrosoft.com", "model": "iPhone 11", "manufacturer": "Apple", "imei": "352986114316684", "complianceGracePeriodExpirationDateTime": "9999-12-31T23:59:59Z", "serialNumber": "GV4D807ZN73C", "phoneNumber": "", "androidSecurityPatchLevel": "", "userDisplayName": "exchange_online_test", "configurationManagerClientEnabledFeatures": null, "wiFiMacAddress": "20698078b17a", "deviceHealthAttestationState": null, "subscriberCarrier": "", "meid": "35298611431668", "totalStorageSpaceInBytes": 68719476736, "freeStorageSpaceInBytes": 56372494336, "managedDeviceName": "exchange_online_test_IPhone_6/27/2023_8:15 AM", "partnerReportedThreatState": "unknown", "requireUserEnrollmentApproval": null, "managementCertificateExpirationDate": "2024-06-25T16:52:09Z", "iccid": null, "udid": null, "notes": null, "ethernetMacAddress": null, "physicalMemoryInBytes": 0, "deviceActionResults": []}]
```



#### Ping
Test connectivity to the Microsoft Intune service with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Locate Managed Device
Locate managed device with the Microsoft Intune service. The action starts the task, to check the current task status, run "Get Managed Device" action and see "deviceActionResults" section for task status.  The host name to run the action on can be provided either as a Siemplify entity or as an action input parameter. If the host name is passed to action both as an entity and input parameter - action will be executed on the input parameter. Host name is case insensitive. Action also can be provided with the host id to run on. If both host id and hostname are provided, action will run on the host id as a priority.  Please refer to our doc portal for more details.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Host Name|Specify a comma-separated list of host names to run the action on. Host name is case insensitive. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||
|Host Id|Specify a comma-separated list of host ids to run the action on. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||



#### Reset Managed Device Passcode
Reset managed device passcode. The action starts the task, to check the current task status, run "Get Managed Device" action and see "deviceActionResults" section for task status.  The host name to run the action on can be provided either as a Siemplify entity or as an action input parameter. If the host name is passed to action both as an entity and input parameter - action will be executed on the input parameter. Host name is case insensitive. Action also can be provided with the host id to run on. If both host id and hostname are provided, action will run on the host id as a priority.  Please refer to our doc portal for more details.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Host Name|Specify a comma-separated list of host names to run the action on. Host name is case insensitive. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||
|Host Id|Specify a comma-separated list of host ids to run the action on. If the action does not run on a hostname entity, it can run either on Host Name or Host ID. Note: if both "Host Name" and "Host Id" are provided, then "Host Id" value will have priority. Multiple values can be as a comma-separated string.|False|String||









