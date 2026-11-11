# Enterprise Major Incident Management (MIM) Playbooks

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Framework: ITIL 4](https://img.shields.io/badge/Framework-ITIL%204-blue.svg)](https://www.axelos.com/certifications/itil-service-management)
[![Contributions welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)](CONTRIBUTING.md)

Practitioner-oriented guidance for major incident command, operational recovery, security escalation, and post-incident improvement in enterprise platform environments.

## Purpose

Use this repository as a practical reference library for teams responsible for production stability and service resilience. Its documents support incident response, stakeholder communications, security handoffs, change governance, problem management, and reliability oversight. Adapt the guidance to your organization’s service definitions, authority model, regulatory obligations, and tooling before using it operationally.

## Start here

- **During a major incident:** [Incident Commander's first 15 minutes](playbooks/incident/incident-commander-first-15-min.md), then [P1 major incident command](playbooks/incident/p1-major-incident-command.md).
- **To execute and restore service:** [P1 incident execution](runbooks/incident-response/p1-incident-execution.md) and the [service restoration checklist](runbooks/service-recovery/service-restoration-checklist.md).
- **For security concerns:** [SecOps / SIRT escalation matrix](playbooks/security/secops-sirt-escalation-matrix.md) and [security and operations escalation paths](escalation/security-and-ops-escalation-paths.md).
- **After recovery:** [Problem investigation and RCA lifecycle](playbooks/problem/problem-investigation-and-rca-lifecycle.md) and the [blameless post-mortem template](templates/blameless-post-mortem-template.md).
- **For controlled changes and reliability:** [Change governance](governance/change-management/cab-governance-and-emergency-changes.md) and [SLO / SLA / error-budget governance](governance/metrics/sla-slo-error-budget-governance.md).

## Repository structure

```text
.
├── checklists/      Short-form incident and change checklists
├── docs/            Repository navigation and structure guidance
├── escalation/      Operational and security escalation routes
├── examples/        Illustrative communication artifacts
├── governance/      Change management and reliability oversight
├── legacy-compatibility/  Migration note; no legacy topic folders are included
├── playbooks/       Incident command, problem management, and security guidance
├── policies/        Formal incident governance expectations
├── runbooks/        Repeatable incident execution and service recovery procedures
└── templates/       Reusable status-update and post-incident documents
```

See the [documentation index](docs/README.md) and [repository layout guide](docs/repo-layout.md) for more detail.

## Using this library

These are Markdown reference documents; there is no application to install or run. Start with the relevant playbook, use its linked runbook or checklist for execution, and capture outcomes with the provided templates. Treat examples as fictional illustrations, not approved customer communications or incident facts.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before proposing changes. Keep documents actionable, use relative links, and avoid sensitive or organization-specific information.

## License

Distributed under the [MIT License](LICENSE).
