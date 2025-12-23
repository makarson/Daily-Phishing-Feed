# 🧟 ZONBI - Daily Phishing & Malware Feed

<p align="center">
  <pre>
#  ______  ____  _   _  ____  _____ 
# |__  / |/ __ \| \ | || __ )|_   _|
#   / /| | |  | |  \| ||  _ \  | |  
#  / /_| | |__| | |\  || |_) | _| |_ 
# /____|_|\____/|_| \_||____/ |_____|
#
  </pre>
  <b>Automated Threat Intelligence Gathering System</b><br>
  <i>Maintained by <b>makarson</b></i>
</p>

---

## 🛡️ Project Overview
**ZONBI** is a high-frequency **Threat Intelligence (TI)** feed that aggregates, cleans, and categorizes malicious indicators from multiple trusted sources including OpenPhish, URLHaus, and Phish.Database.

This repository provides daily-updated blocklists designed for security analysts, SOC teams, and network administrators to strengthen their defense infrastructure.

## 📊 Data Feeds
All data is processed and split into three specific formats to ensure compatibility with various security solutions:

| Category | Indicator Type | Direct Link | Primary Usage |
| :--- | :--- | :--- | :--- |
| **URLs** | Full Path | [🔗 urls.txt](urls.txt) | Proxy, EDR, SIEM Correlation |
| **Domains** | FQDN | [🔗 domains.txt](domains.txt) | DNS Sinkhole, Pi-hole, AdGuard |
| **IPs** | IPv4 | [🔗 ips.txt](ips.txt) | Firewall, IPS/IDS Blocklists |

---

## ⚙️ Automated Workflow
1. **Aggregation:** Collects raw data from global threat intelligence providers.
2. **Validation:** Sanitizes links and removes duplicates using the `validators` library.
3. **Categorization:** Parses raw URLs into separate Domain and IP datasets.
4. **Continuous Update:** Synchronized every 24 hours via GitHub Actions.

## 🚀 Quick Integration
You can fetch the latest feeds directly via `curl` for your automation scripts:

```bash
# Get the latest Domain list
curl -O [https://raw.githubusercontent.com/makarson/Daily-Phishing-Feed/main/domains.txt](https://raw.githubusercontent.com/makarson/Daily-Phishing-Feed/main/domains.txt)

# Get the latest IP list
curl -O [https://raw.githubusercontent.com/makarson/Daily-Phishing-Feed/main/ips.txt](https://raw.githubusercontent.com/makarson/Daily-Phishing-Feed/main/ips.txt)
