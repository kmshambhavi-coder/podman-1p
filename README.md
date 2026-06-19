# GitSync

## Integrations
|Name|Description|
|----|-----------|
|Amazon Macie|Amazon Macie is a powerful security and compliance service that provides an automatic method to detect, identify, and classify data within your AWS account.|
|CrowdStrike Falcon|CrowdStrike Falcon is the leader in next-generation endpoint protection, threat intelligence and incident response through cloud-based endpoint protection.|
|McAfee Mvision EDR V2|McAfee MVISION Endpoint Detection and Response (MVISION EDR) is a cloud-delivered service that enables you to detect advanced device threats, fully investigate, and quickly respond. Continuous data collection and advanced analytics detect suspicious behavior.|
|Microsoft Graph Mail|Microsoft 365 and Office 365 deliver the power of cloud productivity to businesses of all sizes, helping save time, money, and free up valued resources. The Microsoft 365 and Office 365 plans combine the familiar Microsoft Office desktop suite with cloud-based versions of Microsoft's next-generation communications and collaboration services (including Office for the web, Microsoft Exchange Online, Microsoft Teams, and Microsoft SharePoint Online) to help users be productive from virtually anywhere through the Internet. This integration uses Microsoft Graph Mail API to communicate with Microsoft 365 and Office 365 services.|


## Connectors
|Name|Description|Has Mappings|
|----|-----------|------------|
|101 AWS Cloud Trail - Insights Connector|Pull insights from AWS Cloud Trail.|False|
|AWS Cloud Trail - Insights Connector|Pull insights from AWS Cloud Trail.|False|


## Jobs
|Name|Description|
|----|-----------|
|CA Close Ticket In CA For Closed Case|Sync closure of the tickets at the CA Desk Manager with Siemplify cases closure.|
|Sync Comments|Sync comments from CA Desk Manager to Siemplify.|
|Sync Incidents V2|Use the Sync Incidents V2 job to synchronize Google SecOps alerts with Microsoft Sentinel incidents. This job ensures that comments, statuses, and tags are synchronized bi-directionally between both systems. Note: Assignee and severity synchronization occurs exclusively from Microsoft Sentinel to Google SecOps. For the job to identify the correct information, the Google SecOps case must have the Microsoft Sentinel Incident tag. This job only works on alerts from the Microsoft Azure Sentinel Incident Connector v2.|
|Sync Incidents|Deprecated. This job synchronizes Google SecOps Alerts and Microsoft Sentinel Incidents. It ensures that comments, status, and tags are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the “Microsoft Sentinel Incident” tag. If the alert didn’t originate from “Microsoft Azure Sentinel Incident Connector v2”,  you will need to add an “Incident_ID” context value to the case for the job to be able to find the correct information.|

