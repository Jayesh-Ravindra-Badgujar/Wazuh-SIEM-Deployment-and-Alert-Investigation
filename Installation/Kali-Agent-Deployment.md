
# Kali Agent Deployment

## Overview

This document describes the deployment of the Wazuh Agent on a Kali Linux endpoint. The agent collects system and security events and securely forwards them to the Wazuh Manager for analysis and alert generation.

---

## Lab Environment

| Component | Details |
|-----------|---------|
| Endpoint | Kali Linux 2026.2 |
| Agent | Wazuh Agent 4.12.0 |
| SIEM Platform | Wazuh 4.12.0 |
| Manager | Wazuh Server |
| Communication | Secure Agent-Manager Connection |

---

## Deployment Steps

### 1. Prepare the Endpoint
- Update the Kali Linux system.
- Verify network connectivity with the Wazuh Manager.

### 2. Install the Wazuh Agent
- Download and install the latest Wazuh Agent package.
- Configure the agent to communicate with the Wazuh Manager.

### 3. Register the Agent
- Enroll the Kali Linux endpoint with the Wazuh Manager.
- Confirm successful agent registration.

### 4. Start the Agent
- Enable and start the Wazuh Agent service.
- Verify that the service is running correctly.

### 5. Verify Connectivity
- Open the Wazuh Dashboard.
- Confirm that the Kali Linux endpoint appears as **Active**.
- Validate that security events are being received.

---

## Monitored Events

- Authentication Logs
- SSH Login Events
- Process Activity
- System Events
- File Integrity Monitoring (FIM)
- Vulnerability Detection

---

## Outcome

- Successfully deployed the Wazuh Agent on the Kali Linux endpoint.
- Established secure communication with the Wazuh Manager.
- Verified log collection and real-time event monitoring through the Wazuh Dashboard.
