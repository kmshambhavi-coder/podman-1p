
# McAfeeMvisionEPO

McAfee MVISION ePO reduces incident response times, strengthens protection, and simplifies risk and security management using automation and end-to-end security visibility. McAfeeÂ® manages the platform infrastructure, upgrades, and maintenance.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|None|https://api.mvision.mcafee.com|
|Client ID||True|String||
|Client Secret||True|Password|*****|
|Scopes||True|String|epo.device.r, epo.device.w,epo.grps.r, epo.grps.w, epo.sftw.r, epo.tags.r, epo.tags.w|
|Group Name||False|String||
|Verify SSL||False|Boolean|True|


#### Dependencies
| |
|-|
|idna-3.13-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Add Tag
Add tag to the endpoint in McAfee Mvision ePO.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tag Name|Specify what tag you want to add to endpoint.|True|String||



#### Enrich Endpoint
Fetch endpoint's system information by its hostname or IP address.
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"id": "123", "uuid": "ae90f557-49bf-4945-9394-a3c361005xxx", "lastcommunicated": "2020-06-22T12:44:47.453+0000", "managedState": "managed", "properties": {"cpuspeed": 2300, "ipaddress": "1.1.1.1", "osplatform": "Workstation", "operatingsystem": "Windows 10", "cputype": "Intel(R) Xeon(R) CPU xxxx", "type": "non-portable", "numofcpu": 2, "hostname": "HW-HOST-023", "windowsdomain": "WORKGROUP", "dnsname": "HW-HOST-023", "totalphysicalmemory": 8588865536, "macaddress": "005056A24BC4", "username": "Admin"}, "group": {"groupId": "123", "name": "My System Tree Group Hebrew", "path": "My Organization My System Tree Group Hebrew", "link": {"rel": "group", "href": "../groups/403528"}}, "tags": [{"tagId": "123", "tagName": "Workstation", "link": {"rel": "tag", "href": "../tags/24751"}}], "productsInstalled": [{"product": "Agent", "version": "5.6.5.165"}, {"product": "MVISION EDR", "version": "3.1.0.482"}, {"product": "Management of Native Encryption", "version": "5.0.1.2"}, {"product": "DLP Endpoint", "version": "11.5.0.602"}, {"product": "MVISION Endpoint", "version": "20.6.0.87"}, {"product": "McAfee DXL Client", "version": "6.0.0.218"}, {"product": "McAfee Client Proxy", "version": "3.1.0.215"}]}, "Entity": "1.1.1.1"}]
```



#### List Endpoints In Group
List endpoints that are in the same group in McAfee Mvision ePO.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Endpoints to Return|Specify how many endpoints to return.|False|String|100|
|Group Name|Specify in which groups to search for endpoints|True|String||



##### JSON Results
```json
[{"id": "123", "uuid": "fef3d9aa-e58e-ea11-87c6-005056a21xxx", "description": "Description Agent", "lastcommunicated": "2020-06-23T13:34:13.870+0000", "managedState": "managed", "properties": {"cpuspeed": "123", "ipaddress": "1.1.1.1", "osplatform": "Workstation", "operatingsystem": "Linux", "cputype": "Intel(R) Xeon(R) CPU E5-2698 v3 @ 2.30GHz", "type": "non-portable", "numofcpu": "2", "hostname": "Centos7-001", "windowsdomain": "(none)", "dnsname": "Centos7-001", "totalphysicalmemory": "123", "macaddress": "005056A219xxx", "datversion": "4276.0", "amcorecontentdate": "2020-06-22 00:00:00.0", "username": "root"}, "group": {"groupId": "123", "name": "Linux", "path": "My OrganizationLinux", "link": {"rel": "group", "href": "example"}}, "tags": [{"tagId": "123", "tagName": "Workstation", "link": {"rel": "tag", "href": "example"}}], "productsInstalled": [{"product": "Agent", "version": "5.6.5.165"}, {"product": "MVISION EDR", "version": "3.1.0.482"}, {"product": "Endpoint Security Platform", "version": "10.7.0.130"}, {"product": "McAfee DXL Client", "version": "6.0.0.218"}, {"product": "Endpoint Security Threat Prevention", "version": "10.7.0.351"}]}]
```



#### List Groups
List groups that are available in McAfee Mvision ePO.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Groups to Return|Specify how many groups to return.|False|String|100|



##### JSON Results
```json
[{"id": 1, "name": "GlobalRoot", "userFriendlyName": "Global Root", "type": "7", "parentId": "0", "description": "", "textPath": "GlobalRoot", "links ": [{"rel": "self", "href": "1"}, {"rel": "parent ", "href": "0"}]}]
```



#### List Tags
List tags that are available in McAfee Mvision ePO.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Tags to Return|Specify how many tags to return.|False|String|100|



##### JSON Results
```json
[{"id": "24753", "name": "Excluded from Compliance Check", "description": "Protection Workspace tag for systems to be excluded from the compliance check", "links": [{"rel": "self", "href": "24753"}]}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Remove Tag
Remove tag from the endpoint in McAfee Mvision ePO.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Tag Name|Specify what tag  you want to remove from endpoint.|True|String||









