
# Fortigate

FortiGate utilize purpose-built security processors and threat intelligence security services from AI-powered FortiGuard labs to deliver top-rated protection, high performance inspection of clear-texted and encrypted traffic. Next-generation firewalls reduce cost and complexity with full visibility into applications, users and networks and provides best of breed security. As an integral part of the Fortinet Security Fabric next-generation firewalls can communicate within Fortinet’s comprehensive security portfolio as well as third-party security solutions in a multivendor environment.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root||True|String|https://{{ip address}}|
|API Key||True|Password|*****|
|Verify SSL||False|Boolean|true|


#### Dependencies
| |
|-|
|certifi-2026.4.22-py3-none-any.whl|
|charset_normalizer-3.4.7-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|requests_file-3.0.1-py2.py3-none-any.whl|
|chardet-7.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|urllib3-2.6.3-py3-none-any.whl|
|tldextract-5.1.2-py3-none-any.whl|
|idna-3.13-py3-none-any.whl|
|filelock-3.29.0-py3-none-any.whl|
|requests-2.32.4-py3-none-any.whl|
|EnvironmentCommon-1.0.0-py3-none-any.whl|
|TIPCommon-1.0.10-py3-none-any.whl|


## Actions
#### Add Entities To Address Group
Add entities to the address group in Fortigate. Supported entities: URL, IP Address. Note: action will extract domain part of URL entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Address Group Name|Specify the name of the address group to which action should add entities.|True|String||



#### Remove Entities From Address Group
Remove entities from the address group in Fortigate. Supported entities: URL, IP Address. Note: action will extract domain part of URL entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Address Group Name|Specify the name of the address group from which action should remove entities.|True|String||



#### Add Entities To Policy
Add entities to policy in Fortigate. Supported entities: URL, IP Address. Note: action will extract domain part of URL entities. 
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|Specify the name of the policy to which action should add entities.|True|String||
|Location|Specify the location for the entities.|False|List|Destination|



#### List Policies
List available policies in Fortigate.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Key|Specify the key that needs to be used to filter policies.|False|List|Select One|
|Filter Logic|Specify what filter logic should be applied. Filtering logic is working based on the value provided in the "Filter Key" parameter.|False|List|Not Specified|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action will try to find the exact match among results and if "Contains" is selected, action will try to find results that contain that substring. If nothing is provided in this parameter, the filter will not be applied. Filtering logic is working based on the value provided in the "Filter Key" parameter.|False|String||
|Max Records To Return|Specify how many records to return. If nothing is provided, action will return 50 records.|False|String|50|



##### JSON Results
```json
[{"policyid": "1xx", "q_origin_key": "1xx", "status": "enable", "name": "Test", "uuid": "5bd6c56a-16e4-51ec-242a-4dxxxxxxxxxx", "uuid-idx": "4xx", "srcintf": [{"name": "lxx.root", "q_origin_key": "lxx.root"}], "dstintf": [{"name": "port", "q_origin_key": "port"}], "action": "deny", "nat64": "disable", "nat46": "disable", "srcaddr": [{"name": "all", "q_origin_key": "all"}], "dstaddr": [{"name": "11:11:11:11:xx:xx", "q_origin_key": "11:11:11:11:xx:xx"}], "srcaddr6": [], "dstaddr6": [], "ztna-status": "disable", "ztna-ems-tag": [], "ztna-geo-tag": [], "internet-service": "disable", "internet-service-name": [], "internet-service-group": [], "internet-service-custom": [], "internet-service-custom-group": [], "internet-service-src": "disable", "internet-service-src-name": [], "internet-service-src-group": [], "internet-service-src-custom": [], "internet-service-src-custom-group": [], "reputation-minimum": 0, "reputation-direction": "destination", "src-vendor-mac": [], "rtp-nat": "disable", "rtp-addr": [], "send-deny-packet": "disable", "firewall-session-dirty": "check-all", "schedule": "always", "schedule-timeout": "disable", "service": [{"name": "ALL", "q_origin_key": "ALL"}], "tos": "0x00", "tos-mask": "0x00", "tos-negate": "disable", "anti-replay": "enable", "tcp-session-without-syn": "disable", "geoip-anycast": "disable", "geoip-match": "physical-location", "dynamic-shaping": "disable", "passive-wan-health-measurement": "disable", "utm-status": "disable", "inspection-mode": "flow", "http-policy-redirect": "disable", "ssh-policy-redirect": "disable", "webproxy-profile": "", "profile-type": "single", "profile-group": "", "profile-protocol-options": "", "ssl-ssh-profile": "", "av-profile": "", "webfilter-profile": "", "dnsfilter-profile": "", "emailfilter-profile": "", "dlp-sensor": "", "file-filter-profile": "", "ips-sensor": "", "application-list": "", "voip-profile": "", "sctp-filter-profile": "", "icap-profile": "", "cifs-profile": "", "videofilter-profile": "", "waf-profile": "", "ssh-filter-profile": "", "logtraffic": "disable", "logtraffic-start": "disable", "capture-packet": "disable", "auto-asic-offload": "enable", "wanopt": "disable", "wanopt-detection": "active", "wanopt-passive-opt": "default", "wanopt-profile": "", "wanopt-peer": "", "webcache": "disable", "webcache-https": "disable", "webproxy-forward-server": "", "traffic-shaper": "", "traffic-shaper-reverse": "", "per-ip-shaper": "", "nat": "disable", "permit-any-host": "disable", "permit-stun-host": "disable", "fixedport": "disable", "ippool": "disable", "poolname": [], "poolname6": [], "session-ttl": "0", "vlan-cos-fwd": 255, "vlan-cos-rev": 255, "inbound": "disable", "outbound": "enable", "natinbound": "disable", "natoutbound": "disable", "wccp": "disable", "ntlm": "disable", "ntlm-guest": "disable", "ntlm-enabled-browsers": [], "fsso-agent-for-ntlm": "", "groups": [], "users": [], "fsso-groups": [], "auth-path": "disable", "disclaimer": "disable", "email-collect": "disable", "vpntunnel": "", "natip": "0.0.0.0 0.0.x.x", "match-vip": "disable", "match-vip-only": "disable", "diffserv-forward": "disable", "diffserv-reverse": "disable", "diffservcode-forward": "000000", "diffservcode-rev": "000000", "tcp-mss-sender": 0, "tcp-mss-receiver": 0, "comments": "", "label": "", "global-label": "", "auth-cert": "", "auth-redirect-addr": "", "redirect-url": "", "identity-based-route": "", "block-notification": "disable", "custom-log-fields": [], "replacemsg-override-group": "", "srcaddr-negate": "disable", "dstaddr-negate": "disable", "service-negate": "disable", "internet-service-negate": "disable", "internet-service-src-negate": "disable", "timeout-send-rst": "disable", "captive-portal-exempt": "disable", "decrypted-traffic-mirror": "", "dsri": "disable", "radius-mac-auth-bypass": "disable", "delay-tcp-npu-session": "disable", "vlan-filter": "", "sgt-check": "disable", "sgt": []}]
```



#### Remove Entities From Policy
Remove entities from the policy in Fortigate. Supported entities: URL, IP Address. Note: action will extract domain part of URL entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Policy Name|Specify the name of the policy from which action should remove entities.|True|String||
|Location|Specify the location for the entities.|False|List|Destination|



#### Ping
Test connectivity to the Fortigate with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### List Address Groups
List available address groups in Fortigate
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Filter Key|Specify the key that needs to be used to filter address groups.|False|List|Select One|
|Filter Logic|Specify what filter logic should be applied. Filtering logic is working based on the value provided in the "Filter Key" parameter.|False|List|Not Specified|
|Filter Value|Specify what value should be used in the filter. If "Equal" is selected, action will try to find the exact match among results and if "Contains" is selected, action will try to find results that contain that substring. If nothing is provided in this parameter, the filter will not be applied. Filtering logic is working based on the value  provided in the "Filter Key" parameter.|False|String||
|Max Records To Return|Specify how many records to return. If nothing is provided, action will return 50 records.|False|String|50|



##### JSON Results
```json
[{"name": "test name", "q_origin_key": "test name", "type": "default", "category": "default", "uuid": "8bf3fcac-1547-51ec-9fcf-fexxxxxxxxxx", "member": [{"name": "10.0.x.x", "q_origin_key": "10.0.x.x"}], "comment": "", "exclude": "disable", "exclude-member": [], "color": 0, "tagging": [], "allow-routing": "disable", "fabric-object": "disable"}, {"name": "Microsoft Office 365", "q_origin_key": "Microsoft Office 365", "type": "default", "category": "default", "uuid": "8bf40256-1547-51ec-2618-72xxxxxxxxxx", "member": [{"name": "login.microsoftonline.com", "q_origin_key": "login.microsoftonline.com"}, {"name": "login.microsoft.com", "q_origin_key": "login.microsoft.com"}, {"name": "login.windows.net", "q_origin_key": "login.windows.net"}], "comment": "", "exclude": "disable", "exclude-member": [], "color": 0, "tagging": [], "allow-routing": "disable", "fabric-object": "disable"}]
```









## Connectors
#### Fortigate - Threat Logs Connector
Pull information about different threat logs from Fortigate. Note: whitelist filter works with "eventtype" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|eventtype|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Root|API root of the Fortigate instance.|True|String|https://{ip}|
|API Key|API key of the Fortigate account.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Fortigate server is valid.|False|Boolean|true|
|Disable Overflow|If enabled, connector will ignore the overflow mechanism.|False|Boolean|true|
|Lowest Security Level To Fetch|Lowest security level that needs to be used to fetch threat logs. Possible values: debug, information, notice, warning, error, critical, alert, emergency. If nothing is specified, the connector will ingest threat logs with all security levels.|False|String|warning|
|Threat Log Location|Location of the threat log.|False|String||
|Threat Subtypes To Fetch|A comma-separated list of threat subtypes to ingest. The possible values are as follows:virus, webfilter, waf, ips, anomaly, app-ctrl, emailfilter, dlp, voip, gtp, dns, ssh, ssl, cifs, file-filter, traffic/local, traffic/forward.|True|String|virus, webfilter, waf, ips, anomaly, file-filter|
|VDOM|The Virtual Domain (VDOM) name to target within the FortiGate device.|False|String||
|Serial Number|The serial number of the FortiGate device.|False|String||
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve threat logs from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Max Alerts To Fetch|How many alerts to process per one connector iteration per subtype. Default: 100.|False|Integer|20|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




