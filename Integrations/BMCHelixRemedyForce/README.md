
# BMCHelixRemedyForce

BMC Helix Remedyforce is comprehensive IT service management that easily scales and adapts to the needs of mid-size companies. Built on Salesforce cloud, it allows you to seamlessly combine IT operations management (ITOM) and cognitive capabilities to ensure the business is efficient, compliant, and secure.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|None|True|URL|https://{{your instance}}.my.salesforce.com|
|Login API Root|None|True|URL|https://login.salesforce.com|
|Username|None|False|String||
|Password|None|False|Password|*****|
|Client ID|None|False|String||
|Client Secret|None|False|Password|*****|
|Refresh Token|None|False|Password|*****|
|Verify SSL|None|False|Boolean|true|


#### Dependencies
| |
|-|
|my_test_package-0.1.1.tar.gz|
|idna-3.8-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|xmltodict-0.13.0-py2.py3-none-any.whl|
|soupsieve-2.6-py3-none-any.whl|
|filelock-3.16.0-py3-none-any.whl|
|lxml-5.3.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|PyPika-0.48.9.tar.gz|
|beautifulsoup4-4.12.3-py3-none-any.whl|
|setuptools-74.1.2-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|tldextract-5.1.2-py3-none-any.whl|
|netaddr-1.3.0-py3-none-any.whl|
|setuptools-80.9.0-py3-none-any.whl|
|certifi-2024.8.30-py3-none-any.whl|
|requests_file-2.1.0-py2.py3-none-any.whl|


## Actions
#### Delete Record
Delete a record in BMC Helix Remedyforce.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record that needs to be deleted. If you don't know what kind of records are available, please execute action "List Record Types".|True|String||
|Record ID|Specify the id of the record that needs to be deleted.|True|String||



#### Get OAuth Refresh Token
Generate the refresh token that is needed for the integration configuration. Authorization code can be generated using "Get OAuth Authorization Code". Please refer to the documentation portal for more information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Redirect URL|Specify the redirect URL that was used when the "Connector App" was created.|True|String|https://localhost|
|Authorization Code|Specify the authorization code from action "Get OAuth Authorization Code".|True|String||



#### List Record Types
List available record types from BMC Helix Remedyforce. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action will try to find the exact match among record types and if "Contains" is selected, action will try to find record types that contain that substring. If nothing is provided in this parameter, the filter will not be applied.|False|String||
|Max Record Types To Return|Specify how many record types to return. Default: 50.|False|String|50|
|Filter Logic|Specify what filter logic should be applied.|False|List|Equal|



#### Ping
Test connectivity to the BMC Helix Remedyforce with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Get OAuth Authorization Code
Generate an OAuth authorization code in BMC Helix Remedyforce. Please refer to the documentation portal for more information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Redirect URL|Specify the redirect URL that was used when the "Connector App" was created.|True|String|https://localhost|



#### Update Record
Update record in BMC Helix Remedyforce.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record that needs to be updated. If you don't know what kind of records are available, please execute action "List Record Types".|True|String||
|Record ID|Specify the id of the record that needs to be updated.|True|String||
|Fields To Update|Specify a JSON object containing all of the needed fields and  values that need to be updated.|True|String|{"field":"value"}|



#### Wait For Fields Update
Wait for fields update in BMC Helix Remedyforce.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record for which you are waiting an update. If you don't know what kind of records are available, please execute action "List Record Types".|True|String||
|Record ID|Specify the ID of the record that needs to be updated.|True|String||
|Fields To Check|Specify a JSON object containing all of the needed fields and  values.|True|String|{"field":"value"}|
|Fail If Timeout|If enabled, action will be failed, if not all of the fields were updated.|False|Boolean|true|



#### Create Record
Create a record in BMC Helix Remedyforce.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record that needs to be created. If you don't know what kind of records are available, please execute action "List Record Types".|True|String||
|Record Payload|Specify a JSON object containing all of the needed fields and values.|True|String||



#### Execute Simple Query
Execute a SOQL query based on parameters in BMC Helix Remedyforce.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify what record type should be queried.|True|String||
|Where Filter|Specify the WHERE filter for the query  that needs to be executed. Note: you don't need to provide time filter, limiting and sorting. Also, you don't need to provide WHERE string in the payload.|False|String||
|Time Frame|Specify a time frame for the results. If "Custom" is selected, you also need to provide "Start Time".|False|List|Last Hour|
|Start Time|Specify the start time for the results. This parameter is mandatory, if "Custom" is selected for the "Time Frame" parameter. Format: ISO 8601|False|String||
|End Time|Specify the end time for the results. Format: ISO 8601. If nothing is provided and "Custom" is selected for the "Time Frame" parameter then this parameter will use current time.|False|String||
|Fields To Return|Specify what fields to return. If nothing is provided action will return all fields.|False|String||
|Sort Field|Specify what parameter should be used for sorting.|False|String|CreatedDate|
|Max Results To Return|Specify how many results to return. Default: 50. Maximum is 200.|False|String|50|
|Sort Order|Specify the order of sorting.|False|List|ASC|



#### Execute Custom Query
Execute a custom SOQL query in BMC Helix Remedyforce. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|SOQL Query|Specify what query should be executed.|True|String||



#### Get Record Details
Get detailed information about the record from BMC Helix Remedyforce. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Record Type|Specify the type of the record for which you want to retrieve details. If you don't know what kind of records are available, please execute action "List Record Types".|True|String||
|Record IDs|Specify the ids of records for which you want to return details.|True|String||
|Fields To Return|Specify what fields to return. If none of the provided fields were found, action will fail. If nothing is provided, action will return all fields. |False|String||









## Connectors
#### BMC Helix Remedyforce - Incidents Connector
Pull information about incidents from BMC Helix Remedyforce.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|API Root|API root of the BMC Helix Remedyforce instance.|True|String|https://{{your instance}}.my.salesforce.com|
|Login API Root|API root that is used to authenticate in BMC Helix Remedyforce.|True|String|https://login.salesforce.com|
|Username|BMC Helix Remedyforce username.|False|String||
|Password|BMC Helix Remedyforce password.|False|Password|*****|
|Client ID|BMC Helix Remedyforce client ID of the connected app. This parameter is needed for OAuth authentication. Note: this parameter has priority over Username + Password authentication.|False|String||
|Client Secret|BMC Helix Remedyforce client secret of the connected app. This parameter is needed for OAuth authentication. Note: this parameter has priority over Username + Password authentication.|False|Password|*****|
|Refresh Token|Refresh token for the OAuth authorization.|False|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the BMC Helix Remedyforce server is valid.|False|Boolean|true|
|Lowest Priority To Fetch|Lowest priority that will be used to fetch incidents. Maximum: 5. Minimum: 1. If nothing is provided, the connector will ingest all incidents.|False|Int|5|
|Ingest Empty Priority Incidents|If enabled, the connector will fetch incidents that don't have priority. Siemplify Alerts created in this manner will have priority set to "Informational".|False|Boolean|true|
|Type Filter|Type filter for the incidents. If nothing is provided, the connector will ingest all incidents. Example: Incident, Service Request.|False|String|Incident,Service Request|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Int|1|
|Max Incidents To Fetch|How many incidents to process per one connector iteration. Maximum is 200.|False|Int|10|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|





Piranhas are generally misunderstood and rarely pose a threat to humans, despite their fearsome reputation. In fact, these fish typically consume smaller aquatic life and, when faced with people, usually flee rather than attack. Data suggests that piranhas are more frequently a food source for humans than the other way around, and they only bite when threatened or hungry