# SLO, SLA, and error budget governance

## Reliability hierarchy

SLI -> SLO -> SLA -> error budget

## Policy

- feature velocity must slow when error budget burn is excessive
- reliability review should include service health, burn rate, and recurring incidents
- corrective actions should be tracked to closure with owners and dates

## Typical governance gates

- >50% remaining: normal operations
- 20–50% remaining: increased scrutiny and stability focus
- <20% remaining: deployment freeze for non-essential work
- 0% remaining: full reliability freeze until recovery
