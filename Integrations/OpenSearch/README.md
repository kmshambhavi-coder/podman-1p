
# OpenSearch

Search engine based on Lucene. It provides a distributed, multitenant-capable full-text search engine.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address|None|True|String|http://x.x.x.x:9200|
|Username|None|False|String||
|Password|None|False|Password|*****|
|JWT Token|None|False|Password|*****|
|Authenticate|None|False|Boolean|False|
|Verify SSL|None|False|Boolean|False|
|CA Certificate File|None|False|String||


#### Dependencies
| |
|-|
|six-1.17.0-py2.py3-none-any.whl|
|google_api_python_client-2.174.0-py3-none-any.whl|
|Events-0.5-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|google_api_core-2.25.1-py3-none-any.whl|
|opensearch_dsl-2.1.0-py2.py3-none-any.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|googleapis_common_protos-1.70.0-py3-none-any.whl|
|typing_extensions-4.14.0-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|TIPCommon-2.2.4-py2.py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|google_auth-2.40.3-py2.py3-none-any.whl|
|protobuf-6.31.1-cp39-abi3-manylinux2014_x86_64.whl|
|anyio-4.9.0-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|opensearch_py-3.0.0-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|


## Actions
#### Advanced OS Search
Premade structured OpenSearch query, returns a dict of dictionaries. This action should be used when you want to use time range in the query. If you don’t want to use the time range, use Simple OpenSearch action.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Index|Search pattern for a OpenSearch index.In OpenSearch, index is like a DatabaseName, and data is stored across various indexes.This param defines in what index(es) to search. It can be an exact name ie: "smp_playbooks-2019.06.13"or you can use a (*) wildcard to search by a pattern. e: "smp_playbooks-2019.06*" or "smp*".To learn more about OpenSearch indexes visit https://www.elastic.co/blog/what-is-an-opensearch-index|False|String|*|
|Query|The search query to perform. It is in Lucene syntax.IE1: "*" (this is a wildcard that will return all record)IE1: "level:error"IE2: "level:information"IE3: "level:error OR level:warning"To learn more about lucene syntax, visithttps://www.elastic.co/guide/en/kibana/current/lucene-query.html#lucene-queryhttps://www.elastic.co/guide/en/opensearch/reference/7.1/query-dsl-query-string-query.html#query-string-syntax|False|String|*|
|Limit|Limits the document return count, ie: 10.0 = No limit|False|String|100|
|Display Field|Limits the returned fields. Default "*" = Return all fields.You can state a single field. ie: "level"|False|String|*|
|Search Field|Search field for free text queries (When query doesn't specify a field name).Default is "_all", which means all fields are searched. It is best to use proper lucene syntanx on "_all" fields, or textual search on a specific field.ie1: Search Field = "_all". Query = "level:error" Query will return all records where "level" field, equals "error".ie2: Search Field = "Message", query = "*Login Alarm*". Query will return all records, which their "Message" field, contains the text "Login Alarm"|False|String|_id|
|Timestamp Field|The name of the field to run time-based filtering against. Default is @timestamp. If both Earliest Date and Oldest Date are empty, no time-based filtering will occur.|False|String|@timestamp|
|Oldest Date|Start date of the search. Search will return only records equal or after this point in time.Input may be in exact UTC:	Format: YYYY-MM-DDTHH:MM:SSZ	ie: 2019-06-04T10:00:00ZInput may also be in relative form (using date-math):	ie: "now", "now-1d", "now-1d/d", "now-2h/h"	to learn more about date-math visit https://www.elastic.co/guide/en/opensearch/reference/7.1/common-options.html#date-math|False|String|now-1d|
|Earliest Date|End date of the search. Search will return only records equal or before this point in time.Input may be in exact UTC:	Format: YYYY-MM-DDTHH:MM:SSZ	ie: 2019-06-04T10:00:00ZInput may also be in relative form (using date-math):	ie: "now", "now-1d", "now-1d/d", "now-2h/h"	to learn more about date-math visit https://www.elastic.co/guide/en/opensearch/reference/7.1/common-options.html#date-math|False|String|now|



#### DSL Search
Execute a DSL query in the OpenSearch. This action fetches data from OpenSearch for past 24 hours.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Index|Search pattern for a OpenSearch index.In OpenSearch, index is like a DatabaseName, and data is stored across various indexes.This param defines in what index(es) to search. It can be an exact name ie: "smp_playbooks-2019.06.13"or you can use a (*) wildcard to search by a pattern. e: "smp_playbooks-2019.06*" or "smp*".To learn more about OpenSearch indexes visit https://www.elastic.co/blog/what-is-an-opensearch-index|False|String|*|
|Query|The DSL query to perform. The query must be a valid JSON, or *. For more information, please refer to https://www.elastic.co/guide/en/opensearch/reference/current/query-dsl.html.|False|String|*|
|Limit|Limits the document return count, ie: 10.0 = No limit|False|String|100|



#### Simple OS Search
Searches through everything in OpenSearch and returns back results in a dictionary format. This action supports only queries without time range, if you want to use time range in your query use Advanced OS Search action.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Index|Search pattern for a OpenSearch index.In OpenSearch, index is like a DatabaseName, and data is stored across various indexes.This param defines in what index(es) to search. It can be an exact name ie: "smp_playbooks-2019.06.13"or you can use a (*) wildcard to search by a pattern. e: "smp_playbooks-2019.06*" or "smp*".To learn more about OpenSearch indexes visit https://www.elastic.co/blog/what-is-an-opensearch-index|False|String|*|
|Query|The search query to perform. It is in Lucene syntax.IE1: "*" (this is a wildcard that will return all record)IE1: "level:error"IE2: "level:information"IE3: "level:error OR level:warning"To learn more about lucene syntax, visithttps://www.elastic.co/guide/en/kibana/current/lucene-query.html#lucene-queryhttps://www.elastic.co/guide/en/opensearch/reference/7.1/query-dsl-query-string-query.html#query-string-syntax|False|String|*|
|Limit|Limits the document return count, ie: 10.0 = No limit|False|String|100|



#### Ping
Verifies connectivity to OpenSearch server
Timeout - 600 Seconds









## Connectors
#### OpenSearch DSL Connector
OpenSearch DSL Connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address|The OpenSearch server address, i.e: http://{ip_address}:{port}|True|String||
|Username|OpenSearch username|False|String||
|CA Certificate File|CA Certificate File|False|String||
|Password|OpenSearch password|False|Password|*****|
|JWT Token|OpenSearch JWT Token.|False|Password|*****|
|Authenticate|Whether to authenticate on connection or not|False|Boolean|FALSE|
|Verify SSL|Whether to use ssl on connection or not|False|Boolean|FALSE|
|Alert Field Name|The name of the field where the alert name is located. e.g. _source_info_alertname|True|String||
|Alert Description Field|The name of the field where the description is located. e.g. _source_alert_info_description|False|String||
|Alert Severity|Severity of the alerts. Possible value: Info, Low, Medium, High, Critical. Note: this parameter has priority over “Severity Field Name“. If you want to work with “Severity Field Name“, this field should be left empty.|False|String||
|Severity Field Name|If you want to map severity based on the string value then you would need to create a mapping file. Please refer to documentation portal for more details.|False|String||
|Timestamp Field|The name of the field where the timestamp is located (flat field path). e.g. _source_@timestamp|True|String||
|Environment Field Name|The name of the field where the environment name is stored. If the environment field isn't found, the environment is ''|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is ''.|False|String|.*|
|Index|Index pattern to search by. e.g. '_all'|True|String|_all|
|Query|DSL Query that is used for the search. Note: Valid Json format needed, to make the connector more stable it is recommended to add a sorting timestamp key in the ascending order.|True|String||
|Alerts Count Limit|Max count of alerts to pull in one cycle. e.g. 20|True|Int|20|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|


#### OpenSearch Connector
OpenSearch Connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address|The OpenSearch server address, i.e: http://{ip_address}:{port}|True|String||
|Username|OpenSearch username|False|String||
|CA Certificate File|CA Certificate File|False|String||
|Password|OpenSearch password|False|Password|*****|
|JWT Token|OpenSearch JWT Token.|False|Password|*****|
|Authenticate|Whether to authenticate on connection or not|False|Boolean|FALSE|
|Verify SSL|Whether to use ssl on connection or not|False|Boolean|FALSE|
|Alert Name Field|The name of the field where the alert name is as it appears in the OpenSearch UI. e.g. alert.info.name|True|String||
|Timestamp Field|The name of the field where the timestamp is located as it appears in the OpenSearch UI. e.g. @timestamp|True|String|@timestamp|
|Environment Field|The name of the field where the environment is located is as it appears in the OpenSearch UI. e.g. host.environment|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is ''.|False|String|.*|
|Indexes|Index pattern to search by. e.g. '*'|True|String|*|
|Query|Search pattern query (Lucene query syntax). e.g. '*'|True|String|*|
|Alerts Count Limit|Max count of alerts to pull in one cycle. e.g. 20|True|Int|20|
|Max Days Backwards|Max number of days to fetch alerts since. e.g. 3|True|Int|1|
|Severity Field Name|If you want to map severity based on the string value then you would need to create a mapping file. Please refer to documentation portal for more details.|False|String||
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




