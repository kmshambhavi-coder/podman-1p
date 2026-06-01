
# CiscoThreatGrid

Threat Grid combines advanced sandboxing with threat intelligence into one unified solution to protect organizations from malware.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|IP_OR_HOST|https://x.x.x.x|
|Api Key||True|Password|*****|
|Use SSL||False|Boolean||


#### Dependencies
| |
|-|
|pycparser-3.0-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|paramiko-3.4.0-py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|bcrypt-5.0.0-cp39-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|idna-3.13-py3-none-any.whl|
|tzdata-2026.2-py2.py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|cryptography-47.0.0-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|six-1.17.0-py2.py3-none-any.whl|
|pynacl-1.6.2-cp38-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|arrow-1.4.0-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Get Submissions
Get submissions by entity
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Mark as suspicious if max threat score pass the threshold|True|String|50|
|Max Submissions To Return|Specify how many submissions to return per entitiy. Default: 10. Maximum: 100|False|String|10|



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Get Hash Associated IPs
Get IPs associated to a given hash
Timeout - 600 Seconds



#### Get Hash Associated Domains
Get domains associated to a given hash
Timeout - 600 Seconds



#### Upload Sample
Upload and analyze a sample. Note: Action is running as async, please adjust script timeout value in Siemplify IDE for action as needed
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Vm|The vm to run the analysis on. e.g. win7-x64|False|String|None|
|File Path|The sample file path|True|String|None|
|Playbook|Name of a playbook to apply to this sample run. e.g. default|False|String|None|
|Network Exit|Any outgoing network traffic that is generated during the analysis to appear to exit from the Network Exit Location.|False|String|None|
|Private|if checked, the sample will be marked private|False|Boolean|true|
|Linux Server Address|Specify the IP address of the remote linux server, where the file is located.|False|String||
|Linux Username|Specify the username of the remote linux server, where the file is located.|False|String||
|Linux Password|Specify the password of the remote linux server, where the file is located.|False|Password|*****|










Piranhas are generally misunderstood and rarely pose a threat to humans, despite their fearsome reputation. In fact, these fish typically consume smaller aquatic life and, when faced with people, usually flee rather than attack. Data suggests that piranhas are more frequently a food source for humans than the other way around, and they only bite when threatened or hungry