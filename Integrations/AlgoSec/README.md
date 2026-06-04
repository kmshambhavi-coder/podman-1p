
# AlgoSec

Manage your network security effectively, swiftly, and confidently. No matter where your network lives. Gain complete visibility, automate changes, and always be compliant.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https:/{{ip address}}|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean|True|


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
#### Allow IP
Allow IPs in AlgoSec. Supported entities: IP address. Note: IP address entities are treated as destinations in the change request. This action creates a traffic change request to allow traffic to IP entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Template|Specify the template for the change request.|True|String|Standard|
|Source|Specify a comma-separated list of sources for the allow rule. It can be an IP address, IP Set or special keyword like (all).|True|String|all|
|Service|Specify a comma-separated list of services that needs to be allowed. Values can have a look of {TCP/UDP}/{port} (tcp/80) or special reserved keyword (all).|True|String|ALL|
|Subject|Specify the subject for the change request. If nothing is provided action will put "Siemplify Allow IP request" in the subject.|False|String||
|Owner|Specify who should be the owner of the change request. If nothing is provided, the user that created the ticket will be the owner.|False|String||
|Due Date|Specify the due date for the change request. Format: ISO 8601. Example: 2021-08-13T08:16:10Z.|False|String||
|Expiration Date|Specify the expiration date for the change request. Format: ISO 8601. Example: 2021-08-13T08:16:10Z.|False|String||
|Custom Fields|Specify a JSON object containing information about all of the fields that need to be added to the change request. Note: this parameter has a priority over other fields|False|String||



#### List Templates
List available templates in AlgoSec.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action will try to find the exact match among record types and if "Contains" is selected, action will try to find items that contain that substring. If nothing is provided in this parameter, the filter will not be applied.|False|String||
|Max Templates To Return|Specify how many templates to return. Default: 50.|False|String|50|



#### Block IP
Block IPs in AlgoSec. Supported entities: IP address. Note: IP address entities are treated as destinations in the change request. This action creates a traffic change request to block traffic to IP entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Template|Specify the template for the change request.|True|String|Standard|
|Source|Specify a comma-separated list of sources for the block rule. It can be an IP address, IP Set or special keyword like (all).|True|String|all|
|Service|Specify a comma-separated list of services that needs to be blocked. Values can have a look of {TCP/UDP}/{port} (tcp/80) or special reserved keyword (all).|True|String|ALL|
|Subject|Specify the subject for the change request. If nothing is provided action will put “Siemplify Block IP request” in the subject.|False|String||
|Owner|Specify who should be the owner of the change request. If nothing is provided, the user that created the ticket will be the owner.|False|String||
|Due Date|Specify the due date for the change request. Format: ISO 8601. Example: 2021-08-13T08:16:10Z.|False|String||
|Expiration Date|Specify the expiration date for the change request. Format: ISO 8601. Example: 2021-08-13T08:16:10Z.|False|String||
|Custom Fields|Specify a JSON object containing information about all of the fields that need to be added to the change request. Note: this parameter has a priority over other fields|False|String||



#### Wait for Change Request Status Update
Wait for change request status update in AlgoSec. Note: Action is running as async, please adjust script timeout value in Siemplify IDE for action as needed. Only traffic change requests are supported.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Request ID|Specify the id of the request for which action needs to check the status.|True|String||
|Status|Specify a comma-separated list of change request statuses for which action should wait. Possible values: resolved, reconcile, open, check, implementation plan, implement, validate.|True|String|resolved|



#### Ping
Test connectivity to the AlgoSec with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









