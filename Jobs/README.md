## CA Close Ticket In CA For Closed Case
Sync closure of the tickets at the CA Desk Manager with Siemplify cases closure.


**Run Interval In Seconds:** 7200

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|http://x.x.x.x:<port>|
|Username|String|True|sfdghh|
|Password|String|True|dfgv|
|Group Filter|String|False|Test|
|Group Field|String|True|group.combo_name|
|Ticket Final Status|String|True|Closed|
|Script Name|String|True|TEST CLOSE|


Readme text## Sync Incidents
Deprecated. This job synchronizes Google SecOps Alerts and Microsoft Sentinel Incidents. It ensures that comments, status, and tags are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the “Microsoft Sentinel Incident” tag. If the alert didn’t originate from “Microsoft Azure Sentinel Incident Connector v2”,  you will need to add an “Incident_ID” context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Azure Active Directory ID|String|True|dfgh|
|OAUTH2 Login Endpoint Url|String|True|https://login.microsoftonline.com|
|API Root|String|True|https://graph.microsoft.com|
|Client ID|String|True|dfgh|
|Max Hours Backwards|Int|False|24|
|Verify SSL|Boolean|False|true|
|Client Secret|Password|True|*****|


Readme text