
# BMCRemedyITSM

BMC Remedy ITSM is industry-leading, service management that transforms the best-practice ITSM principles you've come to appreciate from Remedy to provide unprecedented ROI on your choice of cloud.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://{IP}:{port}|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean|true|


#### Dependencies
| |
|-|
|typing_extensions-4.15.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|TIPCommon-2.2.1-py2.py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|google_api_python_client-2.196.0-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pycparser-3.0-py3-none-any.whl|
|google_auth-2.53.0-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|anyio-4.13.0-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|protobuf-7.34.1-py3-none-any.whl|
|google_api_core-2.30.3-py3-none-any.whl|
|idna-3.15-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|httplib2-0.31.2-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|google_auth_httplib2-0.4.0-py3-none-any.whl|
|googleapis_common_protos-1.75.0-py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|proto_plus-1.28.0-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|cryptography-48.0.0-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|h11-0.16.0-py3-none-any.whl|


## Actions
#### Wait For Incident Fields Update
Wait for incident fields update in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify the ID of the incident that needs to be updated.|True|String||
|Status|Specify what is the expected status for the incident.|False|List|Select One|
|Fields To Check|Specify a JSON object containing all of the needed fields and values. Note: this parameter has priority over "Status" field.|False|String|{"field":"value"}|
|Fail If Timeout|If enabled, action will be failed, if not all of the fields were updated.|False|Boolean|true|



#### Delete Incident
Delete an incident in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify the id of the incident that needs to be deleted.|True|String||



#### Get Incident Details
Get detailed information about the incidents from BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident IDs|Specify the ids of incidents for which you want to return details.|True|String||
|Fields To Return|Specify what fields to return. If invalid fields are provided, action will fail. If nothing is provided, action will return all fields.|False|String||
|Fetch Work Notes|If enabled, action will return work notes related to the incident.|False|Boolean|true|
|Max Work Notes To Return|Specify how many Work Notes to return. If nothing is provided, action will return 50 Work Notes.|False|String|50|



#### Delete Record
Delete a record in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record that needs to be deleted.|True|String||
|Record ID|Specify the id of the record that needs to be deleted.|True|String||



#### Get Record Details
Get detailed information about the record from BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record for which you want to retrieve details.|True|String||
|Record IDs|Specify the ids of records for which you want to return details.|True|String||
|Fields To Return|Specify what fields to return. If invalid fields are provided, action will fail. If nothing is provided, action will return all fields.|False|String||



#### Update Incident
Update an incident in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify the id of the  incident that needs to be updated.|True|String||
|Status|Specify the status for the incident. Note: if status is "Pending" or "Resolved", then you also need to provide "Status Reason" value.|False|List|Select One|
|Status Reason|Specify the status reason for the incident.|False|String||
|Impact|Specify the impact for the incident.|False|List|Select One|
|Urgency|Specify the urgency for the incident.|False|List|Select One|
|Description|Specify the description of the incident|False|String||
|Incident Type|Specify the incident type for the incident.|False|List|Select One|
|Assigned Group|Specify the assigned group for the incident|False|String||
|Assignee|Specify the assignee for the incident|False|String||
|Resolution|Specify the resolution for the incident.|False|String||
|Resolution Category Tier 1|Specify the resolution category tier 1 for the incident.|False|String||
|Resolution Category Tier 2|Specify the resolution category tier 2 for the incident.|False|String||
|Resolution Category Tier 3|Specify the resolution category tier 3 for the incident.|False|String||
|Resolution Product Category Tier 1|Specify the resolution category tier 1 for the incident.|False|String||
|Resolution Product Category Tier 2|Specify the resolution category tier 2 for the incident.|False|String||
|Resolution Product Category Tier 3|Specify the resolution category tier 3 for the incident.|False|String||
|Reported Source|Specify the reported source.|False|List|Select One|
|Custom Fields|Specify a JSON object containing all of the needed fields and  values that need to be updated. Note: this parameter will overwrite other provided parameters.|False|String||



#### Add Work Note To Incident
Add a work note to incidents in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Incident ID|Specify the id of the incident to which you want to add a work note.|True|String||
|Work Note Text|Specify the text for the work note.|True|String||



#### Create Record
Create a record in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record that needs to be created.|True|String||
|Record Payload|Specify a JSON object containing all of the needed fields and  values.|True|String|{"field": "value"}|



#### Create Incident
Create an incident in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Status|Specify the status for the incident.|False|List|Select One|
|Impact|Specify the impact for the incident.|False|List|Select One|
|Urgency|Specify the urgency for the incident.|False|List|Select One|
|Description|Specify the description of the incident|False|String||
|Company|Specify the company for the incident|False|String||
|Customer|Specify the customer for the incident. Note: Customer needs to be provide in the format "{Last Name} {First Name}". Example: Allbrook Allen.|False|String||
|Template Name|Specify the name of the template for the incident. Note: action will try to find the ID of the template in the background. For better precision you can provide the template ID directly via Custom Fields.|False|String||
|Incident Type|Specify the incident type for the incident.|False|List|Select One|
|Assigned Group|Specify the assigned group for the incident|False|String||
|Assignee|Specify the assignee for the incident|False|String||
|Resolution|Specify the resolution for the incident.|False|String||
|Resolution Category Tier 1|Specify the resolution category tier 1 for the incident.|False|String||
|Resolution Category Tier 2|Specify the resolution category tier 2 for the incident.|False|String||
|Resolution Category Tier 3|Specify the resolution category tier 3 for the incident.|False|String||
|Resolution Product Category Tier 1|Specify the resolution category tier 1 for the incident.|False|String||
|Resolution Product Category Tier 2|Specify the resolution category tier 2 for the incident.|False|String||
|Resolution Product Category Tier 3|Specify the resolution category tier 3 for the incident.|False|String||
|Reported Source|Specify the reported source|False|List|Select One|
|Custom Fields|Specify a JSON object containing all of the needed fields and  values that need to be used during the creation. Note: this parameter will overwrite other provided parameters.|False|String||



#### Wait For Record Fields Update
Wait for record fields update in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record for which you are waiting an update.|True|String||
|Record ID|Specify the ID of the record that needs to be updated.|True|String||
|Fields To Check|Specify a JSON object containing all of the needed fields and values.|True|String|{"field":"value"}|
|Fail If Timeout|If enabled, action will be failed, if not all of the fields were updated.|False|Boolean|true|



#### Update Record
Update a record in BMC Remedy ITSM.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record that needs to be updated.|True|String||
|Record ID|Specify the id of the  record that needs to be updated.|True|String||
|Record Payload|Specify a JSON object containing all of the needed fields and values that need to be updated.|True|String|{"field": "value"}|



#### Ping
Test connectivity to the BMC Remedy ITSM with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds






## Jobs

#### Sync Closed Incidents By Tag
This job will synchronize BMC Remedy ITSM incidents that were created within Siemplify Case playbook and Siemplify cases. Note: in BMC Remedy ITSM statuses "Cancelled", "Closed" and "Resolved" are treated as closed. Additionally, in order for the job to work, it's required for the case to have 2 tags. First tag should be "BMC Remedy ITSM" and the second should be with the prefix "BMC Remedy ITSM:{Incident ID}". Job can only close incidents that are assigned in BMC Remedy ITSM.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Incident Table|True|String|HPD:IncidentInterface|
|API Root|True|String|https://{IP}:{port}|
|Username|True|String||
|Password|True|Password|*****|
|Environment|False|String||
|Max Hours Backwards|False|String|24|
|Verify SSL|False|Boolean|true|



