
# Cylance

BlackBerry Cylance is an advanced threat protection platform that, unlike other traditional endpoint protection software, makes no use of malware signatures. Instead, it employs techniques such as machine learning and artificial intelligence, which allows the identification of malicious code based on its behavior. This ensures protection even against zero-day codes, malware that has never been seen before. Among its key features, Cylance includes: True zero-day prevention, AI-driven malware prevention, Script management, Device usage policy enforcement, Memory exploitation detection and prevention, Application control for fixed-function devices

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address||True|String|https://<server-address>|
|Application ID||True|String||
|Application Secret||True|Password|*****|
|Tenant Identifier||True|String||


#### Dependencies
| |
|-|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|pytz-2022.1-py2.py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|PyJWT-2.8.0-py3-none-any.whl|


## Actions
#### Change Policy
Change the policy of an endpoint to an existing policy
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|The new policy name|True|String||



#### Get Global List
Retrieve a list of all hashes in the specified global list (GlobalSafe or GlobalQuarantine)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Type|Name of the global list. e.g. GlobalSafe|True|String||



##### JSON Results
```json
[{"category": "Drivers", "added": "2018-04-01T16:14:01", "name": "MaliciousFile.exe", "classification": "", "sub_classification": "", "av_industry": null, "reason": "Testing actions", "list_type": "GlobalSafe", "sha256": "9890B2F415D096B3E5B259C414166C7E0C7C2BE7AB7FBE0C30ACC67AA78D7BC6", "cylance_score": -0.999, "added_by": "a4366b76-669e-46ac-acb8-67d1d8e2c5ed", "md5": "F0D291E88A11CCCF31BC358DCB83ACC2"}, {"category": "Drivers", "added": "2018-04-01T13:13:03", "name": "ThisWillDestroyYourComputer.exe", "classification": "", "sub_classification": "", "av_industry": null, "reason": "Testing actions", "list_type": "GlobalSafe", "sha256": "EB83B77112874E1082BBD529182DD22C5C0BFD2390E4C1584CBE1C50CBB3FD03", "cylance_score": -0.999, "added_by": "a4366b76-669e-46ac-acb8-67d1d8e2c5ed", "md5": "8A1B7AF7A850493D3683C6EC660CA454"}]
```



#### Get Threat Devices
Get threats associated to a particular hostname or an IP address
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": [{"name": "DESKTOP-CL0OJIN", "ip_addresses": ["169.254.195.84", "192.168.2.100"], "mac_addresses": ["02-00-4C-4F-4F-50", "CC-2F-71-24-2D-59"], "id": "0805c701-009b-4d2a-8d52-142e3af38c33", "state": "OffLine", "date_found": "2018-03-28T20:34:44", "file_status": "Quarantined", "agent_version": "2.0.1480", "file_path": "C:\\Users\\Daniel\\Downloads\\mpress.219\\mpress.exe", "policy_id": "1429b00e-50bc-4038-bcae-04935713aabf"}], "Entity": "2852680c94a9d68cdab285012d9328a1ceca290db60c9e35155c2bb3e46a41b4"}]
```



#### Get Threats
Retrieve a list of all available threats in the system
Timeout - 600 Seconds



##### JSON Results
```json
[{"cylance_score": -0.999, "name": "BADguyFILE.exe", "classification": "", "last_found": "2018-03-29T14:26:56", "av_industry": null, "unique_to_cylance": false, "global_quarantined": false, "sub_classification": "", "file_size": 31246, "safelisted": false, "sha256": "19D51872FEC52363589C46E869B9A7A7EC567CB2AED6DBF9B206FC04AE7361DA", "md5": "859214628259F59A1DD3ABE8C3201346"}, {"cylance_score": -1.0, "name": "mpress.exe", "classification": "Trusted", "last_found": "2018-03-28T20:34:44", "av_industry": null, "unique_to_cylance": true, "global_quarantined": false, "sub_classification": "Local", "file_size": 103424, "safelisted": false, "sha256": "2852680C94A9D68CDAB285012D9328A1CECA290DB60C9E35155C2BB3E46A41B4", "md5": "8B632BFC3FE653A510CBA277C2D699D1"}]
```



#### Ping
Test connectivity to Cylance
Timeout - 600 Seconds



#### Delete From Global List
Remove a hash for the specified global list (GlobalSafe or GlobalQuarantine)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Type|The list to delete the hash from. e.g. GlobalSafe|True|String||



#### Get Threat Download Link
Action fetches The URL you can use to download the file. The action only provides the URL, it does not download the file for you.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threat SHA256 Hash|Threat SHA256 hashes, in a comma separated list. Note - if parameter value will be left empty, action will use file hash entities as input.|False|String||



##### JSON Results
```json
[{"Entity": "xxxxxxxxxxbc70759c9d524cbbac2c3d46c4aed10ac57f622086e71032226295", "EntityResult": {"url": "https://cylanceephemeralfilestore.s3.amazonaws.com/xx/28/DE/xx/xxxxxxxxxxBC70759C9D524CBBAC2C3D46C4AED10AC57F622086E71032226295.zip?Signature=xxxxxxxxxxOhVCOBegxqzCD%2Ftfs%3D&Expires=1608059967&AWSAccessKeyId=xxxxxxxxxx2YTYVBFRFA"}}, {"Entity": "xxxxxxxxxx7c49b233cace747951911f320bd43be8a79ce455b97403c2f7de2c", "EntityResult": {"url": "https://cylanceephemeralfilestore.s3.amazonaws.com/xx/37/A0/xx/xxxxxxxxxx7C49B233CACE747951911F320BD43BE8A79CE455B97403C2F7DE2C.zip?Signature=xxxxxxxxxx7aIjdokpB5agK2B7Y%3D&Expires=1608059968&AWSAccessKeyId=xxxxxxxxxx2YTYVBFRFA"}}]
```



#### Change Zone
Change zone for an endpoint (group of endpoints)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Zones to Add|The new Zone to add. Comma separated.|False|String||
|Zones to Remove|The Zone to be removed. Comma separated.|False|String||



#### Get Threat
Enrich a hash with data from Cylance
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark entity as suspicious if the threat Cylance score pass the given threshold. e.g. 3|True|String|0|



##### JSON Results
```json
[{"EntityResult": {"cylance_score": -1.0, "name": "mpress.exe", "classification": "Trusted", "last_found": "2018-03-28T20:34:44", "av_industry": null, "unique_to_cylance": true, "global_quarantined": false, "file_size": 103424, "safelisted": false, "sha256": "2852680C94A9D68CDAB285012D9328A1CECA290DB60C9E35155C2BB3E46A41B4", "md5": "8B632BFC3FE653A510CBA277C2D699D1", "sub_classification": "Local"}, "Entity": "8B632BFC3FE653A510CBA277C2D699D1"}]
```



#### Enrich Entities
Enrich hostnames and IP addresses with additional data from Cylance
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"update_available": false, "date_last_modified": "2012-01-16T10:04:27", "distinguished_name": "CN=PC-01,CN=Computers,DC=DOMAIN,DC=COM", "policy": {"id": "1413b00e-50bc-4438-base-04935713aabf", "name": "A_policy"}, "date_offline": null, "ip_addresses": ["1.92.168.0.3"], "mac_addresses": ["AB-CD-C4-12-A2-73"], "last_logged_in_user": "DOMAIN\\user", "agent_version": "2.0.1510", "os_version": "Microsoft Windows 10 Pro", "state": "Online", "update_type": null, "date_first_registered": "2012-03-27T11:35:12", "host_name": "PC-01.DOMAIN.COM", "is_safe": true, "background_detection": false, "id": "8e501f3b-d3c3-4549-94af-5b3335af247d", "name": "PC-01"}, "Entity": "PC-01"}]
```



#### Add To Global List
Add a hash to one of the two global lists: GlobalSafe or GlobalQuarantine
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Type|The list to add the hash to. e.g. GlobalSafe|True|String|GlobalSafe|
|Category|The category of the hash|False|String|None|
|Reason|The reason for adding the hash to the list|False|String||









## Connectors
#### Cylance connector
Cylance connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|60|
|Api Root|https://<instance>.cylance.com|True|String|None|
|DeviceProductField|The field name used to determine the device product|True|String|device_product|
|EventClassId|The field name used to determine the event name (sub-type)|False|String|cylance_event|
|Application Secret| Used to sign the Application ID|True|Password|*****|
|Application ID|Used to indicate the token requested|True|String|None|
|Tenant Identifier|ID number of tenant information being queried|True|String|None|
|Proxy Server Address|The address of the proxy server to use.|False|String|None|
|Proxy Username|The proxy username to authenticate with.|False|String|None|
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




