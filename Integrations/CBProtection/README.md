
# CBProtection

Cb Protection delivers application control and critical infrastructure protection to lock down servers, critical systems and fixed-function devices in highly regulated environments.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|IP_OR_HOST|https://x.x.x.x|
|Api Key|None|True|String||


#### Dependencies
| |
|-|
|urllib3-2.2.1-py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|prompt_toolkit-3.0.43-py3-none-any.whl|
|protobuf-5.26.1-cp37-abi3-manylinux2014_x86_64.whl|
|certifi-2024.2.2-py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|requests-2.31.0-py3-none-any.whl|
|validators-0.28.1-py3-none-any.whl|
|types_python_dateutil-2.9.0.20240316-py3-none-any.whl|
|cbapi-1.7.10-py2.py3-none-any.whl|
|solrq-1.1.2-py2.py3-none-any.whl|
|wcwidth-0.2.13-py2.py3-none-any.whl|
|cachetools-5.3.3-py3-none-any.whl|
|pika-1.3.2-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|PyYAML-6.0.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pygments-2.17.2-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|packaging-24.0-py3-none-any.whl|


## Actions
#### Block Hash
Block a hash on specific policies or globally
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Names|e.g. Default Policy,Local Approval Policy|False|String||



#### Find File
Find a file instance on multiple computers
Timeout - 600 Seconds



#### Get System Info
Get information about a computer
Timeout - 600 Seconds



#### Get Computers By File
Get the computers on which a file with the given SHA-256 value exists
Timeout - 600 Seconds



#### Change Computer Policy
Move a computer to a new policy
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|The new policy name. e.g. Default Policy|True|String||



#### Unblock Hash
Unblock a hash on specific policies or globally.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Names|Separated by comma. e.g. Default Policy,Local Approval Policy|False|String||



#### Analyze File
Analyze a file
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Connector Name|The name of the analyzing connector. e.g. Palo Alto Networks|True|String||
|Priority|The priority of the analysis (-2 to 2)|True|String||
|Timeout|Wait timeout. e.g. 120|True|String||



#### Ping
Test connectivity
Timeout - 600 Seconds









