
# SentinelOne

Endpoint security software that defends every endpoint against every type of attack, at every stage in the threat lifecycle.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|URL|https://{server}.sentinelone.net/|
|Username|None|True|String||
|Password|None|True|Password|*****|



## Actions
#### Get Process List For Endpoint
Get process list by an endpoint
Timeout - 600 Seconds



#### Get Hash Reputation
Get hash reputation by SHA1
Timeout - 600 Seconds



#### Disconnect Agent From Network
Disconnect agent from network connection
Timeout - 600 Seconds



#### Get System Status
Get SentinelOne system health status
Timeout - 600 Seconds



#### Initiate Full Scan
Initiate full disk scan on an endpoint
Timeout - 600 Seconds



#### Update Exclusion List Add Path 
Add a path to an existing exclusion list (Note - OS can be: Windows, OSX, Linux or Android)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|List Name|Exclusion list name.|True|String|None|
|Path|Path to add to the list.|True|String|None|
|Operation System|Operation system, can be: windows, osx, linux or android.|True|String|None|



#### Get Agent Status
Get agent's current status (active/inactive)
Timeout - 600 Seconds



#### Reconnect Agent To The Network
Reconnect a disconnected agent to the network
Timeout - 600 Seconds



#### Get Events For Endpoint By Time
Get all events related to an endpoint
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Hours Back|How match time back fetch events from.|True|String|None|
|Events Amount Limit|Events amount limit.|True|String|None|



#### Get System Version
Get SentinelOne system version
Timeout - 600 Seconds



#### Enrich Endpoint
Enrich endpoint entity with its system information
Timeout - 600 Seconds



#### Get Application List For Endpoint
Get a list of applications by endpoint (host or IP address)
Timeout - 600 Seconds



#### Ping
Test Connectivity
Timeout - 600 Seconds









