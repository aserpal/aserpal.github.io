---
title: "Using Security Onion for Network Analysis"
date: 2023-04-29T15:56:17+02:00
draft: false
categories: ["Security Onion", "Network Analysis", "Tool Usage"]
---

# Introduction

[Security Onion](https://securityonionsolutions.com/software) is a popular open-source network security monitoring and intrusion detection system that is used to analyze and respond to security threats. It includes a range of tools and features that are designed to help organizations detect and respond to security incidents.  
Security Onion features include network security monitoring tools (Snort, Suricata, Zeek/Bro), intrusion detection, log management (Logstash, Elasticsearch, Kibana), threat intelligence integration, incident response tools (Wireshark, tcpdump) and scalability. 

Because SO is pretty heavy on system resources when monitoring live traffic we will be testing some of its capabilities with an Import Module, using so-import to inspect a PCAP from [Malware Traffic Analysis](https://www.malware-traffic-analysis.net/2022/03/21/index3.html) that I have previously analyzed in Wireshark. Click on the [link](https://www.malware-traffic-analysis.net/2022/03/21/index3.html) for context and a download link for the [PCAP](https://www.malware-traffic-analysis.net/2022/03/21/2022-03-21-traffic-analysis-exercise.pcap.zip).

## Security Onion Installation

We will Install SO from their [official ISO image (2.3.240-20230426)](https://download.securityonion.net/file/securityonion/securityonion-2.3.240-20230426.iso) in a Virtual Machine. 

### SO-ALLOW

SO uses a role based permission system. Run so-allow and choose the first option, Analyst Machine, to authorize the IP or range of IPs you want to allow web connections from.  
For more information about roles and permissions, check [SO's documentation](https://docs.securityonion.net/en/2.3/): [Role-Based Access Control](https://docs.securityonion.net/en/2.3/rbac.html?highlight=role#role-based-access-control-rbac). 

## SO-IMPORT
[so-import-pcap](https://docs.securityonion.net/en/2.3/so-import-pcap.html?highlight=so-import) will import one or more PCAPs into SO and preserve original timestamps.  

It will: 
- Generate IDS alerts using Suricata
- Generate network metadata using Zeek
- Store IDS alerts and network metadata in Elasticsearch with original timestamps
- Store pcaps where Security Onion Console (SOC) can find them
- Provide a hyperlink for you to view all alerts and logs in Security Onion Console (SOC)


# Alerts

# Dashboard

# Discover



