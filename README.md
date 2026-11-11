# Enterprise Major Incident Management (MIM) Playbooks

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Framework: ITIL 4](https://img.shields.io/badge/Framework-ITIL%204-blue.svg)](https://www.axelos.com/certifications/itil-service-management)
[![Contributions welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)](CONTRIBUTING.md)

Repository for practitioner-grade major incident response, problem management, change governance, and reliability operations guidance for enterprise platforms.

## Repository structure

```text
enterprise-major-incident-playbooks/
├── README.md
├── CONTRIBUTING.md
├── LICENSE
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
├── governance/
│   ├── README.md
│   ├── change-management/
│   │   └── cab-governance-and-emergency-changes.md
│   └── metrics/
│       └── sla-slo-error-budget-governance.md
├── templates/
│   └── blameless-post-mortem-template.md
├── Incident Management/
├── Change Management/
├── Problem Management/
├── Metrics/
├── Security/
└── ...
```

The new `playbooks/`, `governance/`, and `templates/` folders form the primary structure. The existing named folders remain as compatibility shims so current links continue to resolve.

## Start here

- [Incident Commander first 15 minutes](playbooks/incident/incident-commander-first-15-min.md)
- [P1 major incident command](playbooks/incident/p1-major-incident-command.md)
- [SecOps / SIRT escalation matrix](playbooks/security/secops-sirt-escalation-matrix.md)
- [CAB governance and emergency changes](governance/change-management/cab-governance-and-emergency-changes.md)
- [Problem investigation and RCA lifecycle](playbooks/problem/problem-investigation-and-rca-lifecycle.md)
- [Blameless post-mortem template](templates/blameless-post-mortem-template.md)
- [SLA / SLO / error budget governance](governance/metrics/sla-slo-error-budget-governance.md)

## How to use this repo

1. Establish a single incident commander, communication channel, and a written timeline during P1 response.
2. Use the security runbook whenever suspicious access, data movement, or malware indicators are involved.
3. Apply change controls before high-risk production changes and use eCAB only under approved emergency criteria.
4. Convert post-incident findings into problem records and action items so recurring issues do not repeat.
5. Track service health through SLOs, error budgets, and monthly reliability reviews.

## Contributing

This repo welcomes operational improvements, additional playbooks, and clearer templates. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting changes.

## License

This project is distributed under the [MIT License](LICENSE).
