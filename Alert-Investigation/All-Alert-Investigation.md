
# Alert Investigation

## Overview

This document summarizes the security events generated and investigated in the Wazuh SIEM lab. Each event was analyzed through the Wazuh Dashboard to understand its cause, assess its impact, and simulate the alert investigation workflow followed by a SOC L1 analyst.

---

# Investigation Workflow

For every security event, the following investigation process was followed:

1. Generate the security event.
2. Verify that the alert is received in the Wazuh Dashboard.
3. Review the alert severity and rule information.
4. Analyze the associated logs.
5. Identify the root cause.
6. Document the findings.

---

# 1. Failed SSH Login

## Description

Multiple failed SSH authentication attempts were generated to simulate unauthorized access attempts.

### Logs Observed

- Authentication logs
- SSH login failures
- Source IP
- Username
- Timestamp

### Investigation

- Verified repeated failed login attempts.
- Reviewed authentication logs.
- Confirmed no successful login occurred.
- Determined the activity as a failed authentication attempt.

### Outcome

The event was successfully detected and logged by Wazuh for further analysis.

---

# 2. Successful SSH Login

## Description

A successful SSH login was performed to verify user authentication monitoring.

### Logs Observed

- Successful authentication
- Username
- Source IP
- Login timestamp

### Investigation

- Verified successful user authentication.
- Reviewed login details.
- Confirmed legitimate access.

### Outcome

The successful login event was collected and displayed correctly in the Wazuh Dashboard.

---

# 3. Sudo Activity

## Description

Privilege escalation was simulated using the `sudo` command.

### Logs Observed

- User executing sudo
- Executed command
- Timestamp
- Terminal session

### Investigation

- Reviewed sudo execution logs.
- Verified the executed command.
- Confirmed privilege escalation activity.

### Outcome

The sudo activity was successfully detected and monitored.

---

# 4. File Integrity Monitoring (FIM)

## Description

File Integrity Monitoring was used to detect modifications made to monitored files.

### Logs Observed

- File created
- File modified
- File deleted
- Permission changes

### Investigation

- Identified the modified file.
- Compared file attributes.
- Verified whether the modification was expected.

### Outcome

Wazuh generated alerts whenever monitored files changed.

---

# 5. Vulnerability Detection

## Description

The Vulnerability Detection module scanned installed packages and identified software with known security vulnerabilities.

### Information Reviewed

- Vulnerable package
- CVE Identifier
- Severity
- Installed version

### Investigation

- Reviewed affected software.
- Checked associated CVEs.
- Evaluated vulnerability severity.

### Outcome

The dashboard successfully identified vulnerable software packages present on the endpoint.

---

# Skills Demonstrated

- Security Event Monitoring
- Alert Investigation
- Authentication Log Analysis
- Linux Log Analysis
- SSH Monitoring
- Privilege Escalation Monitoring
- File Integrity Monitoring (FIM)
- Vulnerability Detection
- SOC L1 Alert Analysis
- Security Event Documentation

---

# Summary

This investigation demonstrates the deployment and practical use of Wazuh SIEM for monitoring endpoint activity, analyzing security events, and investigating alerts. The project provides hands-on experience with authentication monitoring, privilege escalation detection, file integrity monitoring, vulnerability detection, and process analysis, closely reflecting the daily responsibilities of a SOC L1 Analyst.
