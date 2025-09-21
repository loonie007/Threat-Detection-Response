# 🛡️ SOC Lab Project – Threat Detection & Response

This repository showcases my Security Operations Center (SOC) lab project, simulating real-world attacks and defensive monitoring using a custom virtualized environment.  
It highlights threat detection, incident response, and automated defense mechanisms through hands-on SOC workflows.

---

## 🚀 Project Overview
- Tools Used: pfSense, Wazuh SIEM, Suricata IDS/IPS, Splunk, Microsoft Sentinel, Kali Linux, Windows Server 2022, Ubuntu.
- Attack Simulations:
  - 🔑 SSH Brute Force (Hydra)
  - 📂 File Integrity Monitoring (FIM) tampering
- Detection & Response:
  - Wazuh alerting with Active Response
  - Splunk dashboards
  - Microsoft Sentinel correlation rules

---

## 🏗️ Architecture
![SOC Architecture](docs/architecture_diagram.png)  
Diagram: pfSense firewall, segmented LANs (IT, HR, Marketing, DMZ), SIEM integration.

---

## ⚡ Lab Setup
1. VirtualBox Topology:
   - pfSense firewall with 3 LANs
   - Windows Server 2022 (Domain Controller)
   - Ubuntu server (Wazuh Agent)
   - Kali Linux attacker
   - Windows 10/11 endpoints
2. SIEM Deployment:
   - Wazuh OVA (standalone manager)
   - Splunk forwarders
   - Sentinel connector
3. EDR/NDR Simulation:
   - Suricata IDS for network traffic
   - Wazuh Active Response for endpoint defense

📖 Full step-by-step guide → [docs/lab_manual.md](docs/lab_manual.md)

---

## 🔥 Attack Simulations
### 1. SSH Brute Force (Hydra)
```bash
hydra -l user -P rockyou.txt ssh://192.168.56.101
