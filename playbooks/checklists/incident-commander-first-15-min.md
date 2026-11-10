# Checklist: Incident Commander's First 15 Minutes

This rapid-action checklist is designed for the Incident Commander (IC) upon the declaration of a Priority 1 (P1) outage. The objective is to establish immediate operational control, isolate the blast radius, and quiet bridge noise.

## [00:00 - 00:05] Detection & Bridge Initialization
* [ ] **Acknowledge & Declare:** Formally classify the incident as P1 based on core service impact or data loss risk.
* [ ] **Spin Up Bridge:** Open the dedicated emergency bridge (video/audio line) and secondary communication channel (e.g., Slack/Teams incident channel).
* [ ] **Assign Core Roles:** Explicitly designate:
  * **Technical Lead (SME):** Lead engineer driving triage.
  * **Communications Lead:** Responsible for stakeholder updates.
  * **Scribe:** Documenting key timestamps, hypotheses, and decisions.

---

## [00:05 - 00:10] Containment & Noise Quarantining
* [ ] **Quarantine Executive Noise:** Mute all non-essential observers on the bridge. Direct leadership and stakeholders to the asynchronous communication channel.
* [ ] **Enforce Change Freeze:** Issue an immediate freeze on all CI/CD deployment pipelines across the affected service domain.
* [ ] **Review Telemetry Baselines:** Ask SMEs: *"What alerts triggered first, and what system components changed in the 60 minutes prior?"*

---

## [00:10 - 00:15] Hypothesis & First Stakeholder Sync
* [ ] **Drive Single Hypothesis:** Force SMEs to align on one primary working hypothesis rather than chasing multiple edge cases simultaneously.
* [ ] **Publish First Update:** Send out the initial asynchronous stakeholder communication (Impact summary, current containment action, and next update time).
* [ ] **Set Next Cadence:** Establish a firm 15-minute sync interval for technical checkpoints.

---
*Reference artifact from the [Enterprise Major Incident Management Playbooks](https://github.com/A-Akhi/enterprise-major-incident-playbooks) repository.*
