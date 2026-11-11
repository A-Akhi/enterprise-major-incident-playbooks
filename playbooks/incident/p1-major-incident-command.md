# P1 Major Incident Command

## Purpose

This playbook provides a standard command framework for a Priority 1 incident. It should be adapted to the organization’s service taxonomy, approval routes, and external notification requirements.

## 1. Declare and establish command

1. Declare the incident and record the ID, time, affected service, and clear customer impact.
2. Start the incident bridge and a written channel that acts as the source of truth.
3. Assign the Incident Commander, Technical Lead, Communications Lead, and Scribe.
4. Set a common cadence, usually every 15 minutes during active triage.
5. Ask all participants to focus on facts, risks, decisions, and next actions.

## 2. Assess impact and isolate scope

- Confirm the affected customers, services, and data paths.
- Review monitoring signals, prior changes, and dependencies for the failing system.
- Separate validated facts from hypotheses and assign owners to each line of investigation.
- Maintain a single timeline and decision log.

## 3. Containment and mitigation

- Freeze or restrict unsafe changes only under an authorized process.
- Apply the lowest-risk mitigation that reduces impact without creating new instability.
- Capture rollback criteria, expected duration, and service verification steps.
- If suspicion of compromise or data exposure exists, escalate to the security process immediately.

## 4. Communicate clearly

Every update should include:

- incident ID and severity
- impact summary
- what is known versus unknown
- current mitigation or containment action
- next update time

## 5. Recovery and closure

1. Verify recovery from direct customer-impact evidence and system health checks.
2. Record the end time, final status, and key decision points.
3. Confirm ownership of follow-up actions and review scheduling.
4. Route the incident to the post-incident review process.

## 6. Link to follow-up work

- [Blameless post-mortem template](../../templates/blameless-post-mortem-template.md)
- [Problem investigation and RCA lifecycle](../problem/problem-investigation-and-rca-lifecycle.md)
- [SecOps / SIRT escalation matrix](../security/secops-sirt-escalation-matrix.md)
