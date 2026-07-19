# 2 · Data Classification × AI Access

The single most important control in this framework. **What data touches a tool matters more than which tool it is.** Get this table right and most other decisions follow automatically.

## Data tiers

| Tier | Examples | AI handling rule |
|------|----------|------------------|
| **Public** | Published reports, marketing copy, public web data | Any approved tool, including public consumer AI. |
| **Internal** | Internal docs, non-sensitive analytics, meeting notes | Enterprise AI tools only (see below). No public/consumer AI. |
| **Confidential** | Unreleased research, financials, source code, contracts | Enterprise AI with **no-training** guarantee and access controls. Human review of outputs before external use. |
| **Restricted / Regulated** | Customer PII, payment data, anything under GDPR/CCPA/contractual limits | **On-prem / private-tenant models only.** Never sent to a shared or public model. DPIA required. |

## What "approved tool" means by mode

| Tool mode | Data-training? | Max data tier |
|-----------|----------------|---------------|
| **Public / consumer AI** (free ChatGPT, etc.) | Often yes | **Public only** |
| **Enterprise AI** (Copilot, ChatGPT Enterprise, Claude/Gemini enterprise) with signed no-train terms | No (contractually) | **Confidential** |
| **Private-tenant / VPC or on-prem model** | No | **Restricted / Regulated** |

## The rules that fall out of this

1. **Default deny for regulated data on shared models.** If a use case needs Restricted data, it needs a private-tenant or on-prem model — full stop.
2. **Label before you build.** Every use case declares its highest data tier at [intake](06-intake-and-approval.md). That tier sets the tool constraint and the [risk tier](03-risk-tiering.md).
3. **No copy-paste laundering.** Pasting Confidential data into a consumer tool is a data-classification violation regardless of intent.
4. **Retrieval counts.** If a system *retrieves* Restricted data at runtime (RAG), the retrieved data inherits the same rule as if it were in the prompt.

> This table is the thing to tailor first for any given company — swap the examples for that org's real data taxonomy and it becomes immediately actionable.
