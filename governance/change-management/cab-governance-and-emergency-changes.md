# CAB governance and emergency changes

## Objective

Reduce avoidable incidents by applying consistent pre-flight review, approval, and emergency-change control.

## Risk tiers

| Risk tier | Example | Governance |
| --- | --- | --- |
| Standard | low-impact config updates | automated gate |
| Normal | feature releases and schema changes | CAB / peer approval |
| High | critical platform changes | full CAB review |
| Emergency | active P1 mitigation or critical vulnerability fix | eCAB fast-track |

## eCAB rules

- emergency change approval requires documented risk and rollback criteria
- at least two authorized approvers are preferred for critical change execution
- post-implementation review must be completed within the operational review window

## Definition of done

- automated tests pass
- rollback plan is documented
- observability is configured
- maintenance window is approved when required
