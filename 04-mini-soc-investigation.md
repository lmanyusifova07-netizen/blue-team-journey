# Mini SOC Investigation #4

## Scenario

A suspicious `svchost.exe` process was found in Task Manager.

```text
Process: svchost.exe
PID: 24160
Location: C:\Users\Vivabook\AppData\Roaming\svchost.exe
Company: Microsoft Corporation
Description: Host Process for Windows Services
```
### My Analysis
- The process name is svchost.exe.
- The PID is 24160.
- The company is listed as Microsoft Corporation.
- The description looks normal.
- However, the process location is suspicious.
- A normal svchost.exe is usually located in C:\Windows\System32.
- The location C:\Users\Vivabook\AppData\Roaming\ is not the normal location for svchost.exe.
- The company name and description alone do not prove that the process is safe.
- The suspicious location is the main reason for considering this process suspicious.
- I would not delete the file immediately because it could remove important evidence.

### Conclusion

- Classification: Potentially Suspicious Activity

- The process requires further investigation because its location is unusual.

### Further Investigation
- Check the Parent PID.
- Identify which process created svchost.exe.
- Check the digital signature.
- Investigate the file and its location.
- Check related Windows logs and other process activity.

### What I Learned
- Learned that the process path is important when investigating a process.
- Learned that a normal process name does not always mean the process is safe.
- Learned that company and description information should also be verified.
- Learned why suspicious files should not be deleted immediately.
- Learned how Parent PID can help during process investigation.
- Practiced analyzing a suspicious process from a SOC Analyst perspective.
