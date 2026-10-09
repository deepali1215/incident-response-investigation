# Incident Investigation & Response

## 1. Incident Summary
A user received and downloaded a ZIP email attachment. After extraction, an executable file was created, followed by a suspicious PowerShell process and an outbound connection attempt.

## 2. Initial Assessment
- **Priority:** High — pending further investigation
- **Suspected entry point:** Email attachment
- **Affected user:** jpatel
- **Affected endpoint:** Not yet identified
- **Current containment:** `invoice_viewer.exe` was quarantined by a security tool.

## 3. Evidence Observed
- Email attachment received: `invoice_viewer.zip`
- Executable created: `invoice_viewer.exe`
- Suspicious PowerShell child process detected
- Outbound connection attempt to `203.0.113.77:443`
- Executable quarantined by the security tool

## 4. Unknowns
- Did the user execute the file?
- Did the outbound connection succeed?
- Was any data accessed or stolen?
- Were other users or endpoints affected?
- Is any suspicious process or persistence mechanism still present?

## 5. Recommended Next Steps
1. Assess whether the endpoint requires network isolation.
2. Preserve relevant endpoint, email, and network logs.
3. Investigate the executable and suspicious PowerShell activity.
4. Check for other affected users or endpoints.
5. Confirm the scope and impact before closing the incident.

## 6. Current Conclusion
The available evidence indicates potentially malicious activity that requires investigation. A successful compromise or data breach has not yet been confirmed.

## 7. Scope Investigation

- Review email logs to identify other users who received or downloaded `invoice_viewer.zip`.
- Search endpoint logs for `invoice_viewer.exe` and suspicious PowerShell activity on other computers.
- Review network logs for related outbound connection attempts.
- Check whether other security alerts or unusual activity occurred around the same time.

**Current status:** The scope is unknown. Further log analysis is required to determine whether other users or endpoints were affected.

## 8. Containment and Recovery Plan

- Prioritize investigation of Employee C's endpoint due to the suspicious PowerShell alert.
- Assess whether network isolation is needed and follow the organization's incident-response procedure.
- Preserve endpoint, email, and network logs for further analysis.
- Check whether the suspicious process is still active and whether the outbound connection succeeded.
- Determine whether other endpoints were affected.
- Restore normal access only after the threat has been addressed and the endpoint has been verified as safe.

**Current status:** Containment and recovery are not yet confirmed complete.

## 9. Final Assessment

**Finding:** Suspicious activity involving an email attachment, executable file, PowerShell process, and outbound connection attempt.

**Response:** The executable was quarantined. Network isolation and further investigation are recommended as appropriate.

**Remaining checks:** Determine what the PowerShell process did, whether the connection succeeded, and whether other systems were affected.

**Conclusion:** Potentially malicious activity was identified, but a successful compromise or data breach has not been confirmed.