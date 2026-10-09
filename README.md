# Incident Investigation & Response

## Overview
A simulated incident investigation focused on identifying suspicious activity, assessing risk, and recommending appropriate containment and response actions.

## Scenario
A user received and downloaded a ZIP email attachment. After extraction, an executable was created, followed by suspicious PowerShell activity and an outbound connection attempt.

## Tools
- Windows incident scenario logs
- Notepad
- Manual timeline and evidence analysis

## Key Findings
- Suspicious attachment: `invoice_viewer.zip`
- Executable created: `invoice_viewer.exe`
- Suspicious PowerShell child process detected
- Outbound connection attempt to `203.0.113.77:443`
- Security tool quarantined the executable
- Other employees may have been exposed to the same attachment

## Response Recommendations
- Assess whether the affected endpoint requires network isolation.
- Preserve relevant email, endpoint, and network logs.
- Investigate PowerShell activity and determine whether the outbound connection succeeded.
- Check for additional affected users or endpoints.
- Verify that the threat has been addressed before restoring normal access.

## Conclusion
The available evidence indicates potentially malicious activity requiring further investigation. A successful compromise or data breach has not been confirmed.

## Important Note
This is a simulated training scenario. The events and IP address are illustrative and do not represent a confirmed real-world attack.
