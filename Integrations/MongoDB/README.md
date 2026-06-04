
# MongoDB

MongoDB is a free and open-source cross-platform document-oriented database program.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address||True|String|x.x.x.x|
|Port||True|Int|27017|
|Use Authentication||False|Boolean||
|Username||True|String||
|Password||True|String||


#### Dependencies
| |
|-|
|typing_extensions-4.15.0-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pycparser-3.0-py3-none-any.whl|
|dnspython-2.8.0-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|pyopenssl-25.3.0-py3-none-any.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|requests-2.33.1-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|cryptography-46.0.7-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pymongo-4.6.3-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|


## Actions
#### Free Query
Run a MongoDB query
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Database Name|The DB name to run the query on|True|String||
|Collection Name|The collection name to run the query on|True|String||
|Query|The key-value query. Default: {"key": "value"}|True|String||
|Return a single JSON result|If enabled, action will return a single JSON result, instead of a few results together, for better and easier usage in Playbooks.|False|Boolean|false|



#### Ping
Test connectivity to MongoDB
Timeout - 600 Seconds









