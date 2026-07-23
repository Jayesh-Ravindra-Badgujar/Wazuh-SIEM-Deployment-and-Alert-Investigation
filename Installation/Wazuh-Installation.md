# Wazuh Installation

## Overview

This document outlines the installation of the Wazuh SIEM platform in a virtualized lab environment using Oracle VirtualBox. The Wazuh Server was deployed to collect, analyze, and visualize security events from monitored endpoints.

---

## Lab Environment

| Component | Details |
|-----------|---------|
| Host OS | Windows 11 |
| Virtualization | Oracle VirtualBox |
| Wazuh Version | 4.12.0 |
| Wazuh Server | Linux VM |
| Endpoint | Kali Linux 2026.2 |

---

## Installation Steps

### 1. Create the Virtual Machine
- Create a Linux virtual machine in Oracle VirtualBox.
- Allocate CPU, RAM, and storage resources.
- Install the operating system.

### 2. Install Wazuh
- Update the operating system.
- Download and install the latest Wazuh server package.
- Complete the installation using the official installer.

### 3. Access the Dashboard
- Open the Wazuh Dashboard using the server IP address.
- Log in with the administrator credentials.
- Verify that the dashboard is accessible.

### 4. Verify the Installation
- Confirm that the Wazuh services are running.
- Ensure the dashboard loads successfully.
- Verify that the Wazuh Manager is ready to receive agent connections.

---

## Outcome

- Successfully deployed the Wazuh SIEM platform.
- Verified dashboard accessibility.
- Prepared the environment for agent deployment and security event monitoring.
