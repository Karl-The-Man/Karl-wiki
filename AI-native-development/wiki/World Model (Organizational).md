---
type: concept
title: "World Model (Organizational)"
created: 2026-04-11
updated: 2026-04-11
sources: [From Hierarchy to Intelligence.md]
tags: [concept, organizational-design, ai-native]
---

# World Model (Organizational)

A continuously updated AI-maintained representation of a company's operations and its customers, replacing the contextual knowledge that managers traditionally carry. Introduced by [[Jack Dorsey]] in [[From Hierarchy to Intelligence]] as a foundation of the [[Company as Intelligence]] model at [[Block]].

## Two Sides

### Company World Model

How the company understands itself: what's being built, what's blocked, where resources are allocated, what's working and what isn't. In a traditional company, this picture exists in the heads of managers and is relayed through status meetings, alignment sessions, and reporting chains. In the AI-native model, the system maintains it continuously.

**Prerequisite:** remote-first work culture where everything creates machine-readable artifacts. Decisions, discussions, code, designs, plans, problems, and progress all exist as recorded actions.

> "In a traditional company, a manager's job is to know what's happening across their team and relay that context up and down the chain. In a remote-first company where work is already machine-readable, AI can build and maintain that picture continuously."

### Customer World Model

A per-customer, per-merchant, per-market representation built from proprietary data. In Block's case, this is financial behavior observed through transaction data from both sides of every transaction (buyer via Cash App, seller via Square).

**Why financial data:** "People lie on surveys. They ignore ads. They abandon carts. But when they spend, save, send, borrow, or repay, that's the truth. Every transaction is a fact about someone's life."

**Flywheel:** richer signal → better model → more transactions → richer signal. The understanding compounds.

**Evolution path:** starts with raw transaction data, evolves toward full causal and predictive models over time.

## Role in the Architecture

The world model is the second of four layers in Block's [[Company as Intelligence]] architecture:

1. Capabilities (atomic primitives)
2. **World Model** ← this
3. [[Intelligence Layer]] (composes capabilities using the world model)
4. Interfaces (delivery surfaces)

The world model feeds the [[Intelligence Layer]], which uses it to recognize customer moments and compose appropriate solutions from available capabilities.

## Relationship to Management

The company world model directly replaces the information-carrying function of middle management:

- **Traditional:** manager knows what's happening → relays context up and down → coordinates across teams
- **World model:** system knows what's happening → provides context to ICs directly → DRIs coordinate using the model

This is why Block's structure has no permanent middle management layer. The world model "handles alignment."

## Generalizability

The *company* world model generalizes well — any remote-first organization producing machine-readable artifacts has the raw material. The *customer* world model is more domain-specific: Block's version is powered by uniquely rich two-sided transaction data. Companies in other domains would need equivalently honest, high-frequency customer signals.

## Related

- [[Company as Intelligence]] — the organizational thesis this enables
- [[Intelligence Layer]] — what consumes the world model
- [[Hierarchy as Information Routing]] — the problem the world model solves
- [[Block]] — the company building this
