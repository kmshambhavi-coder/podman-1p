
# Office365ManagementAPI

The Office 365 Management APIs provide a single extensibility platform for all Office 365 customers' and partners' management tasks, including service communications, security, compliance, reporting, and auditing.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|String|https://manage.office.com|
|Azure Active Directory ID|None|True|String||
|Client ID|None|True|String||
|Client Secret|None|False|Password|*****|
|Certificate Path|None|False|String||
|Certificate Password|None|False|Password|*****|
|OAUTH2 Login Endpoint Url|None|True|String|https://login.microsoftonline.com|
|Verify SSL|None|False|Boolean|True|


#### Dependencies
| |
|-|
|requests-2.32.3-py3-none-any.whl|
|cryptography-43.0.1-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|PyJWT-2.9.0-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|cffi-1.17.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pycparser-2.22-py3-none-any.whl|
|idna-3.8-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|pyOpenSSL-24.2.1-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|


## Actions
#### Stop Subscription
Stop a subscription to a chosen Office 365 Management API content type. Note: When a subscription is stopped, you will no longer receive notifications and you will not be able to retrieve available content. If the subscription is later restarted, you will have access to new content from that point forward. You will not be able to retrieve content that was available between the time the subscription was stopped and restarted.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Stop a Subscription for|Specify for which content type to stop a subscription.|True|List|Select content type|



#### Start Subscription
Start a subscription to a chosen Office 365 Management API content type.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Start a Subscription for|Specify for which content type to start a subscription.|True|List|Select content type|



#### Ping
Test connectivity to the O365 Management API service with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### Office 365 Management API Audit General Events Connector
Fetch Audit.General events from  Office 365 Management API. Please make sure that first you enabled subscription for Audit.General events by running "Start a Subscription" action.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Api Root|Api root url to use with integration.|True|String|https://manage.office.com|
|Azure Active Directory ID|Azure Active Directory Tenant ID, can be viewed in Active Directory > App Registration > <Application you configured for your integration> > Directory (tenant) ID. Eg, k48f52ca-0000-4708-8ed0-0000a20a40a|True|String||
|Client ID|Client (Application) ID that was added for the app registration in Azure Active Directory for this integration. Eg, 29bf818e-0000-0000-0000-784fb644178d|True|String||
|Client Secret|Secret that was entered for Azure AD app registration. Eg, XF00000Qc0000000[UZSW7-0?qXb6Qx]|False|Password|*****|
|Certificate Path|If authentication based on certificates is used instead of client secret, specify path to the certificate on Siemplify server.|False|String||
|Certificate Password|Optional, if certificate is password-protected, specify the password to open the certificate file.|False|Password|*****|
|OAUTH2 Login Endpoint Url|Specify the url connector should use for OAUTH2 Login Endpoint Url|True|String|https://login.microsoftonline.com|
|Verify SSL|Specify whether remote API endpoint SSL certificate should be validated.|False|Boolean|true|
|Type of Operation Filter|In audit.general schema there could be different operation types:SearchAirBatch, SearchCustomTag and so on. By default if nothing is specified in this parameter - ingest all possible operation types. If operation type is specified in this parameter - event with this operation type will not be ingested. Parameter accepts multiple values as a comma separated string.|False|String||
|Status Filter|Parameter can be used to specify status that if present in event, event will not be ingested. Parameter works as a blacklist. By default if nothing is specified - ingest all possible status types. Parameter accepts multiple values as a comma separated string.|False|String||
|Use operation and status filters as whitelist|If enabled, operation and status filters will work as a whitelist, by default its a blacklist|False|Boolean|false|
|Entity Keys to Create Additional Events|Specify keys that if seen in the Audit.General entities section of data, related subsection should be taken to create an additional Siemplify event.|False|String|mailMessage, mailbox, ip|
|Max events to fetch|How many events to process per one connector iteration.|True|Int|50|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. Note that O365 Management API allows to return events for the last 7 days, not older.|True|Int|8|
|Fetch Backwards Time Interval (minutes)|Time interval connector should use to fetch events from max hours backwards. If O365 tenant is busy, it could return a lot of event blobs. Because of this, this parameter in minutes can be used to split max hours backwards on smaller segments and process them individually. Time interval cant be bigger than 24 hours in total.|True|Int|240|
|Events Padding Period (minutes)|Event Padding Period in minutes specifies a minimum time interval that will be used by connector to check new events.|True|Int|60|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|


#### Office 365 Management API DLP Events Connector
Fetch DLP events from  Office 365 Management API.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Api Root|Api root url to use with integration.|True|String|https://manage.office.com|
|Azure Active Directory ID|Azure Active Directory Tenant ID, can be viewed in Active Directory > App Registration > <Application you configured for your integration> > Directory (tenant) ID. Eg, k48f52ca-0000-4708-8ed0-0000a20a40a|True|String||
|Client ID|Client (Application) ID that was added for the app registration in Azure Active Directory for this integration. Eg, 29bf818e-0000-0000-0000-784fb644178d|True|String||
|Client Secret|Secret that was entered for Azure AD app registration. Eg, XF00000Qc0000000[UZSW7-0?qXb6Qx]|False|Password|*****|
|Certificate Path|If authentication based on certificates is used instead of client secret, specify path to the certificate on Siemplify server.|False|String||
|Certificate Password|Optional, if certificate is password-protected, specify the password to open the certificate file.|False|Password|*****|
|OAUTH2 Login Endpoint Url|Specify the url connector should use for OAUTH2 Login Endpoint Url|True|String|https://login.microsoftonline.com|
|Verify SSL|Specify whether remote API endpoint SSL certificate should be validated.|False|Boolean|true|
|Type of Operation Filter|The following operation types are available for DLP events: DlpRuleMatch, DlpRuleUndo, DlpInfo. Parameter works as a blacklist. By default if nothing is specified in this parameter - ingest all possible operation types. If operation type is specified in this parameter - event with this operation type will not be ingested. Parameter accepts multiple values as a comma separated string.|False|String||
|Type of Policy Filter|Parameter can be used to specify policy name that if present in event, event will not be ingested. Parameter works as a blacklist. By default if nothing is specified - ingest all possible policy types. Parameter accepts multiple values as a comma separated string.|False|String||
|Mask findings?|Specify whether the connector should mask sensitive findings that triggered DLP policies hits.|False|Boolean|false|
|Max events to fetch|How many events to process per one connector iteration.|True|Int|50|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires. Note that O365 Management API allows to return events for the last 7 days, not older.|True|Int|8|
|Fetch Backwards Time Interval (minutes)|Time interval connector should use to fetch events from max hours backwards. If O365 tenant is busy, it could return a lot of event blobs. Because of this, this parameter in minutes can be used to split max hours backwards on smaller segments and process them individually. Time interval cant be bigger than 24 hours in total.|True|Int|240|
|Events Padding Period (minutes)|Event Padding Period in minutes specifies a minimum time interval that will be used by connector to check new events.|True|Int|60|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




