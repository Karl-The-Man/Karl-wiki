---
type: concept
title: Intelligence Layer
created: 2026-04-11
updated: 2026-04-11
sources: [From Hierarchy to Intelligence.md]
tags: [concept, organizational-design, ai-native, architecture]
---

# Intelligence Layer

The AI system that composes atomic capabilities into solutions for specific customers at specific moments, delivering them proactively. Introduced by [[Jack Dorsey]] in [[From Hierarchy to Intelligence]] as the third layer of [[Block]]'s [[Company as Intelligence]] architecture.

## What It Does

The intelligence layer sits between raw capabilities and customer-facing interfaces. It uses the [[World Model (Organizational)|world model]] to recognize customer moments and compose appropriate responses from available capabilities — without a product manager deciding to build that specific solution.

### Examples from the Source

**Merchant example:** A restaurant's cash flow is tightening ahead of a seasonal dip the model has seen before. The intelligence layer composes a short-term loan (lending capability), adjusts the repayment schedule (payments capability), and surfaces it to the merchant before they even think to look for financing.

**Consumer example:** A Cash App user's spending pattern shifts in a way the model associates with a move to a new city. The intelligence layer composes a new direct deposit setup, a Cash App Card with boosted categories for their new neighborhood, and a savings goal calibrated to their updated income.

> "No product manager decided to build either solution. The capabilities existed. The intelligence layer recognized the moment and composed them."

## Failure Signal as Roadmap

One of the most powerful ideas in [[From Hierarchy to Intelligence]]:

> "When the intelligence layer tries to compose a solution and can't because the capability doesn't exist, that failure signal is the future roadmap."

Traditional roadmaps are built by PMs hypothesizing about what to build next. In this model, customer reality generates the backlog directly. The gap between what the intelligence layer *wants* to compose and what it *can* compose is the most honest prioritization mechanism possible.

> "The traditional roadmap, where product managers hypothesize about what to build next, is any company's ultimate limiting factor."

## Position in the Architecture

1. **Capabilities** — atomic primitives (payments, lending, banking, etc.)
2. **[[World Model (Organizational)|World Model]]** — company + customer understanding
3. **Intelligence Layer** ← this — composes capabilities using the world model
4. **Interfaces** — delivery surfaces (Square, Cash App, etc.)

## Relationship to Agents

The intelligence layer is conceptually related to [[Claws]] and autonomous agents in the individual workflow context. Both represent AI systems that act proactively rather than waiting for human instruction:

- **Individual level:** [[Claws]] loop autonomously, managing tasks without human involvement ([[Andrej Karpathy]])
- **Organizational level:** the intelligence layer composes solutions for customers without PM involvement ([[Jack Dorsey]])

## Open Questions

- What governance layer ensures the intelligence layer doesn't compose harmful solutions?
- How does the intelligence layer handle novel situations where the world model has no precedent?
- What's the boundary between "proactive composition" and "unwanted financial product pushing"?

## Related

- [[Company as Intelligence]] — the organizational thesis
- [[World Model (Organizational)]] — what feeds the intelligence layer
- [[Block]] — the company building this
- [[Hierarchy as Information Routing]] — what the intelligence layer replaces at the coordination level
