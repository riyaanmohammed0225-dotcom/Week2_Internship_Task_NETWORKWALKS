# Week2_Internship_Task_NETWORKWALKS
# 🔐 Week 2 – Footprinting, OSINT & Network Scanning

![Kali Linux](https://img.shields.io/badge/OS-Kali%20Linux-blue?logo=kalilinux)
![Windows](https://img.shields.io/badge/OS-Windows-0078D6?logo=windows)
![Nmap](https://img.shields.io/badge/Tool-Nmap%20%7C%20Zenmap-red)
![Cybersecurity](https://img.shields.io/badge/Domain-Cybersecurity-darkgreen)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview

This repository contains my **Week 2 practical work** as part of the Cybersecurity & Ethical Hacking Program at **NETWORKWALKS**.

The project focuses on three important cybersecurity areas:

- Footprinting and Reconnaissance
- Open Source Intelligence (OSINT)
- Network Scanning and Host Discovery

Through hands-on exercises using Kali Linux and Windows, I explored different techniques to gather publicly available information, identify web technologies, enumerate DNS records and discover active hosts within a local network.

## 🎯 Modules Completed

| Module | Description | Category |
|---|---|---|
| W2-PM1 | Footprinting with Multiple Kali Linux Tools | Main Elective |
| W2-PM4 | theHarvester-based Footprinting Attacks | Extra Elective |
| W2-PM5 | Network Scanning using Zenmap | Essential Module |

---

## 🛠️ Module 1 – Footprinting with Multiple Kali Linux Tools (W2-PM1)

**Target:** `networkwalks.com`

**Environment:** Kali Linux

### Tools and Activities

| Tool | Purpose | Practical Activity |
|---|---|---|
| WHOIS | Domain information gathering | Retrieved domain registration details |
| WhatWeb | Website fingerprinting | Identified web technologies |
| Nslookup | DNS resolution | Resolved domain to IP address |
| cURL | HTTP header inspection | Examined HTTP response headers |
| Wafw00f | WAF detection | Identified ModSecurity |
| DNSRecon | DNS enumeration | Identified DNS and service-related records |

### Commands Executed

**1. WHOIS Enumeration**
```bash
whois networkwalks.com
```

**2. Website Fingerprinting**
```bash
whatweb networkwalks.com
```

**3. DNS Resolution**
```bash
nslookup networkwalks.com
```

**4. HTTP Header Inspection**
```bash
curl -I https://networkwalks.com
```

**5. Web Application Firewall Detection**
```bash
wafw00f networkwalks.com
```

**6. DNS Enumeration**
```bash
dnsrecon -d networkwalks.com
```

### Key Observations

- Identified GoDaddy as the domain registrar.
- Detected Apache and WordPress technologies.
- Resolved the domain to `192.232.216.135`.
- Identified ModSecurity (SpiderLabs) as the WAF.
- Collected DNS, mail and service-related information.

---

## 🔎 Module 4 – OSINT with theHarvester (W2-PM4)

**Target:** `microsoft.com`

**Environment:** Kali Linux

**Tool:** theHarvester 4.10.1

### Objective

To understand OSINT techniques and gather publicly available domain-related information using different search sources.

### Commands Executed

**1. Exploring Tool Options**
```bash
theHarvester -h
```

**2. Baidu Search**
```bash
theHarvester -d microsoft.com -l 1000 -b baidu
```

**Observation:** The search returned no IP addresses, email addresses, people or hosts.

**3. Multiple-Source Search**
```bash
theHarvester -d microsoft.com -l 50 -b all
```

### Key Observations

- Explored different OSINT search sources.
- Observed domain-related information gathering.
- Identified limitations caused by missing or invalid API keys.
- Understood the importance of source availability and API configuration.

**Learning Outcome:** Gained practical exposure to OSINT techniques, search-source selection and information gathering limitations.

---

## 🌐 Module 5 – Network Scanning with Zenmap (W2-PM5)

**Operating System:** Windows

**Tool:** Zenmap 7.993 / Nmap

**Network:** Personal mobile hotspot

### Objective

To identify active hosts within a local network, examine IP and MAC address information and visualize the network topology.

### Network Configuration

| Parameter | Value |
|---|---|
| Local IPv4 Address | `10.91.251.27` |
| Subnet Mask | `255.255.255.0` |
| Default Gateway | `10.91.251.23` |
| Network Subnet | `10.91.251.0/24` |

### Scan Configuration

**Zenmap Profile:** Ping Scan

**Target:**
```bash
10.91.251.0/24
```

**Nmap Command:**
```bash
nmap -sn 10.91.251.0/24
```

### Scan Results

| Parameter | Result |
|---|---|
| Total IP Addresses Scanned | 256 |
| Active Hosts Discovered | 2 |
| Scan Duration | 3.49 seconds |

### Discovered Hosts

| IP Address | Identification |
|---|---|
| `10.91.251.23` | Gateway |
| `10.91.251.27` | Local Windows Laptop |

The MAC addresses were identified using Zenmap output and Windows network configuration.

### Network Topology

The Zenmap Topology feature was used to visualize the discovered hosts. The generated network topology was saved as a PDF for documentation.

---

## 📸 Project Evidence

The repository contains screenshots documenting the practical implementation and results.

#WK2-PM1 - Multiple kali linux tools
(whois_screen.png)
(whatweb_screen.png)
(nslookup_screen.png)
(curl_cmd_screen.png)
(waafw00f_screen.png)
(dnsrecon_screen.png)

#WK2-PM4 - theHarvester
(theHarvester_screen.png)

#WK2-PM5 - Zenmap
(zenmap.png)


*Folder structure is a suggested organization for uploading your evidence.*

---

## 💡 Key Learning Outcomes

Through these practical exercises, I gained experience in:

- Domain footprinting and reconnaissance.
- Website technology identification.
- DNS resolution and enumeration.
- HTTP response header analysis.
- Web Application Firewall identification.
- OSINT information gathering.
- Understanding API dependencies in reconnaissance tools.
- Network host discovery using Nmap and Zenmap.
- IP address and MAC address identification.
- Network topology visualization.
- Technical documentation and evidence collection.

## 🔒 Disclaimer

This repository is intended for educational purposes and documents practical cybersecurity exercises.

All scanning and information-gathering activities should be conducted only against systems and networks for which appropriate authorization has been obtained.

The network scanning exercise documented here was performed on my personal mobile hotspot network.

The results represent observations from the practical exercises and should not be interpreted as confirmed security vulnerabilities.

## 🙏 Acknowledgement

I sincerely thank **Waqas Karim (CCIE)** and the **NETWORKWALKS** team for their guidance, training and support throughout this cybersecurity learning journey.

---

**Author:** Mohammed Riyaan  
**Program:** Cybersecurity & Ethical Hacking  
**Organization:** NETWORKWALKS  
**Project:** Week 2 – Footprinting, OSINT & Network Scanning

🚀 *Continuously learning, exploring and building practical cybersecurity skills.*
