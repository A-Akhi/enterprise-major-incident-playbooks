# Repository layout

This repository uses a layered operating model rather than a single flat document collection.

## Structure summary

```text
playbooks/       -> response and command execution guidance
runbooks/        -> operational procedures and tactical execution flows
governance/      -> cab, metrics, and reliability control frameworks
policies/        -> formal policy and operating expectations
checklists/      -> fast-action checklists and readiness gates
escalation/      -> escalation paths and coordination triggers
templates/       -> reusable forms and standard status/review templates
examples/        -> illustrative artifacts and communication samples
```

## Design principles

- keep live response content separate from governance and policy
- keep reusable artifacts in dedicated template folders
- preserve compatibility with older, topic-based folder names
- make the repository usable by both responders and leadership
