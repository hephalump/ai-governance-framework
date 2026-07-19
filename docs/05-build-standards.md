# 5 · Build Standards (Lifecycle Guardrails)

For anyone building an AI system above self-serve (T1/T2). These are the concrete, buildable controls — each maps to a [NIST AI RMF](../STANDARDS-MAPPING.md) function. The companion [reference implementation](https://github.com/yourusername/vendor-maintenance-parser) demonstrates all of them.

## MAP — before you build

- **Write the spec.** What decision does this support? Who's affected if it's wrong? What's the [risk tier](03-risk-tiering.md) and [data tier](02-data-classification.md)?
- **Define "good."** State the accuracy/quality bar *up front* (e.g., "≥95% field-level extraction; no silent errors — low confidence routes to a human"). If you can't define success, you can't ship.

## MEASURE — prove it works

- **Build an eval set.** A representative, labeled test set — including the hard and adversarial cases. This is non-negotiable for T1/T2.
- **Report the number.** Accuracy/precision/recall against the bar, plus known failure modes. This is what makes AI *board-reportable* instead of vibes-based.
- **Red-team untrusted input.** If the system ingests external content (email, documents, web), test for prompt injection and data exfiltration. Treat all input as hostile.
- **Test for bias** where people are affected (disparate performance across groups).

## MANAGE — run it safely

- **Human-in-the-loop, confidence-gated.** Consequential outputs require human approval; low-confidence results route to review, never to silent action.
- **Fail safe.** Define the safe default when the model is unavailable or unsure. (In the reference implementation: it only ever *unlocks* — a fault can't take a worse action.)
- **Log everything.** Inputs, outputs, confidence, and the human decision — an auditable trail per [incident response](07-incident-response.md).
- **Monitor for drift.** Track quality in production; alert when it degrades. Re-run the eval on a schedule.
- **Publish a [system card](../templates/system-card.md)** and keep it current.

## GOVERN — the wrapper

- Named owner, documented approval at the right [tier](03-risk-tiering.md), and a scheduled review date. No orphaned systems.

> **The one-line test:** *Can you state your accuracy number, show your human-in-the-loop step, and name the owner?* If yes, you've met the spirit of these standards.
