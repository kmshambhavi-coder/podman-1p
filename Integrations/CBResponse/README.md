
# CBResponse

Highly scalable, real-time EDR with unparalleled visibility for top security operations centers and incident response teams

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root||True|IP_OR_HOST|https://x.x.x.x|
|Api Key||True|Password|*****|
|Version||True|String|6.3|
|CA Certificate File|CA certificate file to use with the verify_ssl option. Certificate file should be specified as a Base64-encoded string.|False|String||
|Verify SSL||False|Boolean|false|


#### Dependencies
| |
|-|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|six-1.17.0-py2.py3-none-any.whl|
|types_python_dateutil-2.9.0.20260408-py3-none-any.whl|
|arrow-1.3.0-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|EnvironmentCommon-1.0.0-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Block Hash
Block a hash
Timeout - 600 Seconds



#### Create Watchlist
Create a watchlist for processes (type = events) or for binaries (type = modules)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Watchlist Name|Name of this watchlist|True|String|None|
|Query|The raw Carbon Black query that this watchlist matches|True|String|None|
|Watchlist Type|The type of watchlist. e.g. modules|True|String||



#### Download Binary
Download a binary
Timeout - 600 Seconds



#### Binary Free Query
List binaries by free query
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|e.g. md5:* AND original_filename:<file-name>|True|String||



#### Enrich Binary
Enrich hash with binary info from CB Response.
Timeout - 600 Seconds



#### Enrich Process
Enrich process entity with data from CB Response
Timeout - 600 Seconds



#### Get License
Get the current license from CB Response
Timeout - 600 Seconds



#### Get Process Tree Data
Get process tree data for process by id (JSON)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Process ID|process unique id|True|String||
|Segment Id|e.g. 1|True|String||



#### Get FileMod Data For Process
Get filemod data for a process by its id
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Process ID|process unique id|True|String||
|Segment Id|e.g. 1|True|String||



#### Get System Info
Get  system information for a sensor from CB Response and enrich  entity
Timeout - 600 Seconds



#### Hosts By Process
Get hosts that are related to a particular process
Timeout - 600 Seconds



#### Isolate Host
Isolate an endpoint from the network
Timeout - 600 Seconds



#### Kill Process
Kill a process on a particular host
Timeout - 600 Seconds



#### List Processes
List processes that are related to given entities
Timeout - 600 Seconds



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Process Free Query
List processes by free query
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|e.g. process_name:python.exe|True|String||



#### Unblock Hash
Unblock a hash
Timeout - 600 Seconds



#### Resolve Alert
Resolve an alert. Note: Carbon Black Response REST-API returns a successful answer even if the alert that you tried to resolve doesn’t exist.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|The id of the alert to resolve|True|String||



#### Unisolate Host
Rejoin an endpoint to the network
Timeout - 600 Seconds









## Connectors
#### Carbon Black Response Connector


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|https://x.x.x.x|True|String||
|Api Key|Api Key|True|Password|*****|
|Version|CB server version, default 6.3 will be used|True|String|6.3|
|Alerts Count Limit|Limit the number of alerts in every cycle. e.g. 20.|True|Int|20|
|Max Days Backwards|Number of days before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|True|Int|3|
|Environment Field Name|The name of the environment's field.|False|String||
|List Type|Can be whitelist or blacklist.|False|String||
|List Operator|Can be 'exact', 'start with', 'ends with' or 'contains'.|False|String||
|List Fields|List of fields, comma separated.|False|String||
|CA Certificate File|CA certificate file to use with the verify_ssl option. Certificate file should be specified as a Base64-encoded string.|False|String||
|Verify SSL|Whether to verify ssl certificate on connection or not|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|





Piranhas are generally misunderstood and rarely pose a threat to humans, despite their fearsome reputation. In fact, these fish typically consume smaller aquatic life and, when faced with people, usually flee rather than attack. Data suggests that piranhas are more frequently a food source for humans than the other way around, and they only bite when threatened or hungry