
# GoogleCloudStorage

Google Cloud Storage is a flexible cloud storage product with several options for the way you can manage and store your data. It offers globally unified, scalable, and highly durable object storage. This means customers of all sizes and industries can use it to store and protect any amount of data for a range of use cases.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the Google Cloud Storage instance.|False|String|https://storage.googleapis.com|
|Service Account|Specify the full content of the service account JSON file to use in the integration.|False|Password|*****|
|Workload Identity Email|A Service Account Client Email to replace the usage of "Service Account", which will be used for Impersonation. Note that the SOAR Service Account must be granted the "Service Account Token Creator" IAM role on the User Service Account.|False|String||
|Project ID|ID of the project that should be used in Google Cloud Storage integration.|False|String||
|Quota Project ID|ID of your Google Cloud project for Google Cloud API usage and billing. If no value is provided, the project ID defined in your Google Cloud service account is used. For this parameter to work, make sure to grant the "Service Usage Consumer" IAM role to your Google Cloud service account.|False|String||
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Google Cloud Storage service is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|google_api_python_client-2.128.0-py2.py3-none-any.whl|
|google_api_core-2.19.1-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|pycparser-3.0-py3-none-any.whl|
|pyopenssl-26.2.0-py3-none-any.whl|
|cryptography-48.0.0-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|google_cloud_core-2.4.1-py2.py3-none-any.whl|
|protobuf-5.29.6-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|urllib3-2.7.0-py3-none-any.whl|
|pyparsing-3.3.2-py3-none-any.whl|
|google_resumable_media-2.7.2-py2.py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|TIPCommon-1.1.6.1-py2.py3-none-any.whl|
|idna-3.15-py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|google_auth-2.34.0-py2.py3-none-any.whl|
|soupsieve-2.8.3-py3-none-any.whl|
|beautifulsoup4-4.14.3-py3-none-any.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|proto_plus-1.28.0-py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|google_cloud_storage-2.18.2-py2.py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|google-3.0.0-py2.py3-none-any.whl|
|certifi-2026.4.22-py3-none-any.whl|
|google_crc32c-1.8.0-cp311-cp311-manylinux1_x86_64.manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_5_x86_64.whl|
|googleapis_common_protos-1.63.2-py2.py3-none-any.whl|
|pyasn1-0.6.3-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|


## Actions
#### Download an Object From a Bucket
Download an object from a Cloud Storage bucket.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Bucket Name|Specify the name of the bucket in which the object resides.|True|String||
|Object Name|Specify the name of the object in the bucket to download. Please note, for objects which are stored inside folders in the bucket, you should also specify the inner folder. E.g: folder/object_name|True|String||
|Download Path|Specify the absolute path, where to download the file. Example: /folder_1/folder_2|True|String|/{folder_1}/{folder_2}|



##### JSON Results
```json
[{"object_name": "text.txt", "download_path": "/opt/dir/text.txt"}]
```



#### Get a Bucket’s Access Control List
Retrieve the access control list (ACL) for a Cloud Storage bucket.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Bucket Name|Specify name of the bucket from which to retrieve Access Control list.Comma separated names.|True|String||



##### JSON Results
```json
[{"BucketName": "XXX", "BucketACLs": [{"Entity": "project-XXXX-XXXX", "Role": "OWNER"}]}]
```



#### List Bucket Objects
List objects stored in the Cloud Storage bucket.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Bucket Name|Specify name of the bucket from which to retrieve objects.|True|String||
|Max Objects to Return|Specify how many objects to return.|False|String|50|
|Retrieves the Access Control List of an object|If checked, retrieve the Access Control List of an object.|False|Boolean|false|



##### JSON Results
```json
{"Objects": [{"ObjectName": "XXXX.svg", "Bucket": "siemplify-XXX", "ContentType": "image/svg+xml", "TimeCreated": "2021-01-12 09:20:09.870000+00:00", "TimeUpdated": "2021-01-12 09:31:01.969000+00:00", "Size": 2534, "MD5": "XXXX==", "Owner": "", "CR32c": "XXXXX==", "id": "siemplify-XXX/XXX.svg/XXXX", "ObjectACL": [{"Entity": "project-owners-XXXXX", "Role": "OWNER"}]}]}
```



#### List Buckets
Retrieve a list of buckets from Google Cloud Storage.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Results|Maximum number of buckets to return.|False|String|50|
|Project ID|Specify the name of the project, from where you want to retrieve a list of buckets. If nothing is provided, the project will be extracted from integration configuration.|False|String||



##### JSON Results
```json
{"Buckets": [{"CreationDate": ["2020-11-09T12:57:03.981Z"], "ModificationDate": ["2021-01-03T16:20:44.729Z"], "Name": ["siemplify-tip"], "Owner": ""}]}
```



#### Ping
Test connectivity to Google Cloud Storage with parameters provided at the integration configuration page on Marketplace tab.
Timeout - 600 Seconds



#### Remove Public Access From Bucket
Remove the public access from the bucket using Google Cloud Storage.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Resource Name|Specify the name of the bucket on which you want to modify the Access Control List.|True|String||
|Prevent Public Access From Bucket|If enabled, action will also configure the bucket in a way that will prevent possible public access.|False|Boolean|false|



#### Update an ACL entry on Bucket
Updates an ACL entry on the specified bucket.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Bucket Name|Specify the name of the bucket on which you want to modify the Access Control List.|True|String||
|Entity|The entity holding the permission. Can be user-userId, user-emailAddress, group-groupId, group-emailAddress, allUsers, or allAuthenticatedUsers. For more information, please see this reference: https://cloud.google.com/storage/docs/json_api/v1/bucketAccessControls#resource|True|String||
|Role|The access permission for the entity.Possible values: “OWNER”, ”READER”, “WRITER”|True|List||



#### Upload an Object To a Bucket
Upload an object to a Cloud Storage bucket.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Bucket Name|Specify the name of the bucket in which to upload the object.|True|String||
|Source File Path|Specify the absolute path to the file that needs to be uploaded. Example: /loca/path/to/filename|True|String|/{local}/{path_to}/{filename}|
|Object Name|Specify the name of the uploaded object within the bucket.|True|String||



##### JSON Results
```json
[{"object_id": "XXXXXX/myFile/11111", "Object_name": "myFile", "md5_hash": "XXXXXXXX", "object_path": "/dir/myFile"}]
```









