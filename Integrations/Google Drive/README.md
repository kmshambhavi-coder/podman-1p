
# Google Drive

Google Drive is a cloud-based storage solution that allows you to save files online and access them anywhere from any smartphone, tablet, or computer. You can use Drive on your computer or mobile device to securely upload files and edit them online. Drive also makes it easy for others to edit and collaborate on files.

Python Version - V3_11
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Credentials Json|View the guide on how to create auth json credentials (service account) - provide access for Google Drivehttps://gspread.readthedocs.io/en/latest/oauth2.html#enable-api-access|True|Password|*****|


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
#### Download File To Base64
Downloads a file stored in Google Drive as Base64 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Id|The file Id is presented in the file URL. See example - https://drive.google.com/drive/u/0/folders/{file-id}|True|String|<file_id>|



#### Remove Permission
Removes permission for a specific file stored in Google Drive
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Id|The file Id is presented in the file URL. See example - https://drive.google.com/drive/u/0/folders/{file-id}|True|String|<file_id>|
|Permission Id|The permission Id can be retrieved using the permission list action|True|String|<permission_id>|



#### Permission List
Retrieves the list of users that have permission for a specific file stored in Google Drive
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Id|The file Id is presented in the file URL. See example - https://drive.google.com/drive/u/0/folders/{file-id}|True|String|<file_id>|



#### Delete File
Delete a specific file stored in Google Drive
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Id|The file Id is presented in the file URL. See example - https://drive.google.com/drive/u/0/folders/{file-id}|True|String|<file_id>|



#### Download File To Path
Downloads a file stored in Google Drive to a specific path 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Id|The file Id is presented in the file URL. See example - https://drive.google.com/drive/u/0/folders/{file-id}|True|String|<file_id>|
|Folder Path|The folder path chosen to save the file you want to download from Google Drive. |False|String|/temp|



#### Upload File From Path
Uploads a file from a specific path to Google Drive
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Path|The file path from which the file will be uploaded to Google Drive|True|String|/temp/image.png|
|Share with emails|Email address of the person you would like to add permission to the file. You can add multiple emails by adding ";" as a separator. |True|String|email1@gmail.com;email2@gmail.com|



#### Add Permission
 Adds permission for a specific file stored in Google Drive 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Id|The file Id is presented in the file URL. See example - https://drive.google.com/drive/u/0/folders/{file-id}|True|String|<file_id>|
|Role|"Owner"- allows to make any changes to the document"Reader"- allows to open and view the document"Writer"- allows to leave comments in the document|True|List|reader|
|Emails|Email address of the person you would like to add permission to the file. You can add multiple emails by adding ";" as a separator. |True|String|email_1@gmail.com;email_2@gmail.com|
|Should send notification|Define if you would like to send a notification to the user. |False|Boolean|true|



#### Get File Metadata
Retrieves the file Metadata
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Id|The file Id is presented in the file URL. See example - https://drive.google.com/drive/u/0/folders/{file-id}|True|String|<file_id>|



#### Upload File From Base64
Uploads a Base64 to Google Drive
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Name|The file name you would like to upload in Base64 format.|True|String|example.txt|
|Share with emails|Email address of the person you would like to add permission to the file. You can add multiple emails by adding ";" as a separator. |True|String|email1@gmail.com;email2@gmail.com|
|Base64 String|The file Base64 String|True|String|SGVsbG8sIFdvcmxkIQ==|



#### Ping
Check Connectivity with Google Drive
Timeout - 600 Seconds









