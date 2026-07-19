# Enterprise AI Governance Framework

**A practical, adoption-first framework for scaling AI safely across a data- and research-driven enterprise.**

Most AI governance material is either a bunch of documentation nobody reads or a slide that says "be responsible." Neither of those are particularly effective. 

This is a new framework for adopting AI. Risk considered controls, clear decision rights, and templates that can actually be used, all so governance *accelerates* adoption instead of blocking it.


> **Note** This is authored to demonstrate how to deploy and operationalize AI governance. It's intentionally concise and usable, with consideration given to [NIST AI RMF](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/), [ISO/IEC 42001](https://www.iso.org/standard/81230.html), and the [EU AI Act](https://artificialintelligenceact.eu/).

---

## Principles

1. **Adoption-first.** The goal is *more* AI use, done safely. Controls increase with risk; only the genuinely risky use cases (<10%) get heavy review.
2. **Risk Adjusted** Rick in automated pricing decisions are treated differently from marketing brainstorming.
3. **Builder first** All controls map to builder controlled actions (eval thresholds, humans-in-the-loop, logging requirements) — see [Build Standards](docs/05-build-standards.md).
4. **Data Classification**  *what data touches the model* is what matters most. The [data model](docs/02-data-classification.md) is foundational.
5. **Auditable** Every *consequential* AI system carries a [system card](templates/system-card.md) and a logged decision trail.

## How to navigate

| Section | What it is |
|---|---|
| [1 · Principles](docs/01-principles.md) | The responsible-AI commitments everything else enforces |
| [2 · Data Classification](docs/02-data-classification.md) | The core control layer |
| [3 · Risk Tiering](docs/03-risk-tiering.md) | How use cases are rated, and the controls required at each tier |
| [4 · Acceptable Use](docs/04-acceptable-use.md) | The one-page policy every employee gets |
| [5 · Build Standards](docs/05-build-standards.md) | Lifecycle guardrails: evaluation, human oversight, monitoring |
| [6 · Intake & Approval](docs/06-intake-and-approval.md) | The workflow, SLAs, and who approves what |
| [7 · Incident Response](docs/07-incident-response.md) | What to do when an AI system misbehaves |
| [8 · Operating Model](docs/08-operating-model.md) | Enablement Hub, Steering Committee, Champions network, decision rights |
| [Standards Mapping](STANDARDS-MAPPING.md) | How this maps to NIST AI RMF / ISO 42001 / EU AI Act |
| [Templates](templates/) | Intake form, risk assessment, tool-evaluation checklist, system card |

## Using this framework

- **New to AI at work?** Read [Acceptable Use](docs/04-acceptable-use.md) (5 minutes).
- **Have a use case?** Start with the [Intake form](templates/use-case-intake.md); it auto-routes you to the right controls.
- **Building?** Follow [Build Standards](docs/05-build-standards.md) and publish a [system card](templates/system-card.md).
- **Just starting?** Read [Operating Model](docs/08-operating-model.md) and adapt the [Intake & Approval](docs/06-intake-and-approval.md) workflow.

## A companion reference implementation

Governance is only credible if it's been *built against*. The [Governed AI Workflow Automation](https://github.com/hephalump/vendor-maintenance-parser) reference implementation applies these standards end to end - measured accuracy (eval harness), confidence-gated, human-in-the-loop, untrusted-input handling, and a data-classification-aware deployment mode — as a worked example of what "responsible AI in practice" looks like here.

---

*Licensed [CC BY 4.0](LICENSE) — use and adapt with attribution.*
