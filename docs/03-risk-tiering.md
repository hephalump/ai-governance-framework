# 3 · Use-Case Risk Tiering

Not all AI use carries the same risk, so it shouldn't carry the same process. Every use case is rated into one of four tiers. The tier sets the required controls and the approval level — automatically, from the [intake form](../templates/use-case-intake.md).

## How a tier is assigned

A use case takes the **highest** tier triggered by any of these dimensions:

- **Autonomy** — does it advise a human, or act on its own?
- **Consequence** — who/what is affected if it's wrong? (internal convenience → customers → money → safety/legal)
- **Data** — its highest [data tier](02-data-classification.md).
- **Audience** — internal only, or customer/public facing?

## The tiers

| Tier | Profile | Examples | Required controls | Approval |
|------|---------|----------|-------------------|----------|
| **T0 — Prohibited** | Uses the org won't do | Social scoring; covert biometric ID; fully automated adverse decisions with no recourse | Not permitted | — |
| **T1 — High** | Autonomous action, or affects people/money/compliance, or customer-facing at scale | Automated pricing; anything using Regulated data; content published to customers without review | Full [build standards](05-build-standards.md): eval + **human-in-the-loop** + bias test + monitoring + system card + DPIA if regulated | Steering Committee |
| **T2 — Moderate** | Assists consequential work; internal decisions; Confidential data | Draft customer replies for human send; summarize contracts; internal analytics copilots | Eval + human review of outputs + logging + system card | Enablement Hub + domain owner |
| **T3 — Low** | Productivity assist; Public/Internal data; human owns every output | Drafting, brainstorming, code assist, meeting notes | Acceptable-use policy only; self-serve | None (self-serve) |

## The point of tiering

It's a **speed feature**, not a gate. T3 (the large majority of use) is self-serve with zero process. That's what earns the org the right to review T1 properly — reviewers aren't drowning in low-risk requests, so the genuinely risky 5% gets real attention.
