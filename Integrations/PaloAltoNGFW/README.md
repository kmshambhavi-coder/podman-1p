
# PaloAltoNGFW

Palo Alto Networks next-generation firewalls are architected to safely enable applications and prevent modern threats.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|String|https://x.x.x.x/api|
|Username|None|True|String||
|Password|None|True|Password|*****|
|Verify SSL|None|False|Boolean|False|


#### Dependencies
| |
|-|
|urllib3-2.2.1-py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|defusedxml-0.7.1-py2.py3-none-any.whl|
|xmltodict-0.13.0-py2.py3-none-any.whl|
|certifi-2024.2.2-py3-none-any.whl|
|requests-2.31.0-py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|


## Actions
#### Unblock ips in policy
Unblock IP addresses in a policy (each IP address is removed individually from the policy).
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|The device name in which the group is located. The default device name of NGFW is localhost.localdomain. In case configured differently, please refer to https://<NGFWIP>/php/rest/browse.php/config::devices for the list of all the device names and select the relevant device.|True|String||
|Vsys Name|The vsys in which the group is located. The default vsys name of NGFW is vsys1. In case configured differently, please refer to https://<NGFW IP>/php/rest/browse.php/config::devices::entry[@name='<DEVICE NAME>']::vsys for the list of all the vsys names of the device and select the relevant vsys.|True|String||
|Policy Name|Policy name value.|True|String||
|Target|Has to be source or destination.|True|String||



#### Commit Changes
Commit changes in Palo Alto NGFW. NOTICE! For using Only My Changes option, the user must be an admin.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Only My Changes|Commit only the configured use changes.|False|Boolean|true|



#### Remove Ips from group
Remove IP addresses from an address group
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|The device name in which the group is located. The default device name of NGFW is localhost.localdomain. In case configured differently, please refer to https://<NGFWIP>/php/rest/browse.php/config::devices for the list of all the device names and select the relevant device.|False|String||
|Vsys Name|The vsys in which the group is located. The default vsys name of NGFW is vsys1. In case configured differently, please refer to https://<NGFW IP>/php/rest/browse.php/config::devices::entry[@name='<DEVICE NAME>']::vsys for the list of all the vsys names of the device and select the relevant vsys.|False|String||
|Address Group Name|The name of the required address group.|True|String||
|Use Shared Objects|If enabled, action will use shared objects instead of vsys. Note: action will not create a shared address group, if it doesn't exist.|False|Boolean|false|



#### Edit Blocked Applications
Block and unblock applications. Each application is added to or removed from a given policy.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Applications To Block|List of applications to block, comma separated, e.g: apple-siri,app2.|False|String||
|Applications To UnBlock|List of applications to unblock, comma separated, e.g: apple-siri,app2.|False|String||
|Device Name|The device name in which the group is located. The default device name of NGFW is localhost.localdomain. In case configured differently, please refer to https://<NGFWIP>/php/rest/browse.php/config::devices for the list of all the device names and select the relevant device.|True|String||
|Vsys Name|The vsys in which the group is located. The default vsys name of NGFW is vsys1. In case configured differently, please refer to https://<NGFW IP>/php/rest/browse.php/config::devices::entry[@name='<DEVICE NAME>']::vsys for the list of all the vsys names of the device and select the relevant vsys.|True|String||
|Policy Name|Policy name value.|True|String||



#### Unblock Urls
Remove URLs from a given URL category
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|The device name in which the group is located. The default device name of NGFW is localhost.localdomain. In case configured differently, please refer to https://<NGFWIP>/php/rest/browse.php/config::devices for the list of all the device names and select the relevant device.|False|String||
|Vsys Name|The vsys in which the group is located. The default vsys name of NGFW is vsys1. In case configured differently, please refer to https://<NGFW IP>/php/rest/browse.php/config::devices::entry[@name='<DEVICE NAME>']::vsys for the list of all the vsys names of the device and select the relevant vsys.|False|String|vsys1|
|URL Category Name|URL Category Name|True|String||
|Use Shared Objects|If enabled, action will use shared objects instead of vsys.|False|Boolean|false|



#### Add Ips to group
Add IP addresses to an address group
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|The device name in which the group is located. The default device name of NGFW is localhost.localdomain. In case configured differently, please refer to https://<NGFWIP>/php/rest/browse.php/config::devices for the list of all the device names and select the relevant device.|False|String||
|Vsys Name|The vsys in which the group is located. The default vsys name of NGFW is vsys1. In case configured differently, please refer to https://<NGFW IP>/php/rest/browse.php/config::devices::entry[@name='<DEVICE NAME>']::vsys for the list of all the vsys names of the device and select the relevant vsys.|False|String||
|Address Group Name|Group name value.|True|String||
|Use Shared Objects|If enabled, action will use shared objects instead of vsys. Note: action will not create a shared address group, if it doesn't exist.|False|Boolean|false|



#### Block ips in policy
Block IP addresses in a policy (each IP is added individually to the policy)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|The device name in which the group is located. The default device name of NGFW is localhost.localdomain. In case configured differently, please refer to https://<NGFWIP>/php/rest/browse.php/config::devices for the list of all the device names and select the relevant device.|True|String||
|Vsys Name|The vsys in which the group is located. The default vsys name of NGFW is vsys1. In case configured differently, please refer to https://<NGFW IP>/php/rest/browse.php/config::devices::entry[@name='<DEVICE NAME>']::vsys for the list of all the vsys names of the device and select the relevant vsys.|True|String||
|Policy Name|Policy name value.|True|String||
|Target|Has to be source or destination.|True|String||



#### Get Blocked Applications
List all blocked applications in a given policy
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|The device name in which the group is located. The default device name of NGFW is localhost.localdomain. In case configured differently, please refer to https://<NGFWIP>/php/rest/browse.php/config::devices for the list of all the device names and select the relevant device.|True|String||
|Vsys Name|The vsys in which the group is located. The default vsys name of NGFW is vsys1. In case configured differently, please refer to https://<NGFW IP>/php/rest/browse.php/config::devices::entry[@name='<DEVICE NAME>']::vsys for the list of all the vsys names of the device and select the relevant vsys.|True|String||
|Policy Name|Policy name value.|True|String||



#### Block Urls
Add URLs to a given URL category (NOTE- To actually block the URL, create a policy and add the desired URL category to it.). Note: the length of URL can't exceed 255 characters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Device Name|The device name in which the group is located. The default device name of NGFW is localhost.localdomain. In case configured differently, please refer to https://<NGFWIP>/php/rest/browse.php/config::devices for the list of all the device names and select the relevant device.|False|String||
|Vsys Name|The vsys in which the group is located. The default vsys name of NGFW is vsys1. In case configured differently, please refer to https://<NGFW IP>/php/rest/browse.php/config::devices::entry[@name='<DEVICE NAME>']::vsys for the list of all the vsys names of the device and select the relevant vsys.|False|String||
|URL Category Name|Policy name value.|True|String||
|Use Shared Objects|If enabled, action will use shared objects instead of vsys.|False|Boolean|false|



#### Ping
Test connectivity to Panorama
Timeout - 600 Seconds









