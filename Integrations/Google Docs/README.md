
# Google Docs

Google Docs is an online word processor that lets you create and format documents and work with other people.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Credentials Json|View the guide on how to create auth json credentials (service account) - provide access for Google Docshttps://gspread.readthedocs.io/en/latest/oauth2.html#enable-api-access|True|String|{}|


#### Dependencies
| |
|-|
|protobuf-6.31.1-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|charset_normalizer-3.4.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|google_auth-2.37.0-py2.py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|google_api_core-2.25.1-py3-none-any.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|googleapis_common_protos-1.70.0-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|google_api_python_client-2.156.0-py2.py3-none-any.whl|
|certifi-2025.6.15-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Remove Content
Removes content from a specific document 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Document Id|The document Id can be found in the URL.For example: https://docs.google.com/document/d/{YourDocumentId}/|True|String|<document_id>|
|Json|The content you want to remove. Most elements in the body have startIndex and endIndex, these indicate the offset of an element's beginning and end.|True|Code|{
  "items": [
    {
      "start_index": 1,
      "end_index": 2
    },
    {
      "start_index": 5,
      "end_index": 7
    }
  ]
}|



#### Replace Content
Replaces specific text in a document 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Document Id|The document Id can be found in the URL.For example: https://docs.google.com/document/d/{YourDocumentId}/|True|String|<document_id>|
|Json|The content in json format you want to replace in the document. |True|Code|{
  "items": [
    {
      "text_to_search": "Hello",
      "text_to_replace": "HELLO",
      "match_case": "true"
    },
    {
      "text_to_search": "World",
      "text_to_replace": "WORLD",
      "match_case": "true"
    }
  ]
}|



#### Create Content
Creates new content in a specific document
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Document Id|The document Id can be found in the URL.For example: https://docs.google.com/document/d/{YourDocumentId}/|True|String|<document_id>|
|Json|The content you want to insert. Most elements in the body have startIndex and endIndex, these indicate the offset of an element's beginning and end.|True|Code|{
  "items": [
    {
      "index": 1,
      "text": "Hello "
    },
    {
      "index": 7,
      "text": "World"
    }
  ]
}|



#### Create Document
Creates a new document and determining who to share the doc with
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Title|The document title of the document you would like to create. |True|String|New Document|
|Role|"Owner"- allows to make any changes to the document"Reader"- allows to open and view the document"Writer"- allows to leave comments in the document|True|List|reader|
|Emails|Email address of the person you would like to add permission to the document. You can add multiple emails by adding ";" as a separator. |True|String|email_1@gmail.com;email_2@gmail.com|



#### Ping
Testing connectivity with Google Docs
Timeout - 600 Seconds










Readme text