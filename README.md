# SOC-Home-Lab
#🛡️Building a SOC HomeLab: Wazuh SIEM, Kali Linux Attacker, & Windows 11 Endpoint
## 📌 Project Overview
This project demonstrates the deployment and configuration of a Security Operations Center (SOC) homelab environment. The objective is to simulate real-world cyber attacks, collect security telemetry, and detect malicious activities using an enterprise-grade open-source SIEM platform (**WAZUH**).

## 🏗️ Lab Architecture & Network Topology
* **SIEM / Manager:** Wazuh manager & Dashboard
* **Target Endpoint:** Windows 11 pro (Monitored via Wazuh Agent v4.x)
*  **Attacker Node:** Kali Linux (Used for reconnaissance and attack simulation)

## Lab Demostration
**SOC Lab Archtecture & Wazuh Dashboard**

**Installing Wazuh**

<img width="3186" height="1912" alt="Screenshot 2026-09-06 122626" src="https://github.com/user-attachments/assets/fff9a0eb-acb8-42d1-bf57-9d6864a78a6b" />


## Windows 11 endpoint configuration
*installed the **Wazuh Agent** package on the windows 11 target virtual machine.*

**installing Wazuh Agent on Windows 11**

<img width="1740" height="932" alt="Screenshot 2026-09-09 175922" src="https://github.com/user-attachments/assets/8dc98e41-a0ef-44bf-948b-69633a4484b1" />

*Generated authentication key via `manage_agents` on the Wazuh Manager and enrolled the endpoint*

<img width="1584" height="1408" alt="Screenshot 2026-09-09 121440" src="https://github.com/user-attachments/assets/26279d9e-2d19-4d12-8487-eff3ae4be9f9" />

**Verified realtime telemetry streaming from `Application`, `System`, and `Security` Windows Event logs**

**FIM Setup:** *Added a file I created to the configuration `File integrity monitoring` to monitor *Wazuh_test**

<img width="2374" height="1150" alt="Screenshot 2026-09-09 180533" src="https://github.com/user-attachments/assets/ce4f9f4c-39a4-4e49-a2e3-ec76abb2bb45" />

**Event Detection:** *Watched the event generate instantly the wazuh_test is added*

<img width="3192" height="1212" alt="Screenshot 2026-09-09 122533" src="https://github.com/user-attachments/assets/046d4b12-b92b-4710-8c3c-9805e838d000" />

**Alert Drilldown:** *Inpect document detail*

<img width="1570" height="1456" alt="Screenshot 2026-09-09 122603" src="https://github.com/user-attachments/assets/9461a907-7b1b-4e48-8034-fdff1502e019" />

## Key Security Concepts Applied
* **Host Intrusion Detection (HIDS):** Real-time monitoring of the windows file modifications, registry changes,and process excution.
*  **Log Aggregation & Parsing:** Centralizing Windows Security Event IDs into structured JSON for alert generation.
*  **Detection Engineering:** Observing how raw network attacks map to MITRE ATTACK framework techniques inside the Wazuh Dashboard.

## Tools Used 
* ** Wazuh SIEM / Indexer / Dashboard**
* **Kali Linux**
* **VMware / Hyper-v**

