# Template: Blameless Post-Mortem & Root Cause Analysis (RCA)

## 1. Incident Metadata
* **Incident ID:** INC- [Insert Number]
* **Date & Time (UTC):** [YYYY-MM-DD HH:MM]
* **Severity Level:** Priority 1 (P1) / Priority 2 (P2)
* **Duration:** [Total minutes from detection to mitigation]
* **Impacted Services:** [List affected microservices, databases, or API routes]
* **Incident Commander (IC):** [Name]
* **Author:** [Name]

---

## 2. Executive Summary
*Provide a concise 3-sentence summary of what happened, why it happened, the customer impact, and the immediate mitigation taken.*

---

## 3. Timeline of Events (All times in UTC)
* **[HH:MM]** - Monitoring alert fired for [Metric/Service name].
* **[HH:MM]** - Major Incident Commander declared P1 and opened the technical bridge.
* **[HH:MM]** - Change freeze applied across deployment pipelines.
* **[HH:MM]** - Root cause identified as [Brief technical description].
* **[HH:MM]** - Remediation executed (e.g., rollback / traffic reroute).
* **[HH:MM]** - Services stabilized; metrics verified over 15-minute baseline. Bridge closed.

---

## 4. Impact Assessment
* **User Impact:** [Percentage of users affected, failed transactions, or error rates].
* **Financial / Operational Impact:** [Estimated downtime cost or SLA breach metrics].
* **Regulatory / Compliance Flag:** [Indicate whether this incident triggers mandatory reporting thresholds under NIS2/DORA or internal audit standards].

---

## 5. Root Cause Analysis (The "5 Whys")
1. **Why did the service fail?**  
   *Answer:* Connection pool exhaustion due to upstream timeout spikes.
2. **Why did timeout spikes occur?**  
   *Answer:* A cascading failure triggered by an unhandled retry storm from client SDKs.
3. **Why did client SDKs flood the service?**  
   *Answer:* Exponential backoff and jitter configurations were missing from the latest client release.
4. **Why was the configuration missing?**  
   *Answer:* The configuration template lacked automated validation checks during the CI/CD pipeline.
5. **Why were validation checks absent?**  
   *Answer:* Technical debt in the legacy deployment framework prevented pre-flight governance enforcement.

---

## 6. Lessons Learned
* **What went well:** Rapid bridge initialization and clear separation of executive communication channels prevented noise during triage.
* **What went poorly:** Lack of automated circuit breakers prolonged Mean Time to Restore (MTTR).
* **Where we got lucky:** The failure occurred during off-peak traffic hours, limiting total customer exposure.

---

## 7. Action Items & Remediation Roadmap

| ID | Action Item / Corrective Measure | Owner | Priority | Target Date |
| :--- | :--- | :--- | :--- | :--- |
| **ACT-01** | Implement exponential backoff & circuit breakers in client SDKs. | Platform Team | High | [Date] |
| **ACT-02** | Add automated configuration schema validation to CI/CD pipelines. | DevOps / SRE | Medium | [Date] |
| **ACT-03** | Update P1 escalation playbook to include early circuit breaker checks. | Major Incident Lead | Low | [Date] |

---
*Reference artifact from the [Enterprise Major Incident Management Playbooks](https://github.com/A-Akhi/enterprise-major-incident-playbooks) repository.*
