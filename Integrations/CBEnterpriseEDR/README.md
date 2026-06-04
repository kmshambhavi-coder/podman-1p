
# CBEnterpriseEDR

The VMware Carbon Black Enterprise EDR is an advanced threat hunting and incident response solution delivering continuous visibility for top security operations centers (SOCs) and incident response (IR) teams. Enterprise EDR is delivered through the VMware Carbon Black Cloud, a next-generation endpoint protection platform that consolidates security in the cloud using a single agent, console and dataset.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String||
|Organization Key||True|String||
|API ID||True|Password|*****|
|API Secret Key||True|Password|*****|
|Verify SSL||False|Boolean||


#### Dependencies
| |
|-|
|six-1.17.0-py2.py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|arrow-1.3.0-py3-none-any.whl|
|types_python_dateutil-2.9.0.20260408-py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|


## Actions
#### Enrich Hash
Enrich Siemplify File hash entity based on the information from the VMware Carbon Black Enterprise EDR. Note: Action accepts file hashes only in SHA256 format!
Timeout - 600 Seconds



#### Process Search
Search information about process activity on the host with CB sensor based on the provided search parameters. The action accepts Host Siemplify entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Query to execute in process search. For example, process_name:svchost.exe - to search based by process name, process_hash:9520a99e77d6196d0d09833146424113 - to search based by process hash.|False|String||
|Time Frame|Specify a time frame in hours for which to fetch alerts.|False|String|4|
|Record limit|Specify how many records can be returned by the action.|True|String|20|
|Sort By|Specify a parameter for sorting the data.|False|String||
|Sort Order|Sort order.|False|List|ASC|



#### Get Events Associated With Process by Process Guid
Get events associated with specific processes based on the information from the VMware Carbon Black Enterprise EDR. This action can get more detailed results on specific process activity than “Process Search” action. Note for the action to work, Siemplify process artifact passed to action should be a process guid type.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Process GUID|Specify a process guid to search events for.|True|String||
|Search Criteria|Specify a search criteria for the request. Currently, only “event_type” values are accepted as the search criteria, for example, netconn. Multiple values are accepted as a comma separated string.|False|String||
|Query|Query to execute in process search.For example, “netconn_action:ACTION_CONNECTION_CREATE OR netconn_action:ACTION_CONNECTION_ESTABLISHED”|True|String||
|Time Frame|Specify a time frame in hours for which to fetch events.|False|String|4|
|Record limit|Specify how many records can be returned by the action.|True|String|20|
|Sort By|Specify a parameter for sorting the data.|False|String||
|Sort Order|Sort order.|False|List|ASC|



#### Ping
Test connectivity to the VMware Carbon Black Enterprise EDR with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds










Readme text