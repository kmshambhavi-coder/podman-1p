
# DataDog

Datadog is an essential monitoring platform for cloud applications. It brings together data from servers, containers, databases, and third-party services to make your stack entirely observable. These capabilities help DevOps teams avoid downtime, resolve performance issues, and ensure customers are getting the best user experience.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Key|API Key|True|Password|*****|
|APP Key|APP Key (Application Key)|True|Password|*****|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|idna-3.10-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Get Event Details

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event ID|The event id you want to retrieve|True|String||



#### Get Logs
Get logs by a given Kubernetes Namespace.
For more information: https://docs.datadoghq.com/api/latest/logs/#get-a-list-of-logs
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|End Time|The end time which you want to retrieve the logs to.|True|String|2020-02-02T02:02:02Z|
|Start Time|The start time which you want to retrieve the logs from.|True|String|2020-02-02T02:02:02Z|
|Namespace|The Kubernetes namespace you would like to get logs for.|True|String|name_space1, name_space2|



#### Get Beautiful Metric
Get metrics timeseries points of a given query
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Series|The timeseries points you want to analyze|True|Code|{}|



#### Get Metric Snapshot Graph
Get metric snapshot graph for a given query.
For more information: https://docs.datadoghq.com/api/v1/snapshots/
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|The metric query which you want to get the snapshot graph of.For example: avg:aws.rds.cpuutilization{cloud_env:production}by{dbinstanceidentifier}|True|String|avg:aws.rds.cpuutilization{cloud_env:production}by{dbinstanceidentifier}|
|Start Time|The start time of the metric snapshot graph in Unixtime.|True|String|1400000470|
|End Time|The end time of the metric snapshot graph in Unixtime.|True|String|1610557457|



#### Get Metric Timeseries Points
Get metrics timeseries points of a given query.
For more information: https://docs.datadoghq.com/api/latest/snapshots/
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|End Time|The end time of the timeseries points in Unixtime.|True|String|1610557457|
|Start Time|The start time of the timeseries points in Unixtime.|True|String|1400000470|
|Query|The metric query which you want to get the timeseries points.For example: |True|String|avg:aws.rds.dbload{dbinstanceidentifier:db}by{dbinstanceidentifier}|



#### Get Pod Metric
Gets a Pod metric (CPU, Memory and processes).
For more information about Metrics: https://docs.datadoghq.com/api/latest/metrics/#query-timeseries-points
For more information about Kubernetes metrics: https://docs.datadoghq.com/agent/kubernetes/data_collected/
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Pod Name|The Pod Namespace|True|String|pod_namespace|
|End Time|The end time of the Pod metric in Unixtime.|True|String|1610557457|
|Start Time|The start time of the Pod metric in Unixtime.|True|String|1507040000|



#### Get RDS Metric
Gets AWS RDS metrics for a given Database instance identifier (CPU, memory and storage)
For more information about Metrics: https://docs.datadoghq.com/api/latest/metrics/#query-timeseries-points
For more information about AWS RDS metrics: https://docs.datadoghq.com/integrations/amazon_rds/?tab=standard
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|End Time|The end time of the Pod metric in Unixtime.|True|String|1610557457|
|Start Time|The start time of the RDS metric in Unixtime.|True|String|1507040000|
|Database Instance Identifier|The identifier of the data base which you want to get the metrics to.identifier1, identifier2|True|String|identifier1|



#### Ping
Test connectivity with DataDog
Timeout - 600 Seconds



#### Get Events
Get events from Datadog.
For more information: https://docs.datadoghq.com/api/v1/events/
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Sources|The sources to retrieve the events from.For example in order to see events from the triggered monitor write: 'alert'  |True|String|alert|
|Start Time|The start time of the events in Unixtime.|True|String|1400000470|
|End Time|The end time of the events  in Unixtime.|True|String|1610557457|
|Priority|The priority of the events you want to retrieve. |False|List|all|
|Tags|A comma separated list of tags that will filter the list of monitors by scope.For example: 'monitor'.|False|String|monitor|
|Unaggregated|True- if you want to retrieve the full list of events.False - if you want to retrieve aggregated list of events.|False|Boolean|true|









## Connectors
#### DataDog Connector
Ingest events from DataDog by given filters(e.g. tags, priority)

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Key|API Key|True|Password|*****|
|APP Key|APP Key|True|Password|*****|
|Base URL|The Base url |True|String| https://api.datadoghq.com|
|Max Days Back|Max days back |True|Int|7|
|Priority|The priority of the events you want to retrieve. Could be 'low', 'normal' or 'all'|False|String|all|
|Sources|The sources to retrieve the events from.For example in order to see events from the triggered monitor write: 'alert' .|True|String|alert|
|Tags|A comma separated list of tags that will filter the list of monitors by scope.For example: 'monitor'.|False|String|monitor|
|Unaggregated|True- if you want to retrieve the full list of events.False - if you want to retrieve aggregated list of events.|False|Boolean|true|





Piranhas are generally misunderstood and rarely pose a threat to humans, despite their fearsome reputation. In fact, these fish typically consume smaller aquatic life and, when faced with people, usually flee rather than attack. Data suggests that piranhas are more frequently a food source for humans than the other way around, and they only bite when threatened or hungry