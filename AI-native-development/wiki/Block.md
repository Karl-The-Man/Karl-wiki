---
type: entity
title: Block
created: 2026-04-11
updated: 2026-04-11
sources: [From Hierarchy to Intelligence.md]
tags: [company, fintech, organizational-design]
---

# Block

Fintech company (formerly Square) led by [[Jack Dorsey]]. Products include Square (merchant payments), Cash App (consumer finance), Afterpay (BNPL), TIDAL, bitkey, and proto.

## Significance for AI-Native Development

Block is the most prominent example of a company attempting to **redesign its entire organizational structure around AI** — not just giving employees AI copilots, but replacing the management hierarchy itself with AI-coordinated intelligence. Described in [[From Hierarchy to Intelligence]].

## Architectural Vision

Block's model has four layers:

1. **Capabilities** — atomic financial primitives (payments, lending, card issuance, banking, BNPL, payroll). No UIs. Hard to acquire and maintain. These are building blocks, not products.
2. **[[World Model (Organizational)|World Model]]** — two sides: a *company world model* (how Block understands its own operations) and a *customer world model* (per-customer, per-merchant financial reality from transaction data)
3. **[[Intelligence Layer]]** — composes capabilities into solutions for specific customers at specific moments, delivered proactively
4. **Interfaces** — delivery surfaces (Square, Cash App, Afterpay, etc.) through which composed solutions reach customers

## Structural Advantages

- **Remote-first** — all work produces machine-readable artifacts, providing raw material for the company world model
- **Two-sided transaction data** — sees both buyer (Cash App) and seller (Square), creating a uniquely rich customer signal
- **Financial data as honest signal** — "People lie on surveys. They ignore ads. They abandon carts. But when they spend, save, send, borrow, or repay, that's the truth."

## Three Roles (Replacing Hierarchy)

- **ICs** — deep specialists who build and operate capabilities, the model, the intelligence layer, and interfaces. The world model provides context that a manager used to provide.
- **DRIs (Directly Responsible Individuals)** — own cross-cutting problems or customer outcomes for ~90 days with authority to pull resources across teams
- **Player-coaches** — combine building with developing people. Replace traditional managers whose primary job was information routing.

No permanent middle management layer.

## Status

"In the early stages of this transition" as of March 2026. Dorsey acknowledges "parts of it will likely break before they work."

## Related

- [[Jack Dorsey]] — co-founder and head of Block
- [[Company as Intelligence]] — the organizational thesis
- [[From Hierarchy to Intelligence]] — the source document
- [[Hierarchy as Information Routing]] — the problem Block is solving
