# Enterprise Major Incident Management (MIM) Playbooks

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Framework: ITIL 4](https://img.shields.io/badge/Framework-ITIL%204-blue.svg)](https://www.axelos.com/certifications/itil-service-management)
[![Contributions welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)](CONTRIBUTING.md)

Practitioner-grade major incident command playbooks, triage frameworks, and governance references for enterprise platforms. The material is designed to help teams coordinate high-severity response, restore service safely, communicate clearly, and turn incidents into lasting improvements.

> Adapt these practices to your organization’s policies, regulatory obligations, and service architecture. They are operational guidance, not a substitute for approved emergency, security, or legal procedures.

## Start here

- **Responding to a P1:** [Incident Commander’s first 15 minutes](Incident%20Management/incident-commander-first-15-min.md)
- **Running the incident:** [P1 major incident command](Incident%20Management/P1-major-incident-command.md)
- **Security indicators found during triage:** [SecOps/SIRT escalation and handoff](Security/Secops-sirt-escalation-matrix.md)
- **Reviewing a change:** [CAB governance and emergency changes](Change%20Management/cab-governance-and-emergency-changes.md)
- **Investigating recurrence:** [Problem investigation and RCA lifecycle](Problem%20Management/problem-investigation-and-rca-lifecycle.md)
- **Writing the review:** [Blameless post-mortem template](Problem%20Management/blameless-post-mortem-template.md)
- **Reliability governance:** [SLA, SLO, and error-budget governance](Metrics/sla-slo-error-budget-governance.md)

## Repository structure

```text
enterprise-major-incident-playbooks/
├── README.md
├── CONTRIBUTING.md
├── LICENSE
├── Incident Management/
│   ├── README.md
│   ├── P1-major-incident-command.md
│   └── incident-commander-first-15-min.md
├── Change Management/
│   └── cab-governance-and-emergency-changes.md
├── Problem Management/
│   ├── blameless-post-mortem-template.md
│   └── problem-investigation-and-rca-lifecycle.md
├── Metrics/
│   └── sla-slo-error-budget-governance.md
└── Security/
    └── Secops-sirt-escalation-matrix.md
```

Category folders are retained as named so existing links continue to work. Use the category README files as indexes as the collection grows.

## How to use the playbooks

1. Tailor severity definitions, role names, paging paths, and communication channels to your organization before an incident.
2. During a response, appoint one incident commander, keep technical investigation coordinated, and record decisions and timestamps.
3. Route suspected compromise through your approved security response process; preserve evidence and follow your incident commander/SIRT procedures.
4. After service is stable, document impact, contributing conditions, and owned, trackable follow-up actions.

## Contributing

Improvements and additional playbooks are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for the documentation conventions and review checklist.

## License

This project is distributed under the [MIT License](LICENSE).
