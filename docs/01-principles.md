# 1 · Responsible-AI Principles

Seven commitments. Every control elsewhere in this framework exists to enforce one of them.

| # | Principle | What it means in practice |
|---|-----------|---------------------------|
| 1 | **Human accountability** | A named person owns every AI system's outcomes. AI assists decisions; it doesn't absorb responsibility for them. |
| 2 | **Proportionate oversight** | The higher the stakes, the more human review. Consequential decisions (people, money, safety, compliance) always keep a human in the loop. |
| 3 | **Data protection** | Data may only meet AI tools approved for its [classification](02-data-classification.md). Regulated and customer data never trains an external model. |
| 4 | **Measured before trusted** | No AI system reaches production without an [evaluation](05-build-standards.md) showing it meets a stated accuracy/quality bar on a representative test set. |
| 5 | **Transparency** | Users are told when they're interacting with AI. Every consequential system carries a [system card](../templates/system-card.md). |
| 6 | **Fairness** | Systems that affect people are tested for disparate impact before and during production. |
| 7 | **Security by default** | AI inputs are treated as untrusted (prompt injection, data exfiltration). Access, logging, and secrets follow existing security standards. |

### Why "adoption-first" is a principle, not a caveat

Ungoverned AI use doesn't stop when you write a restrictive policy — it goes underground ("shadow AI"), which is *worse* for risk. The safest enterprise is one where the sanctioned path is also the easiest path. Every control here is designed to be the path of least resistance for the 90% of low-risk use, so people don't route around it.
