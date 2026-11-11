# Process: Problem Management, Known Error Databases (KEDB), & Systemic Risk Mitigation

## 1. Overview & Objectives
While Major Incident Management (MIM) focuses on rapid restoration, **Problem Management** focuses on eliminating recurring failures. 
* **Primary Goal:** Investigate underlying root causes of P1/P2 incidents, prevent recurrence, and minimize the impact of known errors across enterprise platforms.
* **Core Rule:** Every P1 incident *must* have a corresponding Problem record linked to its post-mortem action items.

---

## 2. Problem Lifecycle & Investigation Stages

[P1 Incident Closed] ──> [Problem Record Created] ──> [Root Cause Investigation] ──> [KEDB Entry] ──> [Permanent Fix / Patch]

1. **Identification & Triage:** Major Incident Lead converts post-mortem findings into an active Problem ticket.
2. **Investigation & Workaround:** Subject Matter Experts (SMEs) analyze logs, metrics, and failure patterns to develop a temporary workaround if a permanent fix is delayed.
3. **Known Error Database (KEDB) Publication:** Document the failure mode, symptoms, and verified workaround so support teams can instantly mitigate future occurrences.
4. **Permanent Remediation:** Track corrective action items (from post-mortems) through engineering deployment pipelines until verified closed.

---

## 3. Problem Prioritization Matrix (Urgency vs. Impact)

| Impact / Frequency | High Frequency (Recurring) | Low Frequency (Isolated) |
| :--- | :--- | :--- |
| **High Business Impact** | **Priority 1 (P1):** Immediate engineering task force assigned. | **Priority 2 (P2):** Deep-dive investigation required within 5 days. |
| **Low Business Impact** | **Priority 3 (P3):** Backlog item for tech debt sprint. | **Priority 4 (P4):** Monitored; documented in KEDB if needed. |

---

## 4. Known Error Database (KEDB) Entry Template
*When publishing a known error for internal engineering and operations teams, follow this standardized layout:*

* **Error ID:** KEDB- [Insert Number]
* **Related Incidents:** [INC-001, INC-042]
* **Symptom:** [What do users or monitoring tools observe? e.g., HTTP 504 Gateway Timeout during peak auth token exchange]
* **Root Cause:** [Technical explanation: e.g., Connection pool saturation caused by unhandled client SDK retry storms]
* **Verified Workaround:** [Immediate steps support/SMEs can take: e.g., Temporarily scale up database read replicas and throttle client ingress traffic]
* **Permanent Fix Status:** [Scheduled for release v2.14 / Patch deployed on YYYY-MM-DD]

---

## 5. Success Metrics & KPIs
* **Problem Backlog Aging:** Time elapsed from incident closure to permanent fix deployment.
* **Recurring Incident Rate:** Percentage of P1 incidents caused by previously identified, unpatched known errors (Target: 0%).
* **KEDB Utilization:** Frequency of support and engineering teams resolving alerts using documented workarounds.

---
*Reference artifact from the [Enterprise Major Incident Management Playbooks](https://github.com/A-Akhi/enterprise-major-incident-playbooks) repository.*


