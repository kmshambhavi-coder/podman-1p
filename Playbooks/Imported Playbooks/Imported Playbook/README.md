# Imported Playbook
Imported Playbook



**Enabled:** False

**Version:** 0

**Type:** Playbook

**Priority:** 2

**Playbook Simulator:** False



### Playbook Trigger
**Trigger Type:** All

**Conditions Operator:** And

##### Conditions
|Key|Operator|Value|
|---|--------|-----|
||Equals||



### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|GitSync_Ping_1|Test connectivity to GitSync|GitSync|Ping|
|Siemplify_Change Case Stage_1|Change case stage to handling|Siemplify|Change Case Stage|
|Siemplify_Change Priority_1|Automatically change case priority to the given input|Siemplify|Change Priority|
|Siemplify_Case Comment_1|Add a comment to the case the current alert has been grouped to|Siemplify|Case Comment|
|Siemplify_Change Alert Priority_1|Automatically change the alert priority to the given input. Note: This action is compatible only with Siemplify version 5.6 and higher.|Siemplify|Change Alert Priority|
|Siemplify_Case Tag_1|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|

### Involved Blocks
|Name|Description|
|----|-----------|
|Imported Block|Imported block An embedded workflow that can receive inputs and return an output.|
A paragraph is a distinct section of writing that contains one or more sentences. It serves as a structural building block for organizing ideas, with each paragraph typically focusing on a single, controlling idea or topic