# SOC Environment SIEM Lab

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

- **Kali Linux**
  - Wazuh Manager
  - Wazuh Indexer
  - Wazuh Dashboard

- **Windows 11 Endpoint**
  - Wazuh Agent
  - Microsoft Sysmon

- **Ubuntu Linux Endpoint**
  - Wazuh Agent

- **pfSense Firewall**
  - Remote Syslog
  - Network traffic monitoring

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

### Authentication Activity Dashboard

Monitors:

- Successful logins
- Failed logins
- Authentication trends
- Top failed usernames
- Authentication events by host

---

### Endpoint Process Activity Dashboard

Monitors:

- Process creation events
- Frequently executed processes
- Parent-child process relationships
- User activity
- Recent process executions

---

### Network Traffic Dashboard

Monitors:

- Network traffic volume
- Source IP activity
- Destination IP activity
- Firewall pass/block actions
- Protocol distribution
- Recent network connections

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
