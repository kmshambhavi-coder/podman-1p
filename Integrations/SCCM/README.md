
# SCCM

System Center Configuration Manager (SCCM) is a systems management software product developed by Microsoft for managing large groups of computers running Windows NT, Windows Embedded, macOS (OS X), Linux or UNIX, as well as Windows Phone, Symbian, iOS, and Android mobile operating systems. Configuration Manager provides remote control, patch management, software distribution, operating system deployment, network access protection and hardware, and software inventory. Users that will be specified in the integration configuration should be a member of the SMS admins group.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address|None|True|String|x.x.x.x|
|Domain|None|True|String|domain|
|Username|None|True|String||
|Password|None|True|Password|*****|


#### Dependencies
| |
|-|
|sh-1.12.14-py2.py3-none-any.whl|
|idna-3.8-py3-none-any.whl|
|mock-2.0.0-py2.py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|pbr-6.1.0-py2.py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|PyPika-0.48.9.tar.gz|
|setuptools-74.1.2-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|setuptools-80.9.0-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|wmi_client_wrapper_py3-2023.1-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|future-0.18.3.tar.gz|


## Actions
#### Enrich Entities
Enrich Siemplify Host, IP or User entities based on the information from the Microsoft SCCM.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity": "SCCM-SCCM", "EntityResult": [{"AADDeviceID": "00000000-0000-0000-0000-000000000000", "AADTenantID": "00000000-0000-0000-0000-000000000000", "Active": "1", "ADSiteName": "Default-First-Site-Name", "AgentName": ["SMS_WINNT_SERVER_DISCOVERY_AGENT,SMS_AD_SYSTEM_DISCOVERY_AGENT,SMS_AD_SECURITY_GROUP_DISCOVERY_AGENT,MP_ClientRegistration,Heartbeat Discovery"], "AgentSite": ["SCM,SCM,SCM,SCM,SCM"], "AgentTime": ["20200903121201.000000+***,20200903000002.000000+***,20200415051330.000000+***,20200518133142.000000+***,20200831134721.000000+***"], "AlwaysInternet": "0", "AMTFullVersion": null, "AMTStatus": "0", "Build": "10.0.14393", "BuildExt": "10.0.14393.693", "Client": "1", "ClientEdition": "0", "ClientType": "1", "ClientVersion": "5.00.8790.1007", "CPUType": "Intel64 Family 6 Model 63 Stepping 2", "CreationDate": "20200415115126.000000+***", "Decommissioned": "0", "DeviceOwner": "1", "DistinguishedName": "CN=SCCM-SCCM,OU=SCCM,OU=SCCM,DC=sccm-lab,DC=local", "EASDeviceID": null, "FullDomainName": "SCCM-LAB.LOCAL", "HardwareID": "2:292F7AD8AE8BDB4B3E27E8D38xxx45E5C188A7A3", "InternetEnabled": "0", "IPAddresses": ["172.30.000.000"], "IPSubnets": ["172.30.000.000"], "IPv6Addresses": ["fe80:0000:0000:0000:xxxx:xxxx:895c:a5b8"], "IPv6Prefixes": ["fe80:0000:0000:0000"], "IsAOACCapable": false, "IsAssignedToUser": true, "IsClientAMT30Compatible": "0", "IsMachineChangesPersisted": true, "IsPortableOperatingSystem": false, "IsVirtualMachine": false, "IsWriteFilterCapable": false, "LastLogonTimestamp": "20200902203552.000000+***", "LastLogonUserDomain": "SCCM-LAB", "LastLogonUserName": "Administrator", "MACAddresses": ["00:50:56:XX:XX:5E"], "ManagementAuthority": "0", "MDMComplianceStatus": null, "MDMDeviceCategoryID": null, "Name": "SCCM-SCCM", "NetbiosName": "SCCM-SCCM", "ObjectGUID": ["228,160,81,64,189,104,xxx,64,143,240,246,88,41,48,29,224"], "Obsolete": "0", "OperatingSystemNameandVersion": "Microsoft Windows NT Server 10.0", "OSBranch": "2", "PreviousSMSUUID": "GUID:7AxxxB96-F909-446A-AB7C-004B5160D1BC", "PrimaryGroupID": "515", "PublisherDeviceID": null, "ResourceDomainORWorkgroup": "SCCM-LAB", "ResourceId": "16777220", "ResourceNames": ["SCCM-SCCM.sccm-lab.local"], "ResourceType": "5", "SecurityGroupName": ["SCCM-LAB\\Domain Computers"], "SerialNumber": null, "SID": "S-1-5-21-3004247314-75612377-225089022xxx103", "SMBIOSGUID": "CF512242-192E-85EE-3359-244AE4xxxxxx", "SMSAssignedSites": ["SCM"], "SMSInstalledSites": ["SCM"], "SMSResidentSites": ["SCM"], "SMSUniqueIdentifier": "GUID:7A4A2B96-F909-446A-AB7C-004B5160xxxx", "SMSUUIDChangeDate": "202005xxx03142.000000+***", "SNMPCommunityName": null, "SuppressAutoProvision": "0", "SystemContainerName": [""], "SystemGroupName": ["SCCM-LAB\\Domain Computers"], "SystemOUName": ["SCCM-LAB.LOCAL/SCCM,SCCM-LAB.LOCAL/SCCM/SCCM"], "SystemRoles": ["AI Update Service Point,Data Warehouse Service Point,SMS Component Server,SMS Distribution Point,SMS Dmp Connector,SMS Endpoint Protection Point,SMS Fallback Status Point,SMS Management Point,SMS Notification Server,SMS Site Server,SMS Site System,SMS Software Update Point,SMS SQL Server,SMS SRS Reporting Point"], "Unknown": "0", "UserAccountControl": "4096", "VirtualMachineHostName": "", "VirtualMachineType": "0", "WipeStatus": "0", "WTGUniqueKey": null}]}]
```



#### Get Computer Properties
Deprecated, please use the "Enrich Entities" action instead. Get computer properties from MS SCCM instance and use obtained information to enrich the provided Siemplify Host entity.
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"ClientEdition": "None", "SMSInstalledSites": "()", "MDMDeviceCategoryID": "None", "ManagementAuthority": "None", "IPAddresses": "(u'1.1.1.1', u'1.1.1.1')", "EASDeviceID": "None", "ResourceType": "5", "Unknown": "None", "SID": "S-1-5-21-2485274276-3947876705-1900992244-1487", "DeviceOwner": "None", "IsWriteFilterCapable": "None", "HardwareID": "None", "IsMachineChangesPersisted": "None", "SMBIOSGUID": "None", "NetbiosName": "PC_01", "Build": "None", "AgentSite": "(u'001',)", "IPv6Addresses": "()", "Client": "None", "ResourceNames": "(u'PC-01.DOMAIN.COM',)", "PrimaryGroupID": "515", "ClientVersion": "None", "ClientType": "None", "PreviousSMSUUID": "None", "ResourceId": "2097152157", "IPv6Prefixes": "()", "ObjectGUID": "(189, 112, 106, 52, 65, 87, 150, 71, 166, 96, 209, 16, 161, 133, 38, 242)", "SMSAssignedSites": "(u'001',)", "SMSResidentSites": "(u'001',)", "IsPortableOperatingSystem": "None", "MDMComplianceStatus": "None", "WTGUniqueKey": "None", "AMTStatus": "None", "SystemGroupName": "()", "AgentName": "(u'SMS_AD_SYSTEM_DISCOVERY_AGENT',)", "Active": "None", "SNMPCommunityName": "None", "ADSiteName": "Default-First-Site-Name", "IsClientAMT30Compatible": "None", "IsVirtualMachine": "None", "AlwaysInternet": "None", "Decommissioned": "0", "Name": "PC-01", "SystemOUName": "()", "SuppressAutoProvision": "None", "SMSUniqueIdentifier": "None", "ResourceDomainORWorkgroup": "DOMAIN", "UserAccountControl": "4096", "LastLogonTimestamp": "20190203084427.000000+***", "AMTFullVersion": "None", "OperatingSystemNameandVersion": "Microsoft Windows NT Workstation 10.0", "PublisherDeviceID": "None", "SystemContainerName": "(u'DOMAIN\\\\COMPUTERS',)", "LastLogonUserName": "None", "InternetEnabled": "None", "SMSUUIDChangeDate": "None", "AgentTime": "(u'20190207115148.000000+***',)", "IsAssignedToUser": "None", "WipeStatus": "None", "SecurityGroupName": "()", "SystemRoles": "()", "DistinguishedName": "CN=PC-01,CN=Computers,DC=DOMAIN,DC=COM", "Obsolete": "None", "SerialNumber": "None", "FullDomainName": "DOMAIN.COM", "IsAOACCapable": "None", "MACAddresses": "()", "IPSubnets": "()", "VirtualMachineType": "None", "CPUType": "None", "CreationDate": "20190128134818.000000+***", "VirtualMachineHostName": "None", "OSBranch": "None", "LastLogonUserDomain": "None"}, "Entity": "PC_01"}]
```



#### Get Login History
Retrieve user login history from MS SCCM instance based on the provided Siemplify user entity.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Number of Records to Return|Maximum number of records to return in the action.|True|String|100|



##### JSON Results
```json
[{"EntityResult": [{"Username": "pc-01\\local_users", "LoginCount": 22, "LastLoggedIn": "20170815103710.000000+***"}], "Entity": "pc-01"}]
```



#### Ping
Test connectivity to Microsoft SCCM instance with parameters provided at the integration configuration page on Marketplace tab.
Timeout - 600 Seconds



#### Run WQL Query
Run arbitrary Windows Management Instrumentation Query Language (WQL) query against Microsoft SCCM Instance. Note: action is not using Siemplify entities to operate.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query to run|Specify WQL query to run. Consider the default example request for reference.|True|String|SELECT UniqueUserName,LastLoginTime,LoginCount,ResourceName from SMS_UserMachineIntelligence JOIN SMS_R_User ON SMS_UserMachineIntelligence.UniqueUserName = SMS_R_User.UniqueUserName WHERE SMS_R_User.UserPrincipalName = "sccm_user@sccm-domain.com"|
|Number of records to return|Maximum number of records to return in action.|True|String|100|



##### JSON Results
```json
[{"AADDeviceID": "00000000-0000-0000-0000-000000000000", "AADTenantID": "00000000-0000-0000-0000-000000000000", "Active": "1", "ADSiteName": "Default-First-Site-Name", "AgentName": ["SMS_WINNT_SERVER_DISCOVERY_AGENT,SMS_AD_SYSTEM_DISCOVERY_AGENT,SMS_AD_SECURITY_GROUP_DISCOVERY_AGENT,MP_ClientRegistration,Heartbeat Discovery"], "AgentSite": ["SCM,SCM,SCM,SCM,SCM"], "AgentTime": ["20200903121201.000000+***,20200903000002.000000+***,20200415051330.000000+***,20200518133142.000000+***,20200831134721.000000+***"], "AlwaysInternet": "0", "AMTFullVersion": null, "AMTStatus": "0", "Build": "10.0.xxxxx", "BuildExt": "10.0.14393.xxx", "Client": "1", "ClientEdition": "0", "ClientType": "1", "ClientVersion": "5.00.8790.xxxx", "CPUType": "Intel64 Family 6 Model 63 Stepping 2", "CreationDate": "20200415115126.000000+***", "Decommissioned": "0", "DeviceOwner": "1", "DistinguishedName": "CN=SCCM-SCCM,OU=SCCM,OU=SCCM,DC=sccm-lab,DC=local", "EASDeviceID": null, "FullDomainName": "SCCM-LAB.LOCAL", "HardwareID": "2:292F7AD8AE8BDB4B3E27E8D38FFF45xxxxxxxxxx", "InternetEnabled": "0", "IPAddresses": ["1.1.1.1"], "IPSubnets": ["1.1.1.1"], "IPv6Addresses": ["fe80:0000:0000:0000:4d9a:9074:xxxx:xxxx"], "IPv6Prefixes": ["xxxx:0000:0000:0000"], "IsAOACCapable": false, "IsAssignedToUser": true, "IsClientAMT30Compatible": "0", "IsMachineChangesPersisted": true, "IsPortableOperatingSystem": false, "IsVirtualMachine": false, "IsWriteFilterCapable": false, "LastLogonTimestamp": "20200902203552.000000+***", "LastLogonUserDomain": "SCCM-LAB", "LastLogonUserName": "Administrator", "MACAddresses": ["00:50:56:A2:xx:xx"], "ManagementAuthority": "0", "MDMComplianceStatus": null, "MDMDeviceCategoryID": null, "Name": "SCCM-SCCM", "NetbiosName": "SCCM-SCCM", "ObjectGUID": ["xxx,xxx"], "Obsolete": "0", "OperatingSystemNameandVersion": "Microsoft Windows NT Server 10.0", "OSBranch": "2", "PreviousSMSUUID": "GUID:7A4A2B96-F909-xxxx-AB7C-xxxxxxxxxxx", "PrimaryGroupID": "xxx", "PublisherDeviceID": null, "ResourceDomainORWorkgroup": "SCCM-LAB", "ResourceId": "xxxxxxxx", "ResourceNames": ["SCCM-SCCM.sccm-lab.local"], "ResourceType": "5", "SecurityGroupName": ["SCCM-LAB\\Domain Computers"], "SerialNumber": null, "SID": "S-1-5-xx-3004247314-75612377-xxxxxxxxxx-xxxx", "SMBIOSGUID": "CF512242-xxxx-85EE-3359-xxxxxxxxxx", "SMSAssignedSites": ["SCM"], "SMSInstalledSites": ["SCM"], "SMSResidentSites": ["SCM"], "SMSUniqueIdentifier": "GUID:7A4A2B96-xxxx-446A-AB7C-xxxxxxxxxxxx", "SMSUUIDChangeDate": "20200518203142.000000+***", "SNMPCommunityName": null, "SuppressAutoProvision": "0", "SystemContainerName": [""], "SystemGroupName": ["SCCM-LAB\\Domain Computers"], "SystemOUName": ["SCCM-LAB.LOCAL/SCCM,SCCM-LAB.LOCAL/SCCM/SCCM"], "SystemRoles": ["AI Update Service Point,Data Warehouse Service Point,SMS Component Server,SMS Distribution Point,SMS Dmp Connector,SMS Endpoint Protection Point,SMS Fallback Status Point,SMS Management Point,SMS Notification Server,SMS Site Server,SMS Site System,SMS Software Update Point,SMS SQL Server,SMS SRS Reporting Point"], "Unknown": "0", "UserAccountControl": "40xx", "VirtualMachineHostName": "", "VirtualMachineType": "0", "WipeStatus": "0", "WTGUniqueKey": null}, {"AADDeviceID": "00000000-0000-0000-0000-000000000000", "AADTenantID": "00000000-0000-0000-0000-000000000000", "Active": "1", "ADSiteName": "Default-First-Site-Name", "AgentName": ["SMS_AD_SYSTEM_DISCOVERY_AGENT,SMS_AD_SECURITY_GROUP_DISCOVERY_AGENT,MP_ClientRegistration,Heartbeat Discovery"], "AgentSite": ["SCM,SCM,SCM,SCM"], "AgentTime": ["20200903000002.000000+***,20200415051330.000000+***,20200518133221.000000+***,20200831133349.000000+***"], "AlwaysInternet": "0", "AMTFullVersion": null, "AMTStatus": "0", "Build": "1.1.1", "BuildExt": "1.1.1.1", "Client": "1", "ClientEdition": "0", "ClientType": "1", "ClientVersion": "5.00.xxxx.xxxx", "CPUType": "Intel64 Family 6 Model 63 Stepping 2", "CreationDate": "20200415121334.000000+***", "Decommissioned": "0", "DeviceOwner": "1", "DistinguishedName": "CN=SCCM-AD,OU=Domain Controllers,DC=sccm-lab,DC=local", "EASDeviceID": null, "FullDomainName": "SCCM-LAB.LOCAL", "HardwareID": "2:xxxxC90E1312C67C5787A8A102xxxxxxxxxxxxxx", "InternetEnabled": "0", "IPAddresses": ["1.1.1.1"], "IPSubnets": ["1.1.1.1"], "IPv6Addresses": [""], "IPv6Prefixes": [""], "IsAOACCapable": false, "IsAssignedToUser": true, "IsClientAMT30Compatible": "0", "IsMachineChangesPersisted": true, "IsPortableOperatingSystem": false, "IsVirtualMachine": true, "IsWriteFilterCapable": false, "LastLogonTimestamp": "20200827132153.000000+***", "LastLogonUserDomain": null, "LastLogonUserName": null, "MACAddresses": ["xx:50:56:xx:9C:xx"], "ManagementAuthority": "0", "MDMComplianceStatus": null, "MDMDeviceCategoryID": null, "Name": "SCCM-AD", "NetbiosName": "SCCM-AD", "ObjectGUID": ["xxx,xxx,xxx"], "Obsolete": "0", "OperatingSystemNameandVersion": "Microsoft Windows NT Server 10.0", "OSBranch": "2", "PreviousSMSUUID": "GUID:xxxxxxxx-B141-4B12-xxxx-95C14Dxxxxxx", "PrimaryGroupID": "xxx", "PublisherDeviceID": null, "ResourceDomainORWorkgroup": "SCCM-LAB", "ResourceId": "167xxxxx", "ResourceNames": ["SCCM-AD.sccm-lab.local"], "ResourceType": "5", "SecurityGroupName": ["SCCM-LAB\\Denied RODC Password Replication Group,SCCM-LAB\\Domain Controllers"], "SerialNumber": null, "SID": "S-1-5-21-xxxxxxxxxx-75612377-xxxxxxxxxx-xxxx", "SMBIOSGUID": "xxxxxxxx-A9DD-8BA6-xxxx-D09Axxxxxxxx", "SMSAssignedSites": ["SCM"], "SMSInstalledSites": ["SCM"], "SMSResidentSites": ["SCM"], "SMSUniqueIdentifier": "GUID:xxxxxxxx-B141-4B12-xxxx-95C14Dxxxxxx", "SMSUUIDChangeDate": "20200518203221.000000+***", "SNMPCommunityName": null, "SuppressAutoProvision": "0", "SystemContainerName": [""], "SystemGroupName": ["SCCM-LAB\\Denied RODC Password Replication Group,SCCM-LAB\\Domain Controllers"], "SystemOUName": ["SCCM-LAB.LOCAL/DOMAIN CONTROLLERS"], "SystemRoles": [""], "Unknown": "0", "UserAccountControl": "53xxxx", "VirtualMachineHostName": "", "VirtualMachineType": "0", "WipeStatus": "0", "WTGUniqueKey": null}]
```









