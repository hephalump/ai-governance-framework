# 8 · Operating Model

Governance is only as good as the org that runs it. Three bodies, clear decision rights, and a deliberate bias toward *enabling* over *policing*.

## The three bodies

**AI Enablement Hub** *(the engine — small, central, hands-on)*
Owns the framework, tooling, evaluations, training, and the [intake queue](06-intake-and-approval.md). Builds reference implementations and dashboards. Runs day-to-day enablement. This is the team that *builds and ships*, not just writes policy.

**AI Steering Committee** *(the cross-functional brain)*
Chaired by the Hub lead; members from Technology, Data, HR, Legal, Risk/Compliance, and each major business unit. Sets enterprise AI strategy, approves [T1 use cases](03-risk-tiering.md), owns the policy, and reviews the adoption metrics that go to the board. Meets monthly.

**Champions Network** *(the reach — distributed, embedded)*
One or two trained advocates embedded in each business unit. They surface use cases, run local enablement, and are the Hub's eyes and ears. This is how governance and adoption scale to *thousands* of people without a big central team.

## Decision rights (RACI, abridged)

| Decision | Hub | Steering Cmte | BU / Owner | Legal/Risk |
|----------|-----|---------------|------------|-----------|
| Approve T3 use | — | — | self-serve | — |
| Approve T2 use | **A/R** | I | C | I |
| Approve T1 use | R | **A** | C | C |
| Approve a new tool | **A/R** | I | C | C |
| Set policy | R | **A** | C | C |
| Regulatory / disclosure call | I | C | I | **A** |

*(A = accountable, R = responsible, C = consulted, I = informed)*

## What "good" looks like (board-level metrics)

The [adoption dashboard](https://github.com/yourusername/ai-adoption-dashboard) tracks the numbers the board actually cares about:

- **Adoption** — active users and % of eligible workforce, by business unit.
- **Value** — use cases in production and estimated hours/$ saved.
- **Flow** — intake volume, approval SLA attainment, backlog.
- **Risk** — incidents by severity, shadow-AI signals, % of systems with a current eval and system card.

## The 90-day version

1. **Weeks 1–4:** ship the acceptable-use policy, the data-classification table, and the tool-eval rubric; approve an initial tool set; stand up the intake form.
2. **Weeks 5–8:** convene the Steering Committee; recruit the first champions; ship one visible reference implementation.
3. **Weeks 9–12:** launch the adoption dashboard; publish the first metrics; run enablement sessions in two business units.
