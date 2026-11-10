# Playbook: P1 Major Incident Command & Bridge Operations

## 1. Overview & Declaration Criteria
* **Severity Level:** Priority 1 (P1) - Critical Impact
* **Trigger Conditions:** Complete core service degradation, multi-region outage, data loss risk, or uncontained active security event impacting production.
* **Primary Objective:** Restore core service availability and contain blast radius rapidly while maintaining clean operational governance.

---

## 2. Roles & Responsibilities Matrix (RACI)

| Role | Primary Responsibility | Assigned Lead |
| :--- | :--- | :--- |
| **Incident Commander (IC)** | Owns bridge strategy, hypothesis driving, and triage cadence. | Major Incident Lead |
| **Technical Lead (SME)** | Directs hands-on log analysis, telemetry isolation, and fix deployment. | Lead Platform / SRE Engineer |
| **Communications Lead** | Manages asynchronous stakeholder updates (slack/email) every 15 mins. | Service Delivery / MIM |
| **Scribe** | Logs key event timestamps, decisions, and hypothesis test results. | Operations Analyst |

---

## 3. Immediate Action Protocol (First 15 Minutes)
