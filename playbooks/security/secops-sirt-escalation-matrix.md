# SecOps and SIRT escalation matrix

## Objective

This process defines when an operational incident must trigger security escalation, evidence preservation, and a coordinated handoff to the Security Incident Response Team (SIRT).

## Trigger conditions

Escalate immediately when there is evidence of:

- data exfiltration or unusual outbound transfer patterns
- unauthorized administrative access
- privilege misuse or credential compromise
- malware or suspicious binaries on production nodes
- malicious activity tied to an active production outage

## Handoff flow

1. Confirm event severity and operational impact.
2. Notify the on-call SecOps / SIRT lead.
3. Separate the security investigation from the normal operational bridge if needed.
4. Preserve evidence before remediation when the situation requires forensic review.
5. Coordinate service restoration with the Incident Commander and security lead.

## Governance notes

- Preserve evidence before destructive remediation when possible.
- Maintain a clear command split between operations and security where needed.
- Ensure access to logs, forensic snapshots, and vault rotation steps is documented and approved.

## Related

- [P1 major incident command](../incident/p1-major-incident-command.md)
