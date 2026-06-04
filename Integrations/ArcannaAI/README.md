
# ArcannaAI

Arcanna.ai is a platform for delivering decision intelligence. It augments Security Operation Center analysts in dealing with incoming threats by increasing analyst efficiency in decision-making.

Arcanna.ai continuously learns from cybersecurity experts by using an innovative method for expert knowledge integration into deep neural nets by combining a continuous human feedback-loop, Natural Language Processing and deep learning.

Our platform enables SOC Analyst decisions to be augmented using AI models obtained by encoding knowledge from the existing processes across the entire security team and uses it to predict future decisions, increasing efficiency in decision-making.

More information is available at https://arcanna.ai


Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Url||True|String|https://your-arcanna.url|
|Api Key||True|Password|*****|
|SSL Verification||False|Boolean|false|


#### Dependencies
| |
|-|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Send JSON Document to Arcanna

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|Job ID used for sending event to Arcanna.ai|True|String| |
|Identifier field|Identifier field that will be used as an ID in Arcanna.ai when ingesting the document. The field supports dot notation field names such as 'doc.id'.|False|String||
|Use document ID as ID in Arcanna|If False, Arcanna generates a new unique ID for the document.If True, Arcanna uses the id found in the "Identifier field".|False|Boolean|false|
|JSON Document|The JSON document to be sent to Arcanna.|True|Code|{}|



#### Send event to Arcanna

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|Job ID used for sending event to Arcanna.ai|True|String| |
|Username|Username registered for audit purposes|True|User_Repository|@Administrator|
|Event ID mapping field|Field that will be used as reference ID with Arcanna.ai|False|String|None|
|Send individual alerts from case|Send individual alerts or full case to Arcanna.ai|False|Boolean|false|



#### Trigger AI Model training

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|ID For job where training will be triggered|True|String||
|Username|Username for audit|True|User_Repository|@Administrator|



#### Get AI Job decision set

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|Job ID for which decision set should be fetched |True|String| |



#### Export full event

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|Where to fetch event|True|String| |
|Event ID|Event ID To fetch|True|String| |



#### Get AI Job decision set by job name

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job name|Job name for which decision set should be fetched |True|String| |



#### Send Active Alert from Case to Arcanna

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job ID|Job ID used for sending event to Arcanna.ai|True|String| |
|Alert identifier field|Identifier field that will be used as an ID in Arcanna.ai when ingesting the alert. Default value for Google SecOps Alerts is "identifier".|False|String|identifier|
|Use Alert ID as ID in Arcanna|If False, Arcanna generates a new unique ID for the alert.If True, Arcanna uses the id found in the "Alert identifier field".|False|Boolean|false|



#### Get Arcanna decision

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job Id|Arcanna Job id|True|String||
|Event Id|Arcanna Event ID|True|String||
|Retry count|How many times request should be re-tried|True|String|20|
|Seconds per retry|How many seconds should wait between requests|True|String|5|



#### Send Case to Arcanna

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case identifier field|Identifier field that will be used as an ID in Arcanna.ai when ingesting the case. Default value for Google SecOps Cases is "identifier".|False|String|identifier|
|Use case ID as ID in Arcanna|If False, Arcanna generates a new unique ID for the case.If True, Arcanna uses the id found in the "Case identifier field".|False|Boolean|false|
|Job ID|Job ID used for sending event to Arcanna.ai|True|String| |



#### Get AI Job by name

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Job name|Job name for which the job details should be fetched |True|String| |



#### Update alert priority
Change the alert priority based on the input.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Priority|Choose the new priority. Must be one the following values:- Informative- Low- Medium- High- Critical|True|String|[ArcannaAI_Get Arcanna decision_1.JsonResult| "result_label"]|



#### Get Jobs
Retrieves Arcanna.AI available jobs  and saves the results
Timeout - 600 Seconds



#### Send Analyst Feedback to Arcanna

Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event Id|Arcanna Event id|True|String||
|Username|Analyst name who uses this action|True|User_Repository|Admin|
|Job Id|Arcanna Job Id|True|String||
|Analyst Feedback|A string representing the feedback an analyst provides on an event.|True|String|_|



#### Ping

Timeout - 600 Seconds










Readme text