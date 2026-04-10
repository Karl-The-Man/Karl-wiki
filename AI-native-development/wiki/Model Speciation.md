---
type: concept
title: Model Speciation
created: 2026-04-11
updated: 2026-04-11
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [models, architecture, ecosystem, future]
---

# Model Speciation

[[Andrej Karpathy]]'s prediction that AI models will diversify into specialized forms — like species in the animal kingdom — rather than converging on a single "oracle" monoculture.

## The Argument

> "The animal kingdom is extremely diverse in the brains that exist. There are lots of different niches in nature, and some animals have an overdeveloped visual cortex or other parts. I think we should be able to see more speciation."

Current state: labs pursue one massive general-purpose model. Future state: smaller models that retain a "cognitive core" but specialize, becoming more efficient in latency/throughput for specific tasks. Example: a Lean math-specialist model.

## Why It Hasn't Happened Yet

Karpathy identifies several blockers:

1. **Fine-tuning science is immature** — "the science of manipulating the brains is not fully developed yet." Touching weights (vs. context windows) risks breaking the model's general intelligence.
2. **Labs don't know what users will ask** — serving a general model is the safe default when you can't predict use cases.
3. **Monoculture pressure** — even when specialized models are trained (e.g., code models), improvements get merged back into the main model.
4. **Context windows are cheap** — customization via context is easy and risk-free; weight-level customization is hard and risky.

## What Could Trigger Speciation

- **Compute constraints** — if you can't serve a massive model for every use case, efficiency matters, and specialization wins
- **Specific business partnerships** — companies wanting niche capabilities
- **Improved fine-tuning science** — continual learning without catastrophic forgetting

## Open Source as Speciation

Open-source models represent a form of speciation: they lag frontier by ~6–8 months but cover consumer use cases well. Karpathy draws a **Linux analogy** — a common open platform the industry needs, even if it's not at the cutting edge. Frontier closed models handle "Nobel Prize kind of work" or "let's move Linux from C to Rust."

> "I kind of expect that this dynamic will basically continue. We'll have frontier labs that have closed AIs, and then we'll have open source behind by some amount of months."

He considers this dynamic **healthy** and warns about excessive concentration in closed models.

## Related Concepts

- [[Jaggedness]] — the uneven capability profile that motivates speciation
- [[The Bitter Lesson]] — tension: speciation is engineering-heavy, while the Bitter Lesson favors scale
- [[Recursive Self-Improvement]] — frontier models may stay general while specialized models serve niches
