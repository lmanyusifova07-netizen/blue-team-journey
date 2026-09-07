# Mini SOC Investigation #2

## Scenario

A firewall recorded the following network activity:


Sep 07 14:32:11 firewall: ACCEPT TCP src=192.168.1.25:49152 dst=192.168.1.10:22
Sep 07 14:32:13 firewall: ACCEPT TCP src=192.168.1.25:49153 dst=192.168.1.10:22
Sep 07 14:32:15 firewall: ACCEPT TCP src=192.168.1.25:49154 dst=192.168.1.10:22
Sep 07 14:32:17 firewall: ACCEPT TCP src=192.168.1.25:49155 dst=192.168.1.10:22
Sep 07 14:32:19 firewall: ACCEPT TCP src=192.168.1.25:49156 dst=192.168.1.10:22
Sep 07 14:32:25 firewall: ACCEPT TCP src=192.168.1.25:49157 dst=192.168.1.10:443
Sep 07 14:32:27 firewall: ACCEPT TCP src=192.168.1.25:49158 dst=192.168.1.10:443

### My Analysis
All recorded connections came from the same source IP: 192.168.1.25.
The destination IP was 192.168.1.10.
The activity used the TCP protocol.
The source host made five consecutive connection attempts to port 22 (SSH) within a few seconds.
The source host then made two connections to port 443 (HTTPS).
The firewall marked all of these connections as ACCEPT.
However, an ACCEPT action does not automatically mean that the traffic is legitimate or safe.
The repeated connections from the same source IP within a short period could indicate suspicious or automated network activity.
The activity could have a legitimate explanation, so it should not immediately be classified as malicious.
Conclusion

Classification: Alert / Potentially Suspicious Activity

Further investigation is required before determining whether this activity represents a confirmed security incident.

### Further Investigation
Identify what device or user is associated with 192.168.1.25.
Check whether this device normally communicates with 192.168.1.10.
Review authentication logs for SSH activity from 192.168.1.25.
Check whether the source IP attempted to connect to other ports.
Investigate what activity occurred on the destination server around the same time.
Determine whether the connections were expected or authorized.

### What I Learned
Learned how to analyze basic network activity from firewall logs.
Learned how to identify source and destination IP addresses.
Learned how to identify destination ports and protocols.
Learned that repeated connections from the same source can be a reason for further investigation.
Learned that firewall ACCEPT does not necessarily mean that network activity is safe.
Learned the difference between suspicious activity, an alert, and a confirmed incident.
Practiced approaching network activity from a SOC Analyst perspective.
