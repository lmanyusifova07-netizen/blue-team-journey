# Mini SOC Investigation #1

## Scenario

An SSH login activity was observed on a Linux server.

## Log Analysis

There were 4 failed login attempts followed by 1 successful login attempt.

- Username: `admin`
- Source IP: `192.168.1.50`
- Failed attempts: 4
- Successful attempts: 1
- Protocol: SSH

## Analysis

The activity could be suspicious because multiple failed login attempts were followed by a successful login from the same IP address.

However, the activity cannot automatically be considered malicious. The IP address may belong to a legitimate user or internal device.

Further investigation would be required.

## SOC Classification

**Alert / Potentially Suspicious Activity**

Further investigation is needed to determine whether this is a real security incident.

## What I Learned

- How to read SSH authentication logs
- How to identify failed and successful login attempts
- How to identify the source IP and username
- The difference between an alert and an incident
- Why suspicious activity should be investigated before declaring it an incident
