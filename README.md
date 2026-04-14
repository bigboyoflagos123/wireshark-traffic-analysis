# Wireshark Traffic Analysis Project

## 🔍 Overview
This project focuses on analyzing real network traffic captured from a home WiFi environment using Wireshark. A total of 1,965 packets were analyzed, with emphasis on DNS and HTTP protocols to understand device behavior and identify potential security concerns.



## 🛠 Tools Used
- Wireshark (Windows)
- Display Filters: `dns`, `http`, `tcp.stream eq 17`


## 🌐 Environment
- **Network:** Home WiFi  
- **Client Device:** Windows Laptop (172.20.10.5)  
- **Gateway:** 172.20.10.1  
- **Packets Captured:** 1,965  
- **Date:** March 30, 2026  



## 📊 Key Findings
- DNS queries to services from Google, Apple, and Microsoft (normal background activity)
- HTTP download initiated via Microsoft BITS using Google CDN
- Unencrypted HTTP traffic observed ⚠️
- TCP anomalies detected (retransmissions and out-of-order packets)
- QUIC protocol traffic identified (encrypted and harder to inspect)



## 🛡 SOC Analyst Perspective

| Observation | Analysis |
|------------|--------|
| DNS queries | Expected system background activity |
| HTTP download (BITS) | Requires verification (can be abused by malware) |
| TCP anomalies | Likely network congestion |
| QUIC traffic | Normal but reduces visibility |
| RST packets | Potentially suspicious, requires further investigation |



## 📁 Project Files
- `Wireshark_Traffic_Analysis_OLA.docx` — Full technical report



## 🧠 Skills Demonstrated
- Live packet capture and traffic analysis
- Wireshark filtering and investigation
- TCP stream analysis and packet inspection
- Protocol analysis (DNS, HTTP, TCP)
- Security-focused interpretation of network activity



## ⚠️ Security Insight
The presence of unencrypted HTTP traffic and the use of legitimate tools like Microsoft BITS highlight potential attack vectors that should be monitored in a SOC environment.



## 🚀 Next Steps / Improvements
- Deeper analysis of QUIC traffic
- Integration with SIEM tools for log correlation
- Detection rule creation based on observed patterns



**Olamide Olasunkanmi**  
Cybersecurity Student | TryHackMe SOC Level 1 Path
