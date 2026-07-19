# Standards Mapping

This framework is original and practical, but deliberately aligned to the three references enterprises are measured against; it's audit-defensible and easy to reconcile with a formal program.

## NIST AI RMF (Govern · Map · Measure · Manage)

| RMF function | Where this framework does it |
|--------------|------------------------------|
| **Govern** | [Principles](docs/01-principles.md), [Operating Model](docs/08-operating-model.md) (roles, RACI, policy ownership), [Acceptable Use](docs/04-acceptable-use.md) |
| **Map** | [Intake](docs/06-intake-and-approval.md) + [Risk Tiering](docs/03-risk-tiering.md) + [Data Classification](docs/02-data-classification.md) (context, purpose, and risk are established up front) |
| **Measure** | [Build Standards → MEASURE](docs/05-build-standards.md) (eval sets, accuracy targets, bias & prompt-injection testing) |
| **Manage** | [Build Standards → MANAGE](docs/05-build-standards.md) + [Incident Response](docs/07-incident-response.md) (human-in-loop, monitoring, drift, response) |

## ISO/IEC 42001 (AI Management System)

| ISO 42001 theme | Where |
|-----------------|-------|
| Leadership & AI policy | [Operating Model](docs/08-operating-model.md), [Principles](docs/01-principles.md) |
| AI risk & impact assessment | [Risk Tiering](docs/03-risk-tiering.md), [Risk Assessment template](templates/risk-assessment.md) |
| Operational controls | [Build Standards](docs/05-build-standards.md), [Data Classification](docs/02-data-classification.md) |
| Performance evaluation & improvement | [Build Standards](docs/05-build-standards.md) (monitoring), [Incident Response](docs/07-incident-response.md) (blameless review) |
| Documented information | [System Card](templates/system-card.md), logging requirements |

## EU AI Act (risk-based obligations)

| EU AI Act concept | Where |
|-------------------|-------|
| Prohibited practices | [Risk Tier T0](docs/03-risk-tiering.md) |
| High-risk obligations (risk mgmt, data governance, human oversight, accuracy, logging, transparency) | [Tier T1 controls](docs/03-risk-tiering.md) + [Build Standards](docs/05-build-standards.md) |
| Transparency to users | [Principles #5](docs/01-principles.md), [Acceptable Use](docs/04-acceptable-use.md) |
| Post-market monitoring | [Build Standards → MANAGE](docs/05-build-standards.md), [Incident Response](docs/07-incident-response.md) |

> **Design stance:** align to the *substance* of these standards without importing their bureaucracy. A small company gets 80% of the assurance for 20% of the overhead — and can scale into formal certification later without rework.
