# Google Workspace Starting Playbook
Google Workspace Starting Playbook provides reference implementation of how Google Workspace alerts can be processed in Google SecOps.



**Enabled:** False

**Version:** 0

**Type:** Playbook

**Priority:** 3

**Playbook Simulator:** False



### Playbook Trigger
**Trigger Type:** Custom Trigger

**Conditions Operator:** And

##### Conditions
|Key|Operator|Value|
|---|--------|-----|
|[Event.event_metadata_logType]|Equals|WORKSPACE_ACTIVITY|



### Involved Steps (Unordered)
|Step Name|Description|Integration|Original Action|
|---------|-----------|-----------|---------------|
|Get Detection Details|Fetch information about a detection in Google Chronicle.|GoogleChronicle|Get Detection Details|
|Close Alert|Closes the current alert|Siemplify|Close Alert|
|Google Workspace Tag|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|
|SUMMARY_DATA|Action sets a value for a key specified that is stored in the Siemplify database. Available scopes to get context values for: Alert, Case, Global. Action is not working on Siemplify entities. Note: Key Name parameter is case insensitive.|Siemplify|Set Scope Context Value|
|Google Tag|Add given tag to the case the current alert is grouped to|Siemplify|Case Tag|

### Involved Blocks
|Name|Description|
|----|-----------|
|Set Initial Severity|This block sets the initial alert score based on the SIEM detection severity or the rule metadata severity label.|
|Google SecOps Enrichment|This block retrieves relevant details about users and assets involved in the case, enhancing the context available for analysis and subsequent actions within Google SecOps SOAR.|
|Google Workspace Enrichment|This block enriches user entities with relevant information from Google Workspace, providing additional context to support investigation and response activities.|
|Google Workspace Containment|This block allows the playbook to update Google Workspace Directory user accounts as part of containment or response actions, supporting account management and security controls.|
|MITRE Enrichment|This block retrieves detailed information about MITRE ATT&CK techniques and their associated mitigations, providing valuable context to understand adversary behaviors and possible defensive actions.|
|Alert Priority|This block sets the alert priority using a previously defined playbook variable, ensuring consistent prioritization logic for the case workflow.|
|GTI Enrichment|This block enhances case entities with Google Threat Intelligence enrichment information. Works for IPs, URLs, hostnames, domains, hashes (MD5, SHA-1, SHA-256), threat actors, and CVEs.|
A paragraph is a distinct section of writing that contains one or more sentences. It serves as a structural building block for organizing ideas, with each paragraph typically focusing on a single, controlling idea or topic