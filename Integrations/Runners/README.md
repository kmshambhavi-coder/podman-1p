
# Runners

Run commands as different users. Permission to replace a process level token is required (in local policies)

Python Version - 3



## Actions
#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Run Command As User
Run a command as a user (Windows only)
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Command|The command to run, e.g: whoami|True|String||
|Username|Username|True|String||
|Domain|User's domain.|True|String||
|Password|Password|True|Password|*****|
|Daemon|Whether to run in the background or not|False|Boolean|true|









