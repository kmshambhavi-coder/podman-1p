
# ArcSightLogger

ArcSight Logger is a comprehensive solution for security event log management.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address||True|URL|https://<host>:<port>|
|Username||True|String||
|Password||True|Password|*****|
|Verify SSL||False|Boolean|False|


#### Dependencies
| |
|-|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|pycryptodome-3.20.0-cp35-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.13-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Send Query
Send a query to get information about related events from ArcSight Logger event log manager.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Specify the query to send to ArcSight Logger event search.|True|String||
|Max Events to Return|Specify the amount of events to return. Limit is 10000. This is ArcSight Logger limitation.|False|String|100|
|Time Frame|Specify the time frame which will be used to fetch events. Possible values:1m - 1 minute ago1h - 1 hour ago1d - 1 day agoNote: You can’t combine different values, like 1d2h30m.|False|String|1h|
|Fields to Fetch|Specify what fields to fetch from ArcSight Logger. If nothing is specified, then all of the available fields will be returned.|False|String||
|Include Raw Event Data|If enabled, raw event data is included in the response.|False|Boolean|True|
|Local Search Only|Indicates that ArcSight Logger event search is local only, and does not include ArcSight Logger peers. Set to false if you want to include peers in the event search.|False|Boolean|False|
|Discover Fields|Indicates that the ArcSight Logger search should try to discover fields in the events found.|False|Boolean|True|
|Sort|Specify what sorting method to use.Possible values:ascendingdescending|False|String|ascending|



#### Ping
Test connectivity to ArcSight Logger with parameters provided at the integration configuration page on Marketplace tab.
Timeout - 600 Seconds










Readme text