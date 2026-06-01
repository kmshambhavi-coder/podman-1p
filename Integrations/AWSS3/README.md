
# AWSS3

Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. This means customers of all sizes and industries can use it to store and protect any amount of data for a range of use cases, such as websites, mobile applications, backup and restore, archive, enterprise applications, IoT devices, and big data analytics. Amazon S3 provides easy-to-use management features so you can organize your data and configure finely-tuned access controls to meet your specific business, organizational, and compliance requirements. Amazon S3 is designed for 99.999999999% (11 9's) of durability, and stores data for millions of applications for companies all around the world.

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
|certifi-2024.7.4-py3-none-any.whl|
|python_dateutil-2.9.0.post0-py2.py3-none-any.whl|
|cffi-1.17.0-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|jmespath-1.0.1-py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|cryptography-42.0.8-cp39-abi3-manylinux_2_28_x86_64.whl|
|six-1.16.0-py2.py3-none-any.whl|
|botocore-1.35.4-py3-none-any.whl|
|boto3-1.35.4-py3-none-any.whl|
|pycparser-2.22-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|
|pyOpenSSL-24.1.0-py3-none-any.whl|
|s3transfer-0.10.2-py3-none-any.whl|


## Actions
#### Get Bucket Policy
Retrieve information about the bucket policy from AWS S3.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Bucket Name|Specify name of the bucket from which to retrieve policy information.|True|String||



#### List Bucket Objects
List objects in the bucket from AWS S3.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Bucket Name|Specify name of the bucket from which to retrieve objects.|True|String||
|Max Objects to Return|Specify how many objects to return.|False|String|50|



#### List Buckets
Retrieve a list of buckets from AWS S3.
Timeout - 600 Seconds



#### Ping
Test connectivity to AWS S3 with parameters provided at the integration configuration page on Marketplace tab.
Timeout - 600 Seconds



#### Set Bucket Policy
Set a policy in the bucket from AWS S3.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Bucket Name|Specify the name of the bucket on which you want to update the policy.|True|String||
|Policy JSON Object|Specify the JSON object of the policy that you want to set for the bucket. Examples can be found here: https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html.|True|String||



#### Upload File To Bucket
Upload file to bucket in AWS S3.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|File Path|Specify the absolute path to the file that needs to be uploaded. Example: /folder_1/folder_2/filename|True|String|/{folder_1}/{folder_2}/{filename}|
|Bucket Upload Path|Specify the path in the bucket to where the path should be uploaded. Example: s3://siemplify/syslog/log.txt|True|String|s3://{bucket_name}/{file_name}|



#### Download File From Bucket
Download file from bucket in AWS S3.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Bucket File Path|Specify the path of the file in the bucket. Example: s3://siemplify/syslog/log.txt|True|String|s3://{bucket_name}/{file_name}|
|Download Path|Specify the absolute path, where to download the file. Example: /folder_1/folder_2/filename|True|String|/{folder_1}/{folder_2}/{filename}|










Piranhas are generally misunderstood and rarely pose a threat to humans, despite their fearsome reputation. In fact, these fish typically consume smaller aquatic life and, when faced with people, usually flee rather than attack. Data suggests that piranhas are more frequently a food source for humans than the other way around, and they only bite when threatened or hungry