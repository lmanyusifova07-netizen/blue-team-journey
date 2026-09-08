# Mini SOC Investigation #3

## Scenario

A Windows Security log recorded repeated failed logon events when Google Chrome was opened.

```text
Event ID: 4625
Logon Type: 2
Account Name: Vivabook
Failure Reason: Unknown user name or bad password.
Status: 0xC000006E
Caller Process Name:
C:\Users\Vivabook\AppData\Local\Google\Chrome\Application\chrome.exe
Source Network Address: -

```

### My Analysis
Event ID 4625 indicates a failed logon attempt.
The target account was Vivabook.
The failure reason indicated an unknown username or bad password.
Logon Type 2 indicates an interactive/local logon attempt.
The source network address was -, so there was no indication of a remote network source.
The caller process was chrome.exe.
I checked the process ID from the event and matched it with the Chrome process in Task Manager.
I tested the behavior by closing Chrome and observing the Security logs.
No new 4625 event appeared while Chrome was closed.
When Chrome was opened again, a new 4625 event appeared.
This showed a strong correlation between Chrome being opened and the failed authentication event.
However, the event alone does not prove that Chrome is malicious.

### Conclusion

Classification: Potentially Suspicious Activity / Requires Further Investigation

The repeated 4625 events are strongly correlated with the Chrome process, but the exact reason for the failed authentication attempt is not yet known.

### Further Investigation
Determine what Chrome operation is triggering the local authentication attempt.
Investigate Chrome extensions, settings, and stored credentials.
Correlate the 4625 event with other Windows Security and application logs.
Determine whether the authentication attempt is expected or abnormal.

### What I Learned
Learned how to investigate Windows Event ID 4625.
Learned how to interpret Logon Type 2.
Learned how to use the Caller Process Name field during investigation.
Practiced correlating a Security event with a running process using its PID.
Learned how to test a hypothesis by comparing system behavior before and after opening an application.
Learned that correlation does not automatically prove malicious activity.
