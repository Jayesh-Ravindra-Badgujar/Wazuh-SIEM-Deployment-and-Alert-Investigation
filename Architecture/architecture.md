
# Lab Architecture

## Overview

This project demonstrates the deployment of a **Wazuh Security Information and Event Management (SIEM)** environment in a virtualized lab to monitor and investigate Linux security events. The lab consists of a **Wazuh Server** and a **Kali Linux endpoint** configured with the **Wazuh Agent**. Security events generated on the endpoint are collected, analyzed, and displayed through the Wazuh Dashboard to simulate SOC L1 monitoring and alert investigation.

---

# Lab Components

| Component | Description |
|-----------|-------------|
| Host Machine | Windows 11 |
| Virtualization Platform | Oracle VirtualBox |
| SIEM Platform | Wazuh v4.12.0 |
| Wazuh Server | Ubuntu Server |
| Endpoint | Kali GNU/Linux 2026.2 |
| Agent | Wazuh Agent |
| Dashboard | Wazuh Dashboard |
| Manager IP | 192.168.x.x  |

---

# Lab Architecture

The following diagram represents the overall architecture of the lab.

> **Architecture Diagram:** `lab-architecture.png`

```
                    Windows 11 Host
                           │
                Oracle VirtualBox
                           │
        ┌──────────────────┴──────────────────┐
        │                                     │
        ▼                                     ▼
+-------------------+               +----------------------+
|   Wazuh Server    |<------------->|     Kali Linux       |
| Ubuntu Server     |   Agent Comm. |   Wazuh Agent        |
| Manager & Dashboard|              | Security Events      |
+-------------------+               +----------------------+
```

---

# Communication Flow

1. The Wazuh Server is deployed on an Ubuntu Server virtual machine.
2. A Wazuh Agent is installed and configured on the Kali Linux endpoint.
3. The Kali endpoint continuously collects system logs, authentication logs, and process events.
4. The Wazuh Agent securely forwards these events to the Wazuh Manager.
5. The Wazuh Manager analyzes incoming events using built-in detection rules.
6. Generated alerts are indexed and displayed in the Wazuh Dashboard.
7. The SOC analyst investigates alerts, performs triage, and documents findings.

---

# Component Description

## Wazuh Server

The Wazuh Server acts as the central SIEM platform responsible for collecting, processing, and analyzing security events received from monitored endpoints. It correlates logs using predefined detection rules and generates security alerts for further investigation.

### Responsibilities

- Collect endpoint logs
- Analyze security events
- Generate alerts
- Store event data
- Display alerts through the Wazuh Dashboard

---

## Kali Linux Endpoint

The Kali Linux virtual machine acts as the monitored endpoint. The Wazuh Agent installed on this system collects various operating system events and forwards them to the Wazuh Manager.

### Monitored Events

- Authentication logs
- SSH login attempts
- Process activity
- System events
- File Integrity Monitoring (FIM) events
- Vulnerability Detection data

---

## Wazuh Dashboard

The Wazuh Dashboard provides a centralized interface for monitoring endpoint activity and investigating security alerts.

Key capabilities include:

- Security Event Monitoring
- Alert Investigation
- Endpoint Status Monitoring
- File Integrity Monitoring
- Vulnerability Detection
- MITRE ATT&CK Mapping
- Compliance Dashboard

---

# Log Collection Workflow

```
Security Event Generated
           │
           ▼
     Wazuh Agent
           │
           ▼
    Wazuh Manager
           │
           ▼
   Event Correlation
           │
           ▼
     Alert Generated
           │
           ▼
    Wazuh Dashboard
           │
           ▼
 SOC Analyst Investigation
```

---

# Why this Architecture?

This architecture was designed to simulate a basic Security Operations Center (SOC) environment where endpoint logs are centrally collected and analyzed using a SIEM solution. It demonstrates the complete workflow of log collection, alert generation, investigation, and documentation, providing practical experience with SOC L1 operations.

---

# Skills Demonstrated

- Wazuh SIEM Deployment
- Wazuh Agent Configuration
- Linux Log Collection
- Security Event Monitoring
- Alert Triage
- Security Alert Investigation
- File Integrity Monitoring (FIM)
- Vulnerability Detection
- Log Analysis
- SOC L1 Investigation Workflow

---

# Project Workflow

```
Deploy Wazuh Server
        │
        ▼
Install Kali Agent
        │
        ▼
Generate Security Events
        │
        ▼
Collect Endpoint Logs
        │
        ▼
Analyze Events
        │
        ▼
Generate Alerts
        │
        ▼
Investigate Alerts
        │
        ▼
Document Findings
```
