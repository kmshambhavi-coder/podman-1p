
# Automox

Automox is the modern, cloud-native endpoint-hardening platform that empowers organizations to remediate vulnerabilities faster than they can be weaponized.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the Automox instance.|True|String|https://{{api_root}}|
|API Key|API key of the Automox instance.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Automox is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|idna-3.10-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|urllib3-2.2.3-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|


## Actions
#### Enrich Entities
Enrich entities using information from Automox. Supported entities: Hostname, IP Address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Return Patches|If enabled, action will return a list of patches that need to be updated on the machine. Note: action will not return patches that were installed or the ones that are currently ignored.|False|Boolean|true|
|Max Patches To Return|Specify how many patches to return. If nothing is provided, action will return 50 patches.|False|String|50|



##### JSON Results
```json
[{"Entity":"111.11.111.111","EntityResult":{"id":2326721,"agent_version":"1.41.125","commands":[],"compatibility_checks":{"missing_powershell":false,"low_diskspace":false,"missing_wmi_integrity_check":false},"compliant":true,"connected":true,"create_time":"2022-11-17T08:32:39+0000","custom_name":"","deleted":false,"detail":{"LAST_USER_LOGON":{"USER":"XXXXX","TIME":"11/21/2022 1:34:28 AM","SRC":"XXXXX"},"MDM_SERVER":null,"MODEL":"VMware7,1","FQDNS":["XXXXX.WORKGROUP"],"NICS":[{"MAC":"00:50:56:A2:AC:66","IPS":["111.11.111.111","fe80::8ecc:52f1:d111:1111"],"CONNECTED":true,"VENDOR":"Intel(R) 82574L Gigabit Network Connection","DEVICE":"Ethernet0","TYPE":"enet"}],"IPS":["111.11.111.111","fe80::8ecc:52f1:d111:1111"],"CPU":"Intel(R) Xeon(R) CPU E5-2698 v3 @ 2.30GHz","DISKS":[{"TYPE":"VMware Virtual disk SCSI Disk Device","SIZE":"64420392960"}],"AUTO_UPDATE_OPTIONS":{"OPTIONS":"off","ENABLED":"0"},"WSUS_CONFIG":{"WSUS_REACHABLE":"0","WSUS_MANAGED":"0","WSUS_SERVER":""},"UPDATE_SOURCE_CHECK":{"CONNECTED":"True","ERROR":"Succeeded"},"SERIAL":"VMware-42 22 e2 c7 6e 4e e2 d1-db 56 49 67 d0 60 57 d4","VERSION":"440BX Desktop Reference Platform","RAM":"8589934592","SERVICETAG":"No Asset Tag","PS_VERSION":"5.1.19041.1682","SECURE_TOKEN_ACCOUNT":null,"WMI_INTEGRITY_CHECK":"True","DISTINGUISHED_NAME":"","VOLUME":[{"FSTYPE":"NTFS","LABEL":"Local Disk","AVAIL":"63766056960","FREE":"28025298944","IS_SYSTEM_DISK":"True","VOLUME":"C:"}],"MDM_PROFILE_INSTALLED":null,"VENDOR":"VMware, Inc."},"display_name":"ATMX-03","exception":false,"instance_id":"","ip_addrs":["111.11.111.111"],"ip_addrs_private":["176.11.111.111","fe80::8eff:52c1:d111:b111"],"is_compatible":true,"is_delayed_by_notification":false,"is_delayed_by_user":false,"last_disconnect_time":null,"last_logged_in_user":"XXXXX","last_process_time":"2022-11-21T09:35:07+0000","last_refresh_time":"2022-11-21T14:21:21+0000","last_scan_failed":false,"last_update_time":"2022-11-18T11:06:48+0000","mdm":null,"name":"XXXXX","needs_attention":false,"needs_reboot":false,"next_patch_time":null,"notification_count":0,"organization_id":104833,"organizational_unit":"","os_family":"Windows","os_name":"10 Enterprise Evaluation","os_version":"10.0.19043","os_version_id":4876,"patch_deferral_count":0,"patches":6,"pending":false,"pending_patches":0,"policy_status":[{"id":111111112,"organization_id":111111,"policy_id":251870,"server_id":111111,"policy_name":"Policy1-OSUpdatesHighMedium_withNotificationsSeverity","policy_type_name":"patch","status":1,"result":"{}","create_time":"2022-11-21T14:26:12+0000","will_reboot":false,"pending_count":0,"next_remediation":null},{"id":111111111,"organization_id":111111,"policy_id":251874,"server_id":111111,"policy_name":"Policy4_inactive_Browsers","policy_type_name":"patch","status":1,"result":"{}","create_time":"2022-11-21T14:31:17+0000","will_reboot":false,"pending_count":0,"next_remediation":null}],"reboot_deferral_count":0,"reboot_is_delayed_by_notification":false,"reboot_is_delayed_by_user":false,"reboot_notification_count":0,"refresh_interval":240,"serial_number":"VMware-42 22 e2 c7 6e 4e e2 d1-db 56 49 67 d0 60 57 d4","server_group_id":111111,"server_policies":[],"status":{"device_status":"ready","agent_status":"connected","policy_status":"compliant","policy_statuses":[{"id":251870,"compliant":true},{"id":251874,"compliant":true}]},"tags":["Recently Added"],"timezone":"UTC-0800","total_count":1,"uptime":"19770","uuid":"4eb1e92e-f3b8-4467-ba29-35c1c8ac4321","list_of_patches":[{"id":2132927299,"server_id":2326721,"package_id":235849952,"software_id":470331,"installed":false,"ignored":false,"group_ignored":false,"deferred_until":null,"group_deferred_until":null,"name":"VLC_32","display_name":"VLC","version":"3.0.17","repo":"VLC Media Player","cves":[],"cve_score":null,"agent_severity":null,"severity":null,"package_version_id":248242330,"os_name":"10 Enterprise Evaluation","os_version":"10.0.19043","os_version_id":4876,"create_time":"2022-11-18T17:10:34+0000","requires_reboot":false,"patch_classification_category_id":null,"patch_scope":null,"is_uninstallable":false,"secondary_id":null,"is_managed":true,"impact":null,"organization_id":104833},{"id":2136187006,"server_id":2326721,"package_id":227229244,"software_id":732567,"installed":false,"ignored":false,"group_ignored":false,"deferred_until":null,"group_deferred_until":null,"name":"KB2267602","display_name":"Security Intelligence Update for Microsoft Defender Antivirus - KB2267602","version":"1.379.706.0","repo":"WindowsUpdate","cves":[],"cve_score":null,"agent_severity":null,"severity":null,"package_version_id":248294084,"os_name":"10 Enterprise Evaluation","os_version":"10.0.19043","os_version_id":4876,"create_time":"2022-11-21T10:29:46+0000","requires_reboot":false,"patch_classification_category_id":null,"patch_scope":null,"is_uninstallable":false,"secondary_id":null,"is_managed":true,"impact":0,"organization_id":104833}]}}]
```



#### Execute Device Command
Execute a command on the endpoint in Automox. Supported entities: Hostname, IP Address. Note: Action is running as async, please adjust script timeout value in Chronicle SOAR for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Command|Specify a command that needs to be executed on the device. Note: if "Install Specific Patches" is provided, parameter "Patch Names" is mandatory.|False|List|Scan Device|
|Patch Names|Specify a comma-separated list of patches that need to be installed.|False|String||



##### JSON Results
```json
[{"Entity": "111.11.111.111", "EntityResult": {"id": "8527028217", "server_id": "2263017", "command_id": "164850699", "organization_id": "104513", "args": "ASD", "reboot": "0", "exec_time": "2022-10-25T08:02:43+0000", "response": ["0", "Installing MS updates: ASD\r\nCouldn't find update for ASD, skipping.\r\nNothing left to do", "null"], "response_time": "2022-10-25T08:22:14+0000", "policy_id": "null", "agent_command_type": "0", "command_type_name": "InstallUpdate"}}]
```



#### Execute Policy
Execute a policy in Automox. Supported entities: Hostname, IP Address.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Remediation Scope|Specify the remediation scope for the action. If “Only Entities” is selected, then action will execute policies only on the valid entities in the scope. If “All Devices” is selected, then action will execute the policy on all devices in the organization.|True|List|All Devices|
|Policy Name|Specify the name of the policy that needs to be executed.|True|String||



##### JSON Results
```json
[{"Entity": "xxxx-11", "EntityResult": {"status": "done"}}, {"status": "failure"}]
```



#### List Policies
List available policies in Automox.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Key|Specify the key that needs to be used to filter policy.|False|List|Select One|
|Filter Logic|Specify what filter logic should be applied. Filtering logic is working based on the value  provided in the “Filter Key” parameter.|False|List|Not Specified|
|Filter Value|Specify what value should be used in the filter. If “Equal“ is selected, action will try to find the exact match among results and if “Contains“ is selected, action will try to find results that contain that substring. If nothing is provided in this parameter, the filter will not be applied. Filtering logic is working based on the value  provided in the “Filter Key” parameter.|False|String||
|Max Records To Return|Specify how many records to return. If nothing is provided, action will return 50 records.|False|String|50|



##### JSON Results
```json
[{"id": "1111111", "name": "Apply All Patches", "policy_type_name": "patch", "organization_id": "1111111", "configuration_auto_patch": "False", "configuration_patch_rule": "all", "configuration_auto_reboot": "False", "configuration_notify_user": "False", "configuration_include_optional": "True", "configuration_notify_reboot_user": "True", "configuration_missed_patch_window": "True", "configuration_custom_notification_max_delays": "3", "configuration_custom_notification_deferment_periods_1": "1", "configuration_custom_notification_deferment_periods_2": "2", "configuration_custom_notification_deferment_periods_3": "4", "schedule_days": "254", "schedule_weeks_of_month": "62", "schedule_months": "8190", "schedule_time": "17:00", "notes": "", "create_time": "2022-10-24T08:44:37+0000", "server_groups_1": 111111, "server_count": "1", "status": "inactive"}]
```



#### Ping
Test connectivity to the Automox with parameters provided at the integration configuration page on the Marketplace tab
Timeout - 600 Seconds









