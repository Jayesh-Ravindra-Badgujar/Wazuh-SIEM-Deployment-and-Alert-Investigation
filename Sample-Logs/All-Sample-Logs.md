
# Sample Logs

## Overview

This document contains sample security events collected from the Kali Linux endpoint and analyzed using Wazuh SIEM. These logs demonstrate common security activities monitored by a SOC analyst during alert investigation.

---

# 1. Authentication Logs (SSH)

### Failed SSH Login

```log
Jul 23 10:08:01 hacker sshd-session[9703]: pam_unix(sshd:auth): authentication failure
Jul 23 10:08:03 hacker sshd-session[9703]: Failed password for hacker via SSH
Jul 23 10:08:14 hacker sshd-session[9703]: Failed password for hacker via SSH
Jul 23 10:08:21 hacker sshd-session[9703]: Failed password for hacker via SSH
Jul 23 10:08:23 hacker sshd-session[9703]: Connection closed by authenticating user hacker
```

### Successful SSH Login

```log
Jul 23 10:08:41 hacker sshd-session[10224]: Accepted password for hacker via SSH
Jul 23 10:08:41 hacker sshd-session[10224]: pam_unix(sshd:session): session opened for user hacker(uid=1000)
```

---

# 2. Sudo Activity

```log
Jul 22 22:49:49 hacker sudo[2458]: hacker : TTY=pts/0 ; PWD=/home/hacker ; USER=root ; COMMAND=/usr/bin/apt update
Jul 22 22:49:49 hacker sudo[2458]: pam_unix(sudo:session): session opened for user root(uid=0)
Jul 22 22:49:51 hacker sudo[2458]: pam_unix(sudo:session): session closed for user root

Jul 22 23:09:25 hacker sudo[12347]: hacker : COMMAND=/usr/sbin/reboot
Jul 22 23:09:25 hacker sudo[12347]: pam_unix(sudo:session): session opened for user root(uid=0)
Jul 22 23:09:25 hacker sudo[12347]: pam_unix(sudo:session): session closed for user root
```

---

# 3. Process Monitoring

```log
Jul 23 10:12:05 systemd[1]: Started apache2.service
Jul 23 10:12:08 systemd[1]: Started ssh.service
Jul 23 10:13:15 bash[2256]: Executed command: ps aux
Jul 23 10:13:41 bash[2264]: Executed command: top
Jul 23 10:14:03 systemd[1]: Started cron.service
```

---

# 4. File Integrity Monitoring (FIM)

```log
Rule: File Integrity Monitoring

File: /etc/passwd
Action: Modified

Previous SHA256:
8e31d72f7d5b...

Current SHA256:
5d67ab91dfe2...

Timestamp:
2026-07-23 10:18:24
```

---

# 5. Vulnerability Detection

```log
Package:
openssl

Installed Version:
3.0.x

Severity:
Medium

Status:
Package detected during endpoint inventory scan.

Recommendation:
Update to the latest available package version.
```

---

# Log Sources

| Event | Source |
|--------|--------|
| SSH Authentication | sshd |
| User Authentication | PAM |
| Sudo Activity | sudo |
| Process Monitoring | systemd |
| File Integrity Monitoring | Wazuh FIM |
| Vulnerability Detection | Wazuh Vulnerability Detection |

---

# Summary

The collected logs demonstrate common security events monitored by the Wazuh SIEM platform. These events were used to validate log collection, perform alert investigation, and simulate SOC L1 monitoring activities, including authentication monitoring, privilege escalation tracking, process analysis, file integrity monitoring, and vulnerability assessment.
