# Simple Playbook
Simple playbook



**Enabled:** True

**Version:** 1

**Type:** Playbook

**Priority:** 1

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
|Siemplify_Add General Insight_1|Add a general insight configurable message to the case|Siemplify|Add General Insight|
|Siemplify_Case Comment_1|Add a comment to the case the current alert has been grouped to|Siemplify|Case Comment|
|Siemplify_Case Tag_1|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|Siemplify_Remove Tag_1|Remove tags from a case.|Siemplify|Remove Tag|
|Siemplify_Add Entity Insight_1|Add an insight configurable message to each targeted entity|Siemplify|Add Entity Insight|

