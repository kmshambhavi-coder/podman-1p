
# BitSight

BitSight offers the world's leading security ratings solution with a mission to change the way the world manages cybersecurity analytics and risk.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the BitSight instance.|True|String|https://api.bitsighttech.com|
|API Key|API Key of the BitSight instance.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the BitSight is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|certifi-2024.7.4-py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|


## Actions
#### Ping
Test connectivity to the BitSight with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### List Company Highlights
List highlights related to the company in BitSight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Company Name|Specify the name of the company for which you want to return highlights.|True|String||
|Time Frame|Specify a time frame for the results. If "Custom" is selected, you also need to provide the "Start Time" parameter.|False|List|Last Month|
|Start Time|Specify the start time for the results. This parameter is mandatory, if "Custom" is selected for the "Time Frame" parameter. Format: ISO 8601|False|String||
|End Time|Specify the end time for the results. Format: ISO 8601. If nothing is provided and "Custom" is selected for the "Time Frame" parameter then this parameter uses current time.|False|String||
|Max Highlights To Return|Specify the number of  highlights you want to return. Default: 20.|False|String|20|



#### Get Company Details
Get information about a company in BitSight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Company Name|Specify the name of the company for which you want to return details.|True|String||



#### List Company Vulnerabilities
List vulnerabilities related to the company in BitSight.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Company Name|Specify the name of the company for which you want to return vulnerabilities.|True|String||
|Only High Confidence|If enabled, action will only return vulnerabilities with high confidence.|False|Boolean|true|
|Max Vulnerabilities To Return|Specify how many vulnerabilities you want to return. Default: 50.|False|String|50|









## Connectors
#### BitSight - Alerts Connector
Pull information about alerts from BitSight. Note: dynamic list filter works with "trigger" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of the BitSight instance.|True|String|https://api.bitsighttech.com|
|API Key|API Key of the BitSight account. |True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the BitSight server is valid.|False|Boolean|true|
|Lowest Severity To Fetch|Lowest severity that needs to be used to fetch alerts. Possible values: Informational, Increase, Warn, Critical. If nothing is specified, the connector will ingest alerts with all severities.|False|String|WARN|
|Max Days Backwards|Number of days before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Alerts To Fetch|Specify the number of alerts to process per one connector iteration. Default: 20.|False|Int|20|
|Use dynamic list as a blacklist|If enabled, dynamic lists will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|





Piranhas are generally misunderstood and rarely pose a threat to humans, despite their fearsome reputation. In fact, these fish typically consume smaller aquatic life and, when faced with people, usually flee rather than attack. Data suggests that piranhas are more frequently a food source for humans than the other way around, and they only bite when threatened or hungry