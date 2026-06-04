## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/ServiceNow/jobs/103/jobInstances/45
This job will synchronize closed ServiceNow incidents and Google SecOps alerts. This job works with ServiceNow incidents that were ingested as alerts and also cases, which contains tag “ServiceNow” and “TICKET_ID” context value with Incident Number inside of it.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Password|Password|False|*****|
|Api Root|String|False|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|String|False|sdfghj|
|Verify SSL|Boolean|False|true|
|Client ID|String|False|dfghj|
|Use Oauth Authentication|Boolean|False|false|
|Max Hours Backwards|Int|False|24|
|Client Secret|Password|False|*****|
|Table Name|String|False|kjhgfd|
|Refresh Token|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/ServiceNow/jobs/103/jobInstances/44
This job will synchronize closed ServiceNow incidents and Google SecOps alerts. This job works with ServiceNow incidents that were ingested as alerts and also cases, which contains tag “ServiceNow” and “TICKET_ID” context value with Incident Number inside of it.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|False|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|String|False|dfghj|
|Verify SSL|Boolean|False|true|
|Client ID|String|False|cvbnm|
|Use Oauth Authentication|Boolean|False|false|
|Max Hours Backwards|Int|False|24|
|Table Name|String|False|gfds|
|Password|Password|False|*****|
|Client Secret|Password|False|*****|
|Refresh Token|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/CaseFederation/jobs/42/jobInstances/43
This job will sync case metadata to an external platform for central management.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Target Platform|String|False|edrftghj|
|API Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/PaloAltoCortexXDR/jobs/98/jobInstances/47
This job synchronizes Google SecOps Alerts and Palo Alto XDR Incidents. It ensures that comments and status are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the "Palo Alto XDR Incident" tag. If the alert didn’t originate from "Palo Alto Cortex XDR Connector",  you will need to add an "Incident_ID" context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|Api Root|String|False|sdfghj|
|Api Key ID|String|False|sdfghj|
|Max Hours Backwards|Int|False|24|
|User Mapping JSON|String|False|{"Google SecOps Display Name": "XDR Username"}|
|Verify SSL|Boolean|False|true|
|Api Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/Tools/jobs/105/jobInstances/46
This job will close all cases based on a search query.  The Search Payload is the payload used in the 'CaseSearchEverything' API call.  To get an example of this value, go to Search in the UI and open Developer Tools.  Search for the cases to delete.  Look for the "CaseSearchEverything" api call in DevTools.  Copy the JSON payload of the POST request and paste in "Search Payload".  The Close Reason should be 0 or 1.   0 = malicious 1  = not malicious.  Root Cause comes from Settings -> Case Data -> Case Close Root Cause


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Search Payload|String|False|{}|
|Close Comment|String|False|test|
|Close Reason|Int|False|1|
|Root Cause|String|False|not_malicious|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/MicrosoftTeams/jobs/97/jobInstances/48
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False||


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/CrowdStrikeFalcon/jobs/88/jobInstances/50
This job will synchronize Google SecOps Alerts and Crowdstrike alerts. The job synchronizes comments and status. Requires “Crowdstrike Alert” tag on the case. Note: If the alert didn’t originate from “Alerts Connector” or “Identity Protections Detection Connector” you will need to add an “Alert_ID” context value for the job to be able to find the correct information.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|API Root|String|False|https://api.crowdstrike.com|
|Client ID|String|False|dfghj|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/CaServiceDesk/jobs/87/jobInstances/62
Sync closure of the tickets at the CA Desk Manager with Siemplify cases closure.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|False|http://x.x.x.x:<port>|
|Username|String|False|sdfghj|
|Password|String|False|dfghj|
|Group Filter|String|False|Testsdfghj|
|Group Field|String|False|group.combo_name|
|Ticket Final Status|String|False|Closed|
|Script Name|String|False|TEST CLOSE|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/CaServiceDesk/jobs/87/jobInstances/23
Sync closure of the tickets at the CA Desk Manager with Siemplify cases closure.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|False|http://x.x.x.x:<port>|
|Username|String|False|dfghj|
|Password|String|False|dfgvhbn|
|Group Filter|String|False|Test|
|Group Field|String|False|group.combo_name|
|Ticket Final Status|String|False|Closed|
|Script Name|String|False|TEST CLOSE|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/CaseFederation/jobs/42/jobInstances/24
This job will sync case metadata to an external platform for central management.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Target Platform|String|False|hgfds|
|API Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/CaseFederation/jobs/42/jobInstances/51
This job will sync case metadata to an external platform for central management.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Target Platform|String|False|ertyu|
|API Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/CaseFederation/jobs/42/jobInstances/58
This job will sync case metadata to an external platform for central management.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Target Platform|String|False|456789|
|API Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/CaseFederation/jobs/42/jobInstances/36
This job will sync case metadata to an external platform for central management.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Target Platform|String|False|hgfdsgf|
|API Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/Siemplify/jobs/110/jobInstances/42
Collect cases and connector logs from Publisher.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Publisher Id|Int|False|jjhgfd|
|Verify SSL|Boolean|False|false|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/Tools/jobs/105/jobInstances/12
This job will close all cases based on a search query.  The Search Payload is the payload used in the 'CaseSearchEverything' API call.  To get an example of this value, go to Search in the UI and open Developer Tools.  Search for the cases to delete.  Look for the "CaseSearchEverything" api call in DevTools.  Copy the JSON payload of the POST request and paste in "Search Payload".  The Close Reason should be 0 or 1.   0 = malicious 1  = not malicious.  Root Cause comes from Settings -> Case Data -> Case Close Root Cause


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Search Payload|String|False|{}|
|Close Comment|String|False|Closed|
|Close Reason|Int|False|1|
|Root Cause|String|False|Malicious|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/Exchange/jobs/90/jobInstances/22
Note that the job is deprecated and will be removed in the next 6 months. Oauth Token Expiry Notification Job is recommended to use if integration is working with Oauth refresh tokens. Refresh tokens are valid only for 90 days, after that User will need to create a new refresh token to use in the integration. This job will send reminder emails to the configured recipient list when the token will expire in 10, 5 and 1 day. Once a new token is set in this job, the notification timer will start over.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Mail Server Address|String|False|outlook.office365.com|
|Mail Address for sending notifications|String|False|gfd|
|Notifications Recipients List|String|False|gfds|
|Client ID|String|False|hgfdsa|
|Tenant (Directory) ID|String|False|ds|
|Client Secret|Password|False|*****|
|Refresh Token|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/MicrosoftTeams/jobs/97/jobInstances/17
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False||


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/AzureApi/jobs/83/jobInstances/20
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False||


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/MicrosoftTeams/jobs/97/jobInstances/59
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False||


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/AzureSecurityCenter/jobs/84/jobInstances/61
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False||
|Connector Names|String|False||


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/MicrosoftGraphMailDelegated/jobs/96/jobInstances/40
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False|rewf|
|Connector Names|String|False|ds|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/AzureSecurityCenter/jobs/84/jobInstances/66
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False||
|Connector Names|String|False||


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/MicrosoftGraphMailDelegated/jobs/96/jobInstances/49
Token renewal job should be used to periodically update the refresh token configured for the integration. By default, the refresh token expires every 90 days, making integration unusable upon expiration. It is recommended to run this job every 7 or 14 days to make sure that refresh token will be up to date.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Integration Environments|String|False||
|Connector Names|String|False||


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/Microsoft365Defender/jobs/93/jobInstances/19
This job synchronizes Google SecOps Alerts and Microsoft Defender XDR Alerts. It ensures that comments and status are synchronized bi-directionally between both systems. Note: Assignee synchronization occurs exclusively from Microsoft Defender to Google SecOps. For the job to identify the correct information, the Google SecOps case must have the "Microsoft Defender XDR Alert" tag. If the alert didn’t originate from "Microsoft 365 Defender - Incidents Connector",  you will need to add an "Alert_ID" context value to the alert for the job to be able to find the correct information.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|Login API Root|String|False|https://login.microsoftonline.com|
|Graph API Root|String|False|https://graph.microsoft.com|
|API Root|String|False|https://api.security.microsoft.com|
|Tenant ID|String|False|dfghj|
|Client ID|String|False|dfghjkl|
|Max Hours Backwards|Int|False|24|
|Sync Assignee|Boolean|False|true|
|Verify SSL|Boolean|False|false|
|Client Secret|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/CrowdStrikeFalcon/jobs/88/jobInstances/27
This job will synchronize Google SecOps Alerts and Crowdstrike alerts. The job synchronizes comments and status. Requires “Crowdstrike Alert” tag on the case. Note: If the alert didn’t originate from “Alerts Connector” or “Identity Protections Detection Connector” you will need to add an “Alert_ID” context value for the job to be able to find the correct information.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|API Root|String|False|https://api.crowdstrike.com|
|Client ID|String|False|dfghj|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/SentinelOneV2/jobs/99/jobInstances/52
This job will synchronize Google SecOps Alerts and SentinelOne alerts. The job synchronizes status. Requires “SentinelOne Alert” tag on the case. Note: If the alert didn’t originate from “Alerts Connector” you will need to add an “Alert_ID” Alert Context Value for the job to be able to find the correct information.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|API Root|String|False|sdfghj|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|true|
|API Token|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/Microsoft365Defender/jobs/93/jobInstances/65
This job synchronizes Google SecOps Alerts and Microsoft Defender XDR Alerts. It ensures that comments and status are synchronized bi-directionally between both systems. Note: Assignee synchronization occurs exclusively from Microsoft Defender to Google SecOps. For the job to identify the correct information, the Google SecOps case must have the "Microsoft Defender XDR Alert" tag. If the alert didn’t originate from "Microsoft 365 Defender - Incidents Connector",  you will need to add an "Alert_ID" context value to the alert for the job to be able to find the correct information.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|Login API Root|String|False|https://login.microsoftonline.com|
|Graph API Root|String|False|https://graph.microsoft.com|
|API Root|String|False|https://api.security.microsoft.com|
|Tenant ID|String|False|fds|
|Client ID|String|False|gfd|
|Max Hours Backwards|Int|False|24|
|Sync Assignee|Boolean|False|false|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/Microsoft365Defender/jobs/93/jobInstances/64
This job synchronizes Google SecOps Alerts and Microsoft Defender XDR Alerts. It ensures that comments and status are synchronized bi-directionally between both systems. Note: Assignee synchronization occurs exclusively from Microsoft Defender to Google SecOps. For the job to identify the correct information, the Google SecOps case must have the "Microsoft Defender XDR Alert" tag. If the alert didn’t originate from "Microsoft 365 Defender - Incidents Connector",  you will need to add an "Alert_ID" context value to the alert for the job to be able to find the correct information.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|Login API Root|String|False|https://login.microsoftonline.com|
|Graph API Root|String|False|https://graph.microsoft.com|
|API Root|String|False|https://api.security.microsoft.com|
|Tenant ID|String|False|dfghj|
|Client ID|String|False|dfghj|
|Max Hours Backwards|Int|False|24|
|Sync Assignee|Boolean|False|false|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/CrowdStrikeFalcon/jobs/88/jobInstances/37
This job will synchronize Google SecOps Alerts and Crowdstrike alerts. The job synchronizes comments and status. Requires “Crowdstrike Alert” tag on the case. Note: If the alert didn’t originate from “Alerts Connector” or “Identity Protections Detection Connector” you will need to add an “Alert_ID” context value for the job to be able to find the correct information.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|API Root|String|False|https://api.crowdstrike.com|
|Client ID|String|False|fds|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/BMCRemedyITSM/jobs/85/jobInstances/25
This job will synchronize BMC Remedy ITSM incidents that were created within Siemplify Case playbook and Siemplify cases. Note: in BMC Remedy ITSM statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it's required for the case to have 2 tags. First tag should be "BMC Remedy ITSM" and the second should be with the prefix "BMC Remedy ITSM:{Incident ID}". Job can only close incidents that are assigned in BMC Remedy ITSM.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Incident Table|String|False|HPD:IncidentInterface|
|API Root|String|False|https://{IP}:{port}|
|Username|String|False|dfghj|
|Environment|String|False||
|Max Hours Backwards|String|False|24|
|Verify SSL|Boolean|False|true|
|Password|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/ServiceNow/jobs/103/jobInstances/15
This job will synchronize closed ServiceNow incidents and Google SecOps alerts. This job works with ServiceNow incidents that were ingested as alerts and also cases, which contains tag “ServiceNow” and “TICKET_ID” context value with Incident Number inside of it.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|False|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|String|False|dfghj|
|Verify SSL|Boolean|False|true|
|Client ID|String|False|fghjk|
|Use Oauth Authentication|Boolean|False|false|
|Max Hours Backwards|Int|False|24|
|Table Name|String|False|test|
|Password|Password|False|*****|
|Client Secret|Password|False|*****|
|Refresh Token|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/ServiceDeskPlusV3/jobs/115/jobInstances/30
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|False|http://{IP OR FQDN}:8080/api/v3/|
|Max Hours Backwards|String|False|24|
|Verify SSL|Boolean|False|true|
|Api Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/ServiceDeskPlusV3/jobs/115/jobInstances/55
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|False|http://{IP OR FQDN}:8080/api/v3/|
|Max Hours Backwards|String|False|24|
|Verify SSL|Boolean|False|true|
|Api Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/ServiceDeskPlusV3/jobs/115/jobInstances/63
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|False|http://{IP OR FQDN}:8080/api/v3/|
|Max Hours Backwards|String|False|24|
|Verify SSL|Boolean|False|true|
|Api Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/ServiceDeskPlusV3/jobs/115/jobInstances/34
This job will synchronize ServiceDeskPlus requests that were created within Siemplify Case playbook and Siemplify cases. Note: in ServiceDeskPlus statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceDeskPlus" and the second should be with the prefix "ServiceDeskPlus Requests:{request id}".


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|False|http://{IP OR FQDN}:8080/api/v3/|
|Max Hours Backwards|String|False|24|
|Verify SSL|Boolean|False|true|
|Api Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/CaServiceDesk/jobs/86/jobInstances/28
Sync comments from CA Desk Manager to Siemplify.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|False|http://x.x.x.x:<port>|
|Username|String|False|dfgh|
|Summery Field|String|False|summery.combo_name|
|Ticket Fields|String|False|summery.combo_name,customer.combo_name,category.sym,status.sym,priority.sym,active,log_agent.combo_name,assignee.combo_name,group.combo_name,affected_service.name,severity.sym,urgency.sym,impact.sym,problem.ref_num,resolution_code.sym,call_back_date,change.chg_ref_num,caused_by_chg.chg_ref_num,external_system_ticket,resolution_method.sym,symptom_code.sym,requested_by.combo_name,persistent_id,summary,description,open_date,last_mod_dt,resolve_date,close_date,ref_num|
|Script Name|String|False|Test|
|Ticket Type Field|Boolean|False|true|
|Analyst Type Field|Boolean|False|true|
|Time Stamp Field|Boolean|False|true|
|Timezone String|Boolean|False|true|
|Password|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/SOCRadar/jobs/116/jobInstances/31
Scheduled job that fetches IOCs from configured SOCRadar Threat Feed collections and writes them to Chronicle SIEM reference lists. Creates one list per IOC type (ip, domain, hash, url). Run daily to keep threat intelligence feeds current.



**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Key|Password|False|*****|
|Collection UUIDs|String|False|hgfds|
|Max IOCs Per Feed|Int|False|5000|
|Reference List Prefix|String|False|SOCRadar_IOC|
|API Root|String|False|https://platform.socradar.com/api|
|Company ID|String|False|gfds|
|Verify SSL|Boolean|False|true|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/SOCRadar/jobs/116/jobInstances/39
Scheduled job that fetches IOCs from configured SOCRadar Threat Feed collections and writes them to Chronicle SIEM reference lists. Creates one list per IOC type (ip, domain, hash, url). Run daily to keep threat intelligence feeds current.



**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Collection UUIDs|String|False|ertfyguhi|
|Max IOCs Per Feed|Int|False|5000|
|Reference List Prefix|String|False|SOCRadar_IOC|
|API Root|String|False|https://platform.socradar.com/api|
|Company ID|String|False|erftgyhujk|
|Verify SSL|Boolean|False|true|
|API Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/SOCRadar/jobs/116/jobInstances/38
Scheduled job that fetches IOCs from configured SOCRadar Threat Feed collections and writes them to Chronicle SIEM reference lists. Creates one list per IOC type (ip, domain, hash, url). Run daily to keep threat intelligence feeds current.



**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Collection UUIDs|String|False|gfds|
|Max IOCs Per Feed|Int|False|5000|
|Reference List Prefix|String|False|SOCRadar_IOC|
|API Root|String|False|https://platform.socradar.com/api|
|Company ID|String|False|jhgfdsgfds|
|Verify SSL|Boolean|False|true|
|API Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/ServiceNow/jobs/104/jobInstances/7
This job will synchronize incidents fields and attachments that are related to case/alerts in ServiceNow. For the job to work, you need to have the "ServiceNow Incident Sync" tag added to the case and "TICKET_ID" context value added to either Case or Alert depending on the parameter "Sync Level". Example of the "TICKET_ID": "INC0000050,INC0000051".


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|False|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|String|False|wwss|
|Sync Level|String|False|Case|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|false|
|Password|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/MicrosoftAzureSentinel/jobs/94/jobInstances/54
Use the Sync Incidents V2 job to synchronize Google SecOps alerts with Microsoft Sentinel incidents. This job ensures that comments, statuses, and tags are synchronized bi-directionally between both systems. Note: Assignee and severity synchronization occurs exclusively from Microsoft Sentinel to Google SecOps. For the job to identify the correct information, the Google SecOps case must have the Microsoft Sentinel Incident tag. This job only works on alerts from the Microsoft Azure Sentinel Incident Connector v2.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|Azure Subscription ID|String|False|dfgh|
|Azure Active Directory ID|String|False|dfghj|
|OAUTH2 Login Endpoint Url|String|False|https://login.microsoftonline.com|
|Management API Root|String|False|https://management.azure.com|
|Azure Resource Group|String|False|cvbnm|
|Azure Sentinel Workspace Name|String|False|fghj|
|Client ID|String|False|dfghj|
|Max Hours Backwards|Int|False|24|
|Sync Assignee|Boolean|False|true|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/PaloAltoCortexXDR/jobs/98/jobInstances/26
This job synchronizes Google SecOps Alerts and Palo Alto XDR Incidents. It ensures that comments and status are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the "Palo Alto XDR Incident" tag. If the alert didn’t originate from "Palo Alto Cortex XDR Connector",  you will need to add an "Incident_ID" context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|Api Root|String|False|jhgf|
|Api Key ID|String|False|gfds|
|Max Hours Backwards|Int|False|24|
|User Mapping JSON|String|False|{"Google SecOps Display Name": "XDR Username"}|
|Verify SSL|Boolean|False|true|
|Api Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/PaloAltoCortexXDR/jobs/98/jobInstances/57
This job synchronizes Google SecOps Alerts and Palo Alto XDR Incidents. It ensures that comments and status are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the "Palo Alto XDR Incident" tag. If the alert didn’t originate from "Palo Alto Cortex XDR Connector",  you will need to add an "Incident_ID" context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|Api Root|String|False|sdfghj|
|Api Key ID|String|False|dfghj|
|Max Hours Backwards|Int|False|24|
|User Mapping JSON|String|False|{"Google SecOps Display Name": "XDR Username"}|
|Verify SSL|Boolean|False|true|
|Api Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/PaloAltoCortexXDR/jobs/98/jobInstances/32
This job synchronizes Google SecOps Alerts and Palo Alto XDR Incidents. It ensures that comments and status are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the "Palo Alto XDR Incident" tag. If the alert didn’t originate from "Palo Alto Cortex XDR Connector",  you will need to add an "Incident_ID" context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|Api Root|String|False|dfghj|
|Api Key ID|String|False|sdfghjk|
|Max Hours Backwards|Int|False|24|
|User Mapping JSON|String|False|{"Google SecOps Display Name": "XDR Username"}|
|Verify SSL|Boolean|False|true|
|Api Key|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/ServiceNow/jobs/101/jobInstances/41
This job will synchronize comments in ServiceNow table records and Siemplify cases. Additionally, in order for the job to work, it’s required for the case to have 2 tags. First tag should be "ServiceNow {table name}", for example, "ServiceNow incident" and the second should be with the prefix "ServiceNow TicketId: {TICKET_ID}". Example of the "TICKET_ID": "INC0000050,INC0000051".


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|False|https://{dev-instance}.service-now.com/api/now/v1/|
|Username|String|False|gfds|
|Table Name|String|False|fds|
|Verify SSL|Boolean|False|true|
|Password|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/SentinelOneV2/jobs/100/jobInstances/18
This job will synchronize Google SecOps Alerts and SentinelOne threats. The job synchronizes comments and status. Requires “SentinelOne Threat” tag on the case. Note: If the alert didn’t originate from “Threats Connector” you will need to add an “Threat_ID” Alert Context Value for the job to be able to find the correct information. 


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|API Root|String|False|hgfds|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|false|
|API Token|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/SentinelOneV2/jobs/100/jobInstances/16
This job will synchronize Google SecOps Alerts and SentinelOne threats. The job synchronizes comments and status. Requires “SentinelOne Threat” tag on the case. Note: If the alert didn’t originate from “Threats Connector” you will need to add an “Threat_ID” Alert Context Value for the job to be able to find the correct information. 


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Token|Password|False|*****|
|Environment Name|String|False|Default Environment|
|API Root|String|False|dfghj|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|true|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/SentinelOneV2/jobs/100/jobInstances/56
This job will synchronize Google SecOps Alerts and SentinelOne threats. The job synchronizes comments and status. Requires “SentinelOne Threat” tag on the case. Note: If the alert didn’t originate from “Threats Connector” you will need to add an “Threat_ID” Alert Context Value for the job to be able to find the correct information. 


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|False|Default Environment|
|API Root|String|False|dfghjk|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|true|
|API Token|Password|False|*****|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/Tools/jobs/106/jobInstances/33
This job will search all open cases, and identify cases that have not been touched in Max Time hours, and apply the tag/tags listed in the tags parameter


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|False|Open Case Reviewfghm|
|Unmodified Time|Int|False|8|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/Tools/jobs/106/jobInstances/11
This job will search all open cases, and identify cases that have not been touched in Max Time hours, and apply the tag/tags listed in the tags parameter


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|False|Open Case Review|
|Unmodified Time|Int|False|8|


Readme text## projects/spsstg-ck6l5/locations/us/instances/96356bda-a057-49d1-9692-34b4b2c9c3f6/integrations/Tools/jobs/106/jobInstances/60
This job will search all open cases, and identify cases that have not been touched in Max Time hours, and apply the tag/tags listed in the tags parameter


**Run Interval In Seconds:** None

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Tags|String|False|Open Case Reertyuview|
|Unmodified Time|Int|False|8e|


Readme text