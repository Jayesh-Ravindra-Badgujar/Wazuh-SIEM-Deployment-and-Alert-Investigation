
# Dashboard Configuration

## Overview

This document describes the initial configuration and verification of the Wazuh Dashboard after deploying the Wazuh Server and enrolling the Kali Linux agent. The dashboard provides a centralized interface for monitoring endpoint activity, investigating alerts, and analyzing security events.

---

## Lab Environment

| Component | Details |
|-----------|---------|
| Dashboard | Wazuh Dashboard |
| SIEM Platform | Wazuh 4.12.0 |
| Endpoint | Kali Linux 2026.2 |
| Agent Status | Active |

---

## Configuration Steps

### 1. Access the Dashboard
- Open the Wazuh Dashboard using the server IP address.
- Log in using the administrator credentials.

### 2. Verify Agent Status
- Navigate to **Endpoints**.
- Confirm that the Kali Linux agent is listed as **Active**.
- Verify successful communication between the agent and the Wazuh Manager.

### 3. Validate Event Collection
- Generate sample security events on the Kali endpoint.
- Ensure the events are successfully received and displayed in the dashboard.

### 4. Explore Security Modules
Verify the functionality of the following modules:

- Threat Hunting
- File Integrity Monitoring (FIM)
- Vulnerability Detection
- MITRE ATT&CK
- Security Events

### 5. Monitor Alerts
- Review generated alerts based on severity.
- Analyze event details and investigate security logs.
- Validate that alerts are categorized correctly.

---

## Dashboard Features

- Endpoint Monitoring
- Real-Time Alert Monitoring
- Security Event Analysis
- File Integrity Monitoring (FIM)
- Vulnerability Detection
- Threat Hunting
- MITRE ATT&CK Mapping
- Compliance Monitoring

---

## Outcome

- Successfully configured and accessed the Wazuh Dashboard.
- Verified active communication with the Kali Linux agent.
- Confirmed successful log collection and real-time alert monitoring.
- Validated key security modules for SOC L1 alert investigation.
