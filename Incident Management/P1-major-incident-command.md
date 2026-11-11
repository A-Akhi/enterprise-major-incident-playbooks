# P1 Major Incident Command Playbook

## Purpose

This playbook provides a common command structure for coordinating a Priority 1 (P1) service incident from declaration through recovery and handoff. Adapt severity criteria, contact routes, and approval authorities to local policy before using it.

## 1. Activate and establish command

1. Declare the incident using the organization’s severity criteria. Record the incident ID, start time (UTC), affected service, and known customer impact.
2. Open the approved incident bridge and a dedicated written channel. Share the incident ID and a link to the source of truth.
3. Appoint an Incident Commander (IC), Technical Lead, Communications Lead, and Scribe. Name deputies if response is expected to be prolonged.
4. Set a response cadence, initially every 15 minutes or sooner if impact changes materially.
5. Ask participants to keep discussion focused on actionable facts, current hypotheses, and the next decision.

Use the [Incident Commander’s first 15 minutes checklist](incident-commander-first-15-min.md) for the initial setup.

## 2. Roles and responsibilities

| Role | Primary responsibility |
| --- | --- |
| Incident Commander | Owns incident coordination, priorities, decisions, and escalation; delegates technical work. |
| Technical Lead | Coordinates investigation and mitigation with subject-matter experts; reports evidence, risks, and options to the IC. |
| Communications Lead | Publishes approved, time-stamped stakeholder updates and tracks the next update time. |
| Scribe | Maintains the incident timeline, decisions, actions, owners, and key evidence links. |
| Subject-matter experts | Investigate assigned systems and report findings through the Technical Lead. |

One person may cover multiple roles in a small response, but the IC should remain clearly identified and technical investigation should not displace command responsibilities.

## 3. Assess impact and coordinate triage

- Confirm affected services, regions, customer journeys, and the observed symptoms.
- Separate verified facts from hypotheses; assign an owner and a check-in time to each investigation thread.
- Review relevant monitoring, recent changes, dependencies, and known failure modes.
- Record mitigation options with expected benefit, risk, approval needs, and rollback criteria before execution.
- Apply a change freeze or other containment only through the organization’s approved authority and process.
- Escalate promptly when impact expands, the response is blocked, or a security indicator is suspected.

## 4. Mitigate and verify recovery

1. The IC confirms the proposed mitigation and any required approvals; the Technical Lead coordinates execution.
2. Record the action, executor, approval, start time, expected result, and rollback or stop condition.
3. Prefer reversible, scoped actions where practical. Do not make undocumented changes during an active response.
4. Verify recovery using service health signals and customer-impact indicators, not only the completion of a change.
5. Continue monitoring for an agreed stabilization period. If symptoms recur, reassess severity and mitigation rather than assuming recovery.

For suspected compromise, data exposure, or malicious activity, engage the designated security response team and follow the [security escalation and handoff process](../Security/Secops-sirt-escalation-matrix.md). Security evidence handling and external disclosures must follow approved organizational procedures.

## 5. Communications

Every update should include:

- Incident ID, severity, and timestamp (UTC).
- A concise statement of customer/service impact, including what is not yet known.
- Current response or mitigation actions, without unsupported root-cause claims.
- The next update time and the appropriate contact or status page.

The Communications Lead should coordinate updates through approved channels. Correct earlier messages when facts change, and avoid sharing sensitive investigation details in broad channels.

## 6. Resolve, hand off, and learn

1. The IC confirms service stability with the Technical Lead and relevant service owner.
2. Communicate resolution or transition status, remaining customer impact, and any monitoring or workaround instructions.
3. Record the incident end/mitigation times, final impact, key decisions, and outstanding risks before closing the bridge.
4. Assign owners and due dates for follow-up actions. Link the incident to a problem record when required by local policy.
5. Schedule a blameless review and capture findings using the [post-mortem template](../Problem%20Management/blameless-post-mortem-template.md).

## Response record checklist

- [ ] Incident ID, severity, start/end times, and impact recorded
- [ ] Incident Commander and response roles named
- [ ] Timeline, decisions, and action owners maintained
- [ ] Stakeholder updates sent on the agreed cadence
- [ ] Mitigations and recovery checks documented
- [ ] Security escalation considered and completed if indicated
- [ ] Handoff, follow-up actions, and review scheduled
