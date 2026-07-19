# 7 · AI Incident Response

AI incidents are a *when*, not an *if*. A calm, rehearsed process is the difference between a near-miss and a headline.

## What counts as an AI incident

- A harmful, biased, or materially wrong output that reached a person or customer.
- Data exposure (regulated/confidential data sent to an unapproved model or leaked in output).
- A successful prompt injection or misuse of an AI system.
- An automated system taking a wrong consequential action.
- Sustained quality drift past the system's defined threshold.

## Severity

| Sev | Definition | Response |
|-----|-----------|----------|
| **SEV-1** | Customer/regulatory/safety impact, or regulated-data exposure | Immediate: page owner + Risk/Legal; contain now |
| **SEV-2** | Internal harm or a near-miss with real potential | Same-day triage by the Hub |
| **SEV-3** | Minor/contained; no material impact | Logged; reviewed in weekly Hub triage |

## The loop

1. **Report** — anyone, via the incident channel. Good-faith reporting is never penalized.
2. **Contain** — disable or fall back the system to its safe default (see [build standards](05-build-standards.md)). Stop the bleeding before diagnosing.
3. **Assess** — severity, scope, root cause, who's affected. Pull the logs.
4. **Notify** — per severity: owner, Steering Committee, and Legal/Risk for SEV-1 (they own regulatory/disclosure calls).
5. **Remediate** — fix, re-eval, and re-approve before the system goes back live.
6. **Learn** — blameless post-incident review; feed the lesson back into [build standards](05-build-standards.md) so the whole enterprise inherits the fix.

## Why blameless matters

The failure mode isn't incidents — it's *hidden* incidents. A culture where people quietly bury AI mistakes is far more dangerous than one where they surface fast. Protect the reporter, fix the system.
