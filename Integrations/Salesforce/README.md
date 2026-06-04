
# Salesforce

Salesforce is the world's #1 customer relationship management (CRM) platform.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|String|http://www.salesforce.com|
|Username|None|True|String||
|Password|None|True|Password|*****|
|Token|None|True|String||
|Verify SSL|None|False|Boolean|False|


#### Dependencies
| |
|-|
|platformdirs-4.2.0-py3-none-any.whl|
|urllib3-2.2.1-py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|lxml-5.2.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|certifi-2024.2.2-py3-none-any.whl|
|six-1.16.0-py2.py3-none-any.whl|
|requests-2.31.0-py3-none-any.whl|
|attrs-23.2.0-py3-none-any.whl|
|more_itertools-10.2.0-py3-none-any.whl|
|setuptools-70.1.1-py3-none-any.whl|
|pyOpenSSL-24.1.0-py3-none-any.whl|
|requests_toolbelt-1.0.0-py2.py3-none-any.whl|
|zeep-4.2.1-py3-none-any.whl|
|pycparser-2.22-py3-none-any.whl|
|asn1crypto-1.5.1-py2.py3-none-any.whl|
|isodate-0.6.1-py2.py3-none-any.whl|
|cryptography-42.0.5-cp39-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|setuptools-80.9.0-py3-none-any.whl|
|PyPika-0.48.9-py2.py3-none-any.whl|
|typing_extensions-4.11.0-py3-none-any.whl|
|requests_file-2.0.0-py2.py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|PyJWT-2.8.0-py3-none-any.whl|
|simple_salesforce-1.12.6-py2.py3-none-any.whl|
|cffi-1.16.0.tar.gz|
|pytz-2024.1-py2.py3-none-any.whl|


## Actions
#### Get Case
Get case details
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case Number|The number of the case.|True|String|None|



#### List Cases
List all exising cases
Timeout - 600 Seconds



#### Add Comment
Add a comment to a case
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case Number|The number of the case.|True|String|None|
|Title|The comment title|True|String|None|
|Body|The comment's body|True|String|None|



#### Create Case
Create a case
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Subject|The case's subject.|True|String|None|
|Status|The case's status. Valid values: New, On Hold, Closed, Escalated|False|String|None|
|Description|The description of the subject.|False|String|None|
|Origin|The origin of the case. Valid values: Email, Phone, Web|False|String|None|
|Priority|The case's priority. Valid values: Low, Medium, High|False|String|None|
|Type|The case type. Valid values: Question, Problem, Feature Request|False|String|None|



#### Update Case
Update a case
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case Number|The number of the case.|True|String|None|
|Subject|The case's subject|False|String|None|
|Status|The case's status. Valid values: New, On Hold, Closed, Escalated|False|String|None|
|Description|The description of the subject.|False|String|None|
|Origin|The origin of the case. Valid values: Email, Phone, Web|False|String|None|
|Priority|The case's priority. Valid values: Low, Medium, High|False|String|None|
|Type|The case type. Valid values: Question, Problem, Feature Request|False|String|None|



#### Search Records
Search all records that contain values with a given pattern
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Query|Query|True|String|None|



#### Close Case
Close a case
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case Number|The number of the case.|True|String|None|



#### Ping
Test Connectivity
Timeout - 600 Seconds









