# 6 · Intake & Approval Workflow

The operating loop of the Enablement Hub. Designed so the common case is *fast* and only real risk gets real scrutiny.

## The flow

```
  Submit ──▶ Auto-triage ──▶ [T3?] ──▶ Self-serve. Done. (target: instant)
   (form)      (by tier)       │
                               ├─▶ [T2] ──▶ Hub + domain owner review ──▶ Build to standards ──▶ Ship
                               │                                            (eval + human-in-loop)
                               └─▶ [T1] ──▶ Steering Committee review ──▶ Build ──▶ Pre-prod sign-off ──▶ Monitor
                                            (risk assessment + DPIA)
```

## Steps

1. **Submit** — the [intake form](../templates/use-case-intake.md) captures purpose, data tier, autonomy, and audience.
2. **Auto-triage** — those four answers compute the [risk tier](03-risk-tiering.md). No human needed to route.
3. **Review** — scaled to tier (see table). Reviewers use the [risk assessment template](../templates/risk-assessment.md).
4. **Build** — to the [build standards](05-build-standards.md) for the tier.
5. **Approve & ship** — sign-off at the required level; publish the [system card](../templates/system-card.md).
6. **Monitor & review** — production monitoring + a scheduled re-review.

## Who approves what (and how fast)

| Tier | Reviewer | Target SLA | Artifacts required |
|------|----------|-----------|--------------------|
| **T3** | None — self-serve | Instant | Acceptable-use ack |
| **T2** | Enablement Hub + domain owner | 3 business days | Eval results, system card |
| **T1** | AI Steering Committee | 10 business days | Risk assessment, eval, DPIA (if regulated), system card |

## Tool requests

Same front door. Want a tool that isn't approved yet? Submit it; the Hub runs it through the [tool-evaluation checklist](../templates/tool-evaluation-checklist.md) (security, data terms, cost, admin controls) and adds it to the approved list or explains why not. **SLA: 5 business days** — fast enough that nobody needs to go rogue.

## The SLA is the adoption strategy

If T2 review takes three weeks, people route around it and you've lost. Publishing — and *hitting* — these SLAs is what makes the sanctioned path the fastest path.
