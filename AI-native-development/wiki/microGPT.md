---
type: entity
title: microGPT
created: 2026-04-11
updated: 2026-04-11
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [project, karpathy, education, ml-training]
---

# microGPT

[[Andrej Karpathy]]'s ~200-line Python implementation that boils LLM training down to its bare algorithmic essence. The "state of the art" of his decade-long obsession with simplifying neural network training.

## What It Contains

In ~200 lines including comments:
- **Dataset handling** — text input
- **Neural network architecture** — ~50 lines
- **Autograd engine** — ~100 lines for backward pass / gradient calculation
- **Adam optimizer** — ~10 lines
- **Training loop** — ties it all together

All real-world training code complexity is "complexity from efficiency" — making things fast. If you don't need speed, the algorithm is surprisingly simple.

## Significance for Education

Karpathy initially planned to make an explanatory video (his traditional approach), but realized this is no longer necessary:

> "I'm not explaining to people anymore. I'm explaining it to agents."

Instead, the code is simple enough that anyone can ask their agent to explain it in various ways, at their level, with infinite patience. Karpathy envisions writing "skills" — curricula that instruct the agent on how to teach the codebase progressively. See [[Education Through Agents]].

Key insight: **agents can't come up with microGPT** — that required Karpathy's years of obsessive simplification. But agents can perfectly explain and teach it once it exists. The human's value is in the "few bits" of creative reduction; everything downstream is the agent's domain.

## Related Pages

- [[NanoGPT]] — the larger, more practical training codebase
- [[Education Through Agents]] — the teaching paradigm microGPT exemplifies
- [[Andrej Karpathy]] — creator
