# Enterprise Major Incident Management (MIM) Playbooks

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Framework: ITIL 4](https://img.shields.io/badge/Framework-ITIL%204-blue.svg)](https://www.axelos.com/certifications/itil-service-management)
[![Contributions welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)](CONTRIBUTING.md)

Practitioner-grade guidance for major incident command, governance, reliability engineering, and post-incident improvement in enterprise platform environments.

## Repository purpose

This repository is designed as an operational library for teams responsible for production stability, incident response, and service resilience. It supports several common operating model functions:

- rapid response during high-severity incidents
- structure for incident command and stakeholder communication
- security escalation and evidence-handling coordination
- controlled change and emergency-change execution
- recurring problem analysis and root-cause remediation
- SLO, SLA, and error-budget governance

## Enterprise-standard layout

```text
enterprise-major-incident-playbooks/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── docs/
│   ├── README.md
│   └── repo-layout.md
├── playbooks/
│   ├── README.md
│   ├── incident/
│   │   ├── README.md
│   │   ├── p1-major-incident-command.md
│   │   └── incident-commander-first-15-min.md
│   ├── problem/
│   │   └── problem-investigation-and-rca-lifecycle.md
│   └── security/
│       └── secops-sirt-escalation-matrix.md
├── runbooks/
│   ├── README.md
│   ├── incident-response/
│   │   └── p1-incident-execution.md
│   └── service-recovery/
│       └── service-restoration-checklist.md
├── governance/
│   ├── README.md
│   ├── change-management/
│   │   └── cab-governance-and-emergency-changes.md
│   └── metrics/
│       └── sla-slo-error-budget-governance.md
├── policies/
│   ├── README.md
│   └── incident-governance-policy.md
├── checklists/
│   ├── README.md
│   ├── incident-command-checklist.md
│   └── change-readiness-checklist.md
├── escalation/
│   ├── README.md
│   └── security-and-ops-escalation-paths.md
├── templates/
│   ├── README.md
│   ├── blameless-post-mortem-template.md
│   └── executive-status-update-template.md
├── examples/
│   ├── README.md
│   └── incident-communication-example.md
├── Incident Management/
├── Change Management/
├── Problem Management/
├── Metrics/
├── Security/
└── legacy-compatibility/
    └── README.md
```

## Primary navigation

- [Incident command and response](playbooks/incident/README.md)
- [Problem management](playbooks/problem/problem-investigation-and-rca-lifecycle.md)
- [Security / SIRT handoff](playbooks/security/secops-sirt-escalation-matrix.md)
- [Governance and change control](governance/change-management/cab-governance-and-emergency-changes.md)
- [Reliability metrics and error budgets](governance/metrics/sla-slo-error-budget-governance.md)
- [Templates](templates/README.md)
- [Checklists](checklists/README.md)
- [Escalation paths](escalation/README.md)

## Compatibility note

The original named folders remain in place for ongoing links and historical references. The new folders are the canonical home for future repository growth and operational content.

## Suggested usage

1. Start with the playbooks during active response or major incident triage.
2. Use runbooks when standardizing execution steps across teams.
3. Apply policies and governance guidance for change approvals and reliability guardrails.
4. Add examples and templates to standardize communication, review, and recovery artifacts.

## Contributing

Please review [CONTRIBUTING.md](CONTRIBUTING.md) before submitting changes.

## License

Distributed under the [MIT License](LICENSE).
