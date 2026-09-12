# Blue Team Journey 🛡️

This repository documents my journey into Blue Team and SOC cybersecurity.

## Day 1 — Git, GitHub & Linux

### What I've learned

### Git & GitHub
- git init
- git clone
- git status
- git add
- git commit
- git push
- git diff
- git rm
- git mv
- git branch

### Linux
- pwd
- ls
- cd
- mkdir
- touch
- cp
- mv
- rm
- cat
- less
- whoami
- id
- uname -a
- ip addr




## Day 2 — Linux, Permissions & Logs

### Linuxs
- Practiced `chmod` with numeric 
- Practiced file and directory management
- Learned how `~`, `.`, and `..` work
- Learned the difference between files and directories
- Practiced `rm`, `rm -r`, `mv`, `cp`, and other commands

### Linux Permissions
- Learned `read`, `write`, and `execute` permissions
- Learned how to read permissions with `ls -l`
- Learned owner, group, and otherand symbolic notation
- Learned permission values: `r=4`, `w=2`, `x=1`

### Logs
- Learned what system logs are
- Learned why SOC Analysts investigate logs
- Practiced using `journalctl`
- Learned how to filter logs by service and priority




## Day 3 — Networking & Mini SOC Investigation
### Networking
- Learned what an IP address is and how it identifies a host on a network
- Learned the difference between network and host portions of an IPv4 address
- Learned what a subnet mask does
- Learned the difference between public and private IP addresses
- Learned how NAT allows private devices to communicate with the internet
- Learned the basics of IPv4 and IPv6
- Learned the difference between static and dynamic IP addresses
- Learned unicast, multicast, broadcast and anycast
- Learned what network ports are and the basic port ranges
- Learned what a socket is
- Learned the difference between TCP and UDP
- Learned the purpose of DNS and DHCP
- Learned common protocols and ports:
SSH — 22
DNS — 53
HTTP — 80
HTTPS — 443
DHCP — UDP 67/68


## Day 4 — Windows Security & Logs

### Windows Security Logs
- Learned what Windows Event Viewer is
- Learned how Windows Security Logs work
- Learned what Event ID, Source, Level, User, and Computer mean
- Learned the difference between Audit Success and Audit Failure
- Learned how to filter Security Logs by Event ID

### Event ID 4672
- Learned what Event ID 4672 means
- Learned what Special Logon means
- Learned about `SYSTEM` and `NT AUTHORITY`
- Learned that Audit Success does not always mean that an event is safe
- Learned that Event ID 4672 is not necessarily malicious

### Event ID 4624
- Learned what Event ID 4624 means
- Learned that Event ID 4624 indicates a successful logon
- Learned how to check the logon type
- Learned how to identify the account that logged on
- Learned how to identify the source of a logon
- Practiced analyzing successful logon events

### Event ID 4625
- Learned what Event ID 4625 means
- Learned what Logon Type 2 means
- Learned how to investigate failed logon attempts
- Learned how to read Failure Reason and Status
- Learned how to identify the process related to an event
- Practiced checking Process ID in Task Manager


## Day 5 — Windows Processes

### Processes
- Learned what a process is
- Learned what a PID is
- Learned that each process has its own PID
- Learned that one program can have multiple processes
- Practiced finding processes and PIDs in Task Manager
- Practiced checking process properties
- Learned how to check process path, description, and company
- Learned how to identify a suspicious process location
- Learned why the process name alone is not enough
- Learned what Analyze Wait Chain does

### Process Investigation
- Practiced investigating a suspicious `svchost.exe` process
- Identified a suspicious process location
- Learned that process information alone does not prove that a process is safe
- Learned why suspicious files should not be deleted immediately
- Learned the importance of preserving evidence
- Learned how Parent PID can help identify the process that created another process
- Practiced analyzing processes from a SOC Analyst perspective


## Day 6 — SIEM

### SIEM Fundamentals
- Learned what SIEM means
- Learned how SIEM collects logs and events from different sources
- Learned the difference between SIM and SEM
- Learned how SIEM helps SOC Analysts analyze security events

### SIEM Correlation
- Learned what correlation means in SIEM
- Learned how SIEM can correlate events from different sources
- Learned how correlation rules can generate alerts
- Learned the relationship between correlation, alerts, and investigation

### SIEM Alerts
- Learned what a SIEM alert is
- Practiced reading alert information such as source IP, target, protocol, failed logins, severity, and priority
- Learned that an alert does not automatically mean a confirmed security incident

### Severity & Priority
- Learned what Severity means
- Learned what Priority means
- Learned the difference between the seriousness of an event and the urgency of investigation

### Mini SIEM Investigation
- Investigated multiple failed SSH login attempts
- Identified a possible brute-force attack pattern
- Analyzed a successful login following multiple failed attempts
- Practiced classifying suspicious activity
- Identified further investigation steps
- Learned how to approach SIEM alerts from a SOC Analyst perspective



## Day 7 — SIEM Log Sources, Correlation & Query Logic

### SIEM Log Sources
- Learned what log sources are
- Learned how SIEM collects logs from different sources
- Practiced identifying Windows, Firewall, and VPN log sources
- Learned why multiple log sources are useful during security investigations

### Log → Event → Alert
- Learned the relationship between logs, events, and alerts
- Learned that an event represents an activity recorded by a system
- Learned that SIEM can analyze events and generate alerts based on rules and patterns
- Learned that an alert does not automatically mean a confirmed security incident

### SIEM Query Logic
- Learned how SIEM queries can be used to search for specific security events
- Practiced filtering failed login attempts by username, IP address, and time period
- Learned how to identify suspicious patterns in authentication logs
- Practiced identifying possible brute-force activity

### Log Correlation
- Learned how to correlate events from different log sources
- Practiced connecting Windows Security, Firewall, and VPN activity using the same source IP
- Learned how correlation can provide a broader picture of suspicious activity
- Learned that multiple related events can strengthen a security hypothesis

### Practical Investigation
- Investigated multiple failed login attempts followed by a successful login
- Analyzed activity involving an administrator account
- Practiced identifying suspicious authentication patterns
- Learned to investigate activity after a successful login
- Practiced identifying the device or IP involved in suspicious activity
- Learned that suspicious activity should be investigated before being classified as a confirmed incident


 
