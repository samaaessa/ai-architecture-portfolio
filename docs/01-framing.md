# Session 1 – Governance Pack: Marketing Automation with AI & Agents

> **Status: work in progress.** P2 and P3 are done. P1, P4, the ADRs, the ARB checklist and the diagram are still to do.

The principles, decisions and review checklist our Architecture Review Board (ARB) uses before this system goes live. Goals G1–G4 are defined in the [README](../README.md#business-goals).

## 1. Architecture principles

### P1 – Success metrics are agreed before we build *(draft)*
- **Goal:** G1 Grow campaign revenue
- **Why:** _to do_
- **Implication:** _to do_
- **Open questions:**
  - How do we prove extra revenue came from AI-written campaigns and not from the season? Compare with last year, or keep a holdout group in every campaign?
  - Do we measure only before launch and each season, or also every time a prompt or model changes?
  - Finish: "We don't launch an AI-written campaign unless ___ and ___." (two things we can measure)

### P2 – Agents draft, adapt and analyse; people choose the audience, approve and send
- **Goal:** G2 Launch campaigns faster, G3 Keep customer trust
- **Why:** Sending is unrecoverable: if an agent sends without human review, one mistake reaches 2 million customers at once and can't be undone, damaging our brand image.
- **Implication:** Agents have no access to the send function; they can only save drafts. A marketer reviews the drafts and sends the approved ones from the campaign tool.

### P3 – We never move personal customer data out of the customer's country
- **Goal:** G3 Keep customer trust and comply in both countries
- **Why:** If customer data leaks, we lose customer trust and face fines, and even prison, under both countries' data protection laws.
- **Implication:** Agents only see groups and totals, never individual customers. Every prompt passes through a guardrail that blocks any PII before it reaches the model. Customer data stays in a data centre in its own country.

### P4 – Cost *(to do)*
- **Goal:** G4 Keep AI cost predictable
- **Note:** "Use open-source models" is a decision, not a principle, so it moves to ADR-0001 as one of the options.
- **Open question:** What rule keeps AI cost predictable whichever model we choose, API or open-source?

## 2. Architecture decisions *(to do)*
Three ADRs in [adr/](../adr/), each with options, trade-offs and the decision, linked to the principles above.
- ADR-0001: managed LLM API vs self-hosted open-source model (from the P4 discussion)
- ADR-0002: _to choose_ (e.g. vector database)
- ADR-0003: _to choose_ (e.g. real-time vs batch generation)

## 3. ARB checklist *(to do)*
Checks, each with the evidence it needs, for security, privacy (PDPL in Egypt and Saudi Arabia), evals, cost and human oversight.

## 4. Diagram *(to do)*
One draw.io diagram in [diagrams/](../diagrams/), exported as PNG next to its `.drawio` source.

## 5. Automated guardrail *(optional, to do)*
A CI check, or an agent that reviews a design against the principles.
