<img width="1919" height="925" alt="image" src="https://github.com/user-attachments/assets/3b75960e-f67c-4cd9-83b2-f70333352d7d" /># SOC Environment SIEM Lab

A complete Security Operations Center (SOC) lab built using **Wazuh SIEM** to simulate real-world security monitoring, log analysis, and threat detection across Windows, Linux, and network infrastructure.

This project demonstrates the deployment of a centralized SIEM environment capable of collecting, analyzing, and visualizing security events from multiple log sources while supporting incident investigation through custom dashboards and detection rules.

---

## Project Overview

The objective of this project was to design and implement a functional SOC environment capable of:

- Deploying a Wazuh SIEM platform
- Monitoring Windows and Linux endpoints
- Integrating a pfSense firewall
- Collecting logs from multiple sources
- Detecting suspicious activities
- Building operational security dashboards
- Creating custom correlation rules for threat detection

The environment simulates how a Security Operations Center monitors infrastructure using centralized log collection and analysis.

---

## Lab Architecture

The lab consists of the following components:


| Virtual Machines  | Components |
| ------------- | ------------- |
| **Kali Linux**  | Wazuh Manager <br> Wazuh Indexer<br> Wazuh Dashboard |
| **Windows 11 Endpoint**  | Wazuh Agent<br> Microsoft Sysmon |
| **Ubuntu Linux Endpoint** | Wazuh Agent<br> auth.log |
| **pfSense Firewall** | Remote Syslog <br> Network traffic monitoring |
 


---

## Technologies Used

- Wazuh SIEM
- Microsoft Sysmon
- pfSense Firewall
- Ubuntu Linux
- Windows 11
- Kali Linux
- VirtualBox
- Syslog
- XML Rule Development

---

## Features

- Centralized log collection
- Windows endpoint monitoring
- Linux endpoint monitoring
- Firewall log monitoring
- Authentication monitoring
- Process monitoring
- Network traffic monitoring
- Interactive dashboards
- Custom correlation rules
- Threat detection
- Security event investigation

---

## Dashboards

The project includes three operational dashboards:

| **Dashboard** | **Monitors** |
| --------------| -------------|
| Authentication Activity Dashboard | Successful logins<br>Failed logins<br>Top failed usernames<br> Authentication events by host |
| Endpoint Process Activity Dashboard | Process creation events<br>Frequently executed processes<br>Parent-child process relationships<br>User activity<br>Recent process executions |
| Network Traffic Dashboard | Network traffic volume<br>Source IP activity<br>Destination IP activity<br>Firewall pass/block actions<br>Protocol distribution<br>Recent network connections |

---

## Detection Engineering

Custom detection rules were developed to identify suspicious activity, including:

- Brute-force login attempts
- Suspicious PowerShell execution

These rules demonstrate how multiple security events can be correlated to generate meaningful alerts.

---

## Future Improvements

Future versions of this lab will include:

- Suricata IDS integration
- Threat Intelligence feeds
- DNS monitoring
- Web proxy logging
- Sigma rule integration
- MITRE ATT&CK mapping
- Malware sandbox integration
- Automated response workflows

---

## Author

**te7mina1**

Cybersecurity Student | SOC Analyst | SIEM | Blue Team

---

> This project was developed to demonstrate SIEM deployment, security monitoring, and detection engineering within a virtual SOC environment.
