
# APIVoid

Database of API services mostly focused on threat analysis and threat intelligence, that can be easily integrated anywhere.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Root|None|True|String|https://endpoint.apivoid.com|
|Api Key|None|True|Password|*****|
|Verify SSL|None|False|Boolean|False|


#### Dependencies
| |
|-|
|TIPCommon-1.0.11-py2.py3-none-any.whl|
|idna-3.7-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|requests-2.31.0-py3-none-any.whl|
|certifi-2024.2.2-py3-none-any.whl|
|urllib3-2.2.1-py3-none-any.whl|


## Actions
#### Get Screenshot
Capture a high-quality screenshot of any website or URL
Timeout - 600 Seconds



##### JSON Results
```json
[{"EntityResult": {"file_md5_hash": "6ea33856a409c9bf9d1fcad8ce047065"}, "Entity": "www.google.co.il"}, {"EntityResult": {"file_md5_hash": "221f08045ab2b242a92da15de8812857"}, "Entity": "https://google.com"}]
```



#### Get Ip Reputation
Detect potentially malicious IP addresses commonly used for spam, to attack websites or to commit fraudulent activities
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|IP risk threshold. The threshold must be a numeric value. e.g. 3|True|String|0|
|Create Insights|Specify whether the action should create insights or not.|False|Boolean|true|



##### JSON Results
```json
[{"EntityResult": {"information": {"is_proxy": false, "is_vpn": false, "region_name": "Zhejiang", "is_webproxy": false, "latitude": 28.680280685424805, "isp": "ChinaNet Zhejiang Province Network", "continent_code": "AS", "is_tor": false, "reverse_dns": "", "detections": 18, "engines_count": 76, "longitude": 121.44277954101562, "city_name": "Jiaojiang", "country_name": "China", "continent_name": "Asia", "detection_rate": "24%", "country_code": "CN", "is_hosting": false}, "blacklists": {"scantime": "0.57", "detection_rate": "24%", "detections": 18, "engines_count": 76, "engines": [{"engine": "PlonkatronixBL", "detected": false, "reference": "http://bl.plonkatronix.com/"}, {"engine": "Peter-s NUUG IP BL", "detected": true, "reference": "https://home.nuug.no/~peter/"}, {"engine": "Malc0de", "detected": false, "reference": "http://malc0de.com/database/index.php"}]}, "anonymity": {"is_tor": false, "is_proxy": false, "is_vpn": false, "is_webproxy": false, "is_hosting": false}, "ip": "1.1.1.1"}, "Entity": "1.1.1.1"}]
```



#### Get URL Reputation
Get safety reputation and risk score of an URL
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|URL risk threshold. The threshold must be a numeric value. e.g. 3|True|String|0|



##### JSON Results
```json
[{"EntityResult": {"domain_blacklist": {"detections": 0, "engines": [{"detected": false, "name": "SpamhausDBL", "reference": "https://www.spamhaus.org/lookup/"}, {"detected": false, "name": "ThreatLog", "reference": "http://www.threatlog.com/"}, {"detected": false, "name": "OpenPhish", "reference": "http://www.openphish.com/"}, {"detected": false, "name": "PhishTank", "reference": "http://www.phishtank.com/"}, {"detected": false, "name": "Phishing.Database", "reference": "https://github.com/mitchellkrogza/Phishing.Database"}, {"detected": false, "name": "PhishStats", "reference": "https://phishstats.info/"}, {"detected": false, "name": "URLVir", "reference": "http://www.urlvir.com/"}, {"detected": false, "name": "URLhaus", "reference": "https://urlhaus.abuse.ch/"}, {"detected": false, "name": "RPiList Not Serious", "reference": "https://github.com/RPiList/specials"}, {"detected": false, "name": "precisionsec", "reference": "https://precisionsec.com/"}, {"detected": false, "name": "AntiSocial Blacklist", "reference": "https://theantisocialengineer.com/"}, {"detected": false, "name": "PhishFeed", "reference": "https://phishfeed.com/"}, {"detected": false, "name": "Spam404", "reference": "https://www.spam404.com/"}]}, "html_forms": {"number_of_total_input_fields": 0, "email_field_present": false, "number_of_total_forms": 0, "password_field_present": false, "two_text_inputs_in_a_form": false, "credit_card_field_present": false}, "server_details": {"continent_name": "Asia", "hostname": "mfwd12.mailplug.co.kr", "region_name": "Seoul-teukbyeolsi", "ip": "14.49.36.141", "isp": "KT Corporation", "continent_code": "AS", "country_name": "Korea (Republic of)", "city_name": "Seoul", "longitude": 126.97782897949219, "country_code": "KR", "latitude": 37.568260192871094}, "response_headers": {"status": "HTTP/1.1 404 Not Found", "content-length": "177", "code": 404, "server": "nginx/1.4.6 (Ubuntu)", "connection": "keep-alive", "date": "Wed, 15 Jul 2020 08:21:54 GMT", "content-type": "text/html"}, "redirection": {"url": null, "found": false, "external": false}, "file_type": {"headers": "HTML", "extension": "HTML", "signature": ""}, "risk_score": {"result": 10}, "security_checks": {"is_suspended_page": false, "is_defaced_heuristic": false, "is_windows_exe_file": false, "is_credit_card_field": false, "is_windows_exe_file_on_free_hosting": false, "is_masked_linux_elf_file": false, "is_exe_on_directory_listing": false, "is_php_on_directory_listing": false, "is_masked_windows_exe_file": false, "is_sinkholed_domain": false, "is_robots_noindex": false, "is_windows_exe_file_on_free_dynamic_dns": false, "is_doc_on_directory_listing": false, "is_non_standard_port": false, "is_linux_elf_file_on_free_dynamic_dns": false, "is_suspicious_domain": false, "is_suspicious_url_pattern": false, "is_china_country": false, "is_risky_geo_location": false, "is_pdf_on_directory_listing": false, "is_valid_https": false, "is_external_redirect": false, "is_windows_exe_file_on_ipv4": false, "is_phishing_heuristic": false, "is_linux_elf_file_on_ipv4": false, "is_email_address_on_url_query": false, "is_uncommon_clickable_url": false, "is_most_abused_tld": false, "is_domain_blacklisted": false, "is_host_an_ipv4": false, "is_linux_elf_file_on_free_hosting": false, "is_zip_on_directory_listing": false, "is_password_field": false, "is_linux_elf_file": false, "is_empty_page_title": false, "is_directory_listing": false, "is_masked_file": false, "is_suspicious_file_extension": false, "is_suspicious_content": false}, "geo_location": {"countries": ["KR"]}, "url_parts": {"host_nowww": "funad.co.kr", "host": "www.funad.co.kr", "path": "/dynamic/adv/sb/searchnqpopu.html", "query": null, "scheme": "http", "port": 80}, "site_category": {"is_vpn_provider": false, "is_url_shortener": false, "is_anonymizer": false, "is_torrent": false, "is_free_dynamic_dns": false, "is_free_hosting": false}, "web_page": {"keywords": "", "description": "", "title": "404 Not Found"}, "dns_records": {"ns": {"records": [{"country_name": "Korea (Republic of)", "ip": "211.253.28.95", "isp": "KT Corporation", "target": "ns.mailplug.com", "country_code": "KR"}, {"country_name": "Korea (Republic of)", "ip": "223.26.214.26", "isp": "LX", "target": "ns2.mailplug.com", "country_code": "KR"}]}, "mx": {"records": []}}}, "Entity": "www.funad.co.kr:80/dynamic/adv/sb/searchnqpopu.html"}]
```



#### Get domain reputation
Check if a domain is blacklisted by popular and trusted domain blacklist services.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Domain risk threshold. The threshold must be a numeric value. e.g. 3|True|String|0|
|Create Insights|Specify whether the action should create insights or not.|False|Boolean|true|



##### JSON Results
```json
[{"EntityResult": {"alexa_top_100k": false, "domain_length": 17, "alexa_top_10k": false, "blacklists": {"scantime": "0.07", "detection_rate": "0%", "detections": 0, "engines_count": 29, "engines": [{"engine": "ThreatLog", "detected": false, "confidence": "high", "reference": "http://www.threatlog.com/"}, {"engine": "Threat Sourcing", "detected": false, "confidence": "high", "reference": "https://www.threatsourcing.com/"}, {"engine": "URLVir", "detected": false, "confidence": "high", "reference": "http://www.urlvir.com/"}]}, "server": {"region_name": null, "reverse_dns": "", "ip": "", "isp": null, "continent_code": null, "latitude": null, "city_name": null, "longitude": null, "country_code": null, "country_name": null, "continent_name": null}, "host": "qotaerltozres.com", "most_abused_tld": false, "alexa_top_250k": false}, "Entity": "qotaerltozres.com"}, {"EntityResult": {"alexa_top_100k": false, "domain_length": 9, "alexa_top_10k": false, "blacklists": {"scantime": "0.03", "detection_rate": "0%", "detections": 0, "engines_count": 29, "engines": [{"engine": "ThreatLog", "detected": false, "confidence": "high", "reference": "http://www.threatlog.com/"}, {"engine": "Threat Sourcing", "detected": false, "confidence": "high", "reference": "https://www.threatsourcing.com/"}, {"engine": "URLVir", "detected": false, "confidence": "high", "reference": "http://www.urlvir.com/"}]}, "server": {"region_name": null, "reverse_dns": "", "ip": "", "isp": null, "continent_code": null, "latitude": null, "city_name": null, "longitude": null, "country_code": null, "country_name": null, "continent_name": null}, "host": "1.1.1.1", "most_abused_tld": false, "alexa_top_250k": false}, "Entity": "1.1.1.1"}]
```



#### Verify Email
Check if an email is disposable, if it has MX records and more
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Threshold|Email risk threshold. The threshold must be a numeric value. e.g. 3|True|String|0|



##### JSON Results
```json
[{"EntityResult": {"domain": "siemplify.co", "valid_tld": true, "email": "vickie.b@siemplify.co", "role_address": false, "should_block": false, "risky_tld": false, "dirty_words_username": false, "suspicious_domain": false, "score": 100, "educational_domain": false, "dirty_words_domain": false, "did_you_mean": "", "username": "vickie.b", "valid_format": true, "is_spoofable": false, "disposable": false, "government_domain": false, "has_spf_records": true, "domain_popular": false, "has_mx_records": true, "china_free_email": false, "free_email": false, "russian_free_email": false, "police_domain": false, "dmarc_enforced": false, "suspicious_username": false}, "Entity": "VICKIE.B@SIEMPLIFY.CO"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds









