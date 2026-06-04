
# AmazonMacie

Amazon Macie is a powerful security and compliance service that provides an automatic method to detect, identify, and classify data within your AWS account.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|AWS Access Key ID|None|True|String||
|AWS Secret Key|None|True|Password|*****|
|AWS Default Region|None|True|String||


#### Dependencies
| |
|-|
|s3transfer-0.10.2-py3-none-any.whl|
|types_python_dateutil-2.9.0.20240906-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|cryptography-43.0.1-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|arrow-1.3.0-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|botocore-1.35.17-py3-none-any.whl|
|cffi-1.17.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|pycparser-2.22-py3-none-any.whl|
|jmespath-1.0.1-py3-none-any.whl|
|idna-3.8-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|pyOpenSSL-24.2.1-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|boto3-1.35.17-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|


## Actions
#### Enable Macie
Enable Amazon Macie service. Note: Action is not working with Siemplify Entities.
Timeout - 600 Seconds



#### Create Custom Data Identifier
Create Amazon Macie Custom Data Identifier. Note: Action is not working with Siemplify Entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Custom Data Identifier Name|Amazon Macie new custom data identifier name.|True|String||
|Custom Data Identifier Description|Amazon Macie new custom data identifier description.|False|String||
|Custom Data Identifier Regular Expression|Amazon Macie new custom data identifier regular expression, eg I[a@]mAB[a@]dRequest|True|String||
|Custom Data Identifier Keywords|Amazon Macie new custom data identifier keywords.|False|String||
|Custom Data Identifier Ignore Words|Amazon Macie new custom data identifier ignore words.|False|String||
|Custom Data Identifier Maximum Match Distance|Amazon Macie new custom data identifier maximum match distance. Default value is 50.|False|String|50|



#### Get Findings
Get Amazon Macie findings based on specified Finding ID. Note: Action is not working with Siemplify Entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Finding ID|Finding ID to get details for. Parameter can take multiple values as a comma separated string.|True|String||



#### List Findings
List Amazon Macie findings based on the specified action input parameters.  Note: Action is not working with Siemplify entities, only with action input parameters.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Finding Type|Finding type to search for, for example SensitiveData:S3Object/Credentials or SensitiveData:S3Object/Multiple. Parameter accepts multiple values as a comma separated string. If nothing is specified - return all types of findings.|False|String||
|Time Frame|Specify a time frame in hours for which to fetch findings. |False|String|4|
|Severity|Finding severity to search - High, Medium or Low. Parameter accepts multiple values as a comma separated string. If nothing is specified - return all findings regardless of severity.|False|String||
|Include Archived Findings?|Specify whether to include archived findings in results or not.|False|Boolean|false|
|Record Limit|Specify how many records can be returned by the action.|False|String|20|
|Sort By|Specify a parameter for sorting the data, eg updatedAt|False|String||
|Sort Order|Sort order.|False|List|ASC|



#### Delete Custom Data Identifier
Delete Amazon Macie Custom Data Identifier. Note: Action is not working with Siemplify Entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Custom Data Identifier ID|Amazon Macie custom data identifier id to delete.|True|String||



#### Disable Macie
Disable Amazon Macie service. Note: Action is not working with Siemplify Entities.
Timeout - 600 Seconds



#### Ping
Test connectivity to the Amazon Macie service with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds









## Connectors
#### Amazon Macie - Findings Connector
Pull findings from Amazon Macie. Note: Whitelist works with Finding types, for example, SensitiveData:S3Object/Personal.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|AWS Access Key ID|AWS Access Key ID to use in integration.|True|String||
|AWS Secret Key|AWS Secret Key to use in integration.|True|Password|*****|
|AWS Default Region|AWS default region to use in integration, for example us-west-2.|True|String||
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve findings from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max findings to fetch|How many findings to process per one connector iteration.|False|Int|50|
|Finding severity to ingest|Finding severity to ingest - High, Medium or Low. Parameter accepts multiple values as a comma separated string. If nothing is specified - ingest all findings regardless of severity.|False|String||
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




