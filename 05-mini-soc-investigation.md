# Mini SIEM Investigation #5

## Scenario

A SIEM generated the following alert:

```text
ALERT: Suspicious Login Activity

Time: 22:10:15 – 22:13:42
Source IP: 10.0.0.25
Target: WEB-SERVER-01
Username: admin

Failed Logins: 12
Successful Login: 1

Protocol: SSH
Severity: High
Priority: High
```
## My Analysis
### 1. What happened?

- A suspicious login attempt occurred.

- There were 12 failed login attempts, followed by 1 successful login using the admin account.

### 2. What looks suspicious?

- There were 12 failed login attempts followed by a successful login.

- This looks suspicious because multiple login attempts were made from the same IP address within a short period of time.

### 3. What does the successful login change?

- The successful login shows that after multiple failed attempts, the admin account was successfully used to access the system from the 10.0.0.25 IP address.

- This makes the activity more serious and requires further investigation.

### 4. What do Severity and Priority tell us?
- Severity: High — The event is considered high risk.
- Priority: High — The alert should be investigated urgently.
  
### 5. Classification

- Classification: Suspicious Activity / Possible Brute Force Attack

- The successful login following multiple failed attempts makes the activity more suspicious. However, further investigation is required before confirming it as a security incident.

### 6. Further Investigation
- Investigate the source IP address 10.0.0.25.
- Identify which device is associated with this IP address.
- Determine whether the SSH access to the admin account was expected or authorized.
- Review authentication logs for additional activity.
- Investigate what happened after the successful login.
- Check whether any commands were executed after the successful login.
- Check for changes to files, accounts, or system configuration.

### What I Learned
- Learned how to analyze a SIEM alert.
- Learned how to identify a possible brute-force pattern.
- Learned that a successful login following multiple failed attempts requires deeper investigation.
- Learned the difference between Severity and Priority.
- Learned that an alert does not automatically mean a confirmed security incident.
- Learned how to investigate the source IP, account, authentication activity, and post-login activity.
- Practiced approaching a SIEM alert from a SOC Analyst perspective.
