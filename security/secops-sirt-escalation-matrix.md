# Process: SecOps & SIRT Escalation Matrix & Incident Handoff

## 1. Overview & Objectives
During high-severity (P1/P2) operational incidents, the boundary between a standard infrastructure failure and a security breach can be blurred. This document establishes rigorous coordination protocols between IT Operations, Platform Reliability (SRE), and the Security Incident Response Team (SIRT), aligned with **NIST SP 800-61** incident handling standards.
* **Primary Goal:** Ensure immediate identification, containment, and escalation of security incidents discovered during active operational triage without administrative friction.
* **Core Rule:** Any operational incident involving suspected data exfiltration, unauthorized privilege escalation, or active malware compromise immediately triggers dual-command handoff to SIRT.

---

## 2. P1 Operational vs. Security Incident Classification

[P1 Operational Alert] ──> [Triage & Indicators of Compromise (IoC) Check] ──> [Security Breach Detected?]
                                                                               ├── Yes ──> [Activate SIRT & Secure Bridge]
                                                                               └── No  ──> [Standard Major Incident Bridge]

1. **Pure Operational P1:** Massive traffic spikes, hardware failure, database lockups, or cascading microservice timeouts with no evidence of malicious intent or data compromise.
2. **Security-Adjacent P1 (SIRT Handoff Required):** 
   * Rapid or anomalous data egress patterns from core databases.
   * Credential stuffing, unauthorized administrative login spikes, or IAM role assumption misuse.
   * Presence of unauthorized binaries, unexpected listening ports, or known malware signatures on production nodes.

---

## 3. RACI Governance Matrix

| Incident Phase / Task | Major Incident Commander (MIC) | SRE / DevOps Lead | SecOps / SIRT Lead | Executive Leadership |
| :--- | :--- | :--- | :--- | :--- |
| **Initial P1 Triage & Detection** | **A / R** | **R** | **C** | **I** |
| **IoC Analysis & Forensic Preservation** | C | **C** | **A / R** | **I** |
| **Operational Containment (Isolate Traffic/Nodes)** | **A / R** | **R** | **C** | **I** |
| **Forensic Containment (Preserve Evidence/Logs)** | C | C | **A / R** | **I** |
| **External Communications & Legal Disclosure** | C | I | **A / R** | **A** |
| **Post-Incident Review & Blameless RCA** | **A / R** | **R** | **R** | **I** |

*Legend: **R** = Responsible, **A** = Accountable, **C** = Consulted, **I** = Informed*

---

## 4. Handoff & Containment Protocol (NIST SP 800-61 Workflow)

1. **Phase 1: Detection & Immediate Triage**
   * The Incident Commander identifies potential security anomalies on the main bridge and immediately pages the on-call SecOps/SIRT engineer.
2. **Phase 2: Secure Bridge Separation**
   * If malicious activity is confirmed, SIRT assumes operational co-command. A separate, encrypted, and access-restricted secure bridge is convened to prevent internal threat visibility.
3. **Phase 3: Evidence Preservation vs. Service Restoration**
   * *Critical Rule:* Unlike standard P1 outages where nodes are wiped or rebooted instantly to restore service, SIRT must authorize memory dumps, disk snapshotting, and log preservation before any destructive remediation is applied.
4. **Phase 4: Eradication & Recovery**
   * Patch exploited vulnerabilities, rotate compromised API keys and secrets via secure vaults, and validate system integrity before returning assets to production rotation.

---

## 5. Success Metrics & KPIs
* **SecOps Handoff Time:** Average elapsed time from operational P1 identification of security indicators to active SIRT bridge engagement (Target: $< 15 \text{ minutes}$).
* **Forensic Integrity Rate:** Percentage of security-flagged incidents where pre-remediation memory and disk snapshots were successfully preserved without data corruption (Target: $100\%$).
* **Post-Incident Compliance Audit Closure:** Percentage of security audit recommendations addressed within 14 days of incident closure (Target: $\ge 95\%$).

---
*Reference artifact from the [Enterprise Major Incident Management Playbooks](https://github.com/A-Akhi/enterprise-major-incident-playbooks) repository.*
