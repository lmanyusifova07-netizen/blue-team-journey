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






 
