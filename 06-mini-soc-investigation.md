# Mini SIEM Investigation #6

## Scenario

A SIEM collected the following events from Windows Security, Firewall, and VPN logs:

```text
[Windows Security]
Time: 23:14:02
Event ID: 4625
Account: administrator
Source IP: 10.0.0.45
Status: Failed Logon

[Firewall]
Time: 23:14:04
Source IP: 10.0.0.45
Destination: SERVER-02
Port: 22
Action: ACCEPT

[VPN]
Time: 23:14:07
Username: administrator
Source IP: 10.0.0.45
Login: Failed

[Windows Security]
Time: 23:14:18
Event ID: 4625
Account: administrator
Source IP: 10.0.0.45
Status: Failed Logon

[Windows Security]
Time: 23:14:31
Event ID: 4624
Account: administrator
Source IP: 10.0.0.45
Status: Successful Logon
```
## My Analysis

- The activity came from the same source IP address: 10.0.0.45.

- There were multiple authentication attempts involving the administrator account.

- The first Windows Security event was Event ID 4625, which indicates a failed logon.

- The Firewall then recorded a connection from the same IP address to SERVER-02 on port 22. The action was ACCEPT, meaning the network connection was allowed. It does not mean that authentication was successful.

- The VPN also recorded a failed login for the administrator account.

- Another Windows Security Event ID 4625 occurred, showing another failed logon attempt.

- Finally, Event ID 4624 showed that the administrator account successfully logged on from the same IP address.

- The activity is suspicious because multiple failed attempts were followed by a successful login from the same IP address within a short period of time.

- The administrator account also makes the activity more important to investigate because it may have higher privileges on the system.


## Conclusion

- Classification: Suspicious Activity / Possible Brute-Force Attack

- The activity requires further investigation before it can be classified as a confirmed security incident.


## Further Investigation
- Investigate the source IP address 10.0.0.45.
- Identify which device or user is associated with the IP address.
- Determine whether the administrator login was expected or authorized.
- Investigate what happened after the successful login.
- Check which commands or processes were executed after the login.
- Check whether files, accounts, or system configurations were modified.
- Review additional Windows Security, Firewall, and VPN logs for related activity.
- Investigate the SSH connection to port 22.

## What I Learned
- Learned how to correlate Windows Security, Firewall, and VPN logs.
- Learned how the same source IP can help connect related security events.
- Practiced analyzing multiple failed logins followed by a successful login.
- Learned how to interpret Event IDs 4625 and 4624.
- Learned that Firewall ACCEPT does not automatically mean that authentication was successful.
- Learned why successful access to an administrator account requires deeper investigation.
- Learned how to investigate activity that occurs after a successful login.
- Practiced analyzing correlated SIEM events from a SOC Analyst perspective.
