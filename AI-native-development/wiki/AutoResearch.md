---
type: concept
title: AutoResearch
created: 2026-04-11
updated: 2026-04-11
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [research, automation, agents, ml-training]
---

# AutoResearch

[[Andrej Karpathy]]'s paradigm for fully autonomous ML experimentation. The core idea: define an objective metric, set boundaries, and let agents run indefinitely without human involvement.

> "I don't want to be the researcher in the loop looking at results, etc. I'm holding the system back. So the question is: how do I refactor all the abstractions so that I'm not?"

## How It Works

1. Define an **objective** (e.g., minimize validation loss)
2. Define a **metric** for evaluation
3. Define **boundaries** — what the agent can and cannot modify
4. Hit go. The agent loops: try idea → evaluate → keep/discard → try next idea.

## Results on NanoGPT

Karpathy had hand-tuned [[NanoGPT]] extensively — "I've trained these models thousands of times. I have some amount of earned confidence." Then AutoResearch ran overnight and found:

- **Weight decay on value embeddings** was wrong
- **Adam betas** were not sufficiently tuned
- These parameters **jointly interact** — once you tune one, others need to change

> "I was surprised that it found these things in a repo that was already fairly well tuned."

## program.md

The instructions that define how an auto researcher should work live in a file called `program.md` — Karpathy's "crappy attempt at describing how the auto researcher should work."

Key insight: **a research organization is a set of markdown files** that describe roles, connections, and procedures. Different program.mds produce different research outcomes. This is itself optimizable — see [[Recursive Self-Improvement]].

Contest idea: let people write different program.mds for the same hardware, measure improvement, then feed the results to a model to write a better program.md. "There's no way we don't get something better."

## Caveats

1. **Requires objective metrics.** If you can't evaluate, you can't auto-research. Perfect fit: CUDA kernel optimization, hyperparameter tuning. Bad fit: anything soft or subjective.
2. **Models are still rough.** Karpathy describes [[Jaggedness]] — brilliant in verifiable domains, struggling with nuance, intent, and when to ask clarifying questions.
3. **Goodharting risk.** An autonomous loop will overfit to its metrics. Mitigation: use the system to devise more metrics with better coverage.

## Scaling: From Single Loop to Swarm

The single-loop version (one agent trying things in sequence) is just the start:

- **Parallelization:** Multiple auto researchers talking through a common system
- **[[Distributed Auto Research]]:** Untrusted workers on the internet contributing compute, like SETI@home
- **Meta-optimization:** Optimizing the program.md itself; having multiple "research organizations" compete

## Implications for Frontier Labs

> "The most interesting project, and probably what the frontier labs are working on, is: you experiment on the smaller models, you try to make it as autonomous as possible, remove researchers from the loop — they have way too much confidence, and they shouldn't be touching any of this really."

The vision: researchers contribute ideas to a queue, automated workers pull and test them, successful experiments land on a feature branch, humans occasionally review and merge. This is [[Recursive Self-Improvement]] in practice.

## Related Concepts

- [[Recursive Self-Improvement]] — the broader concept AutoResearch instantiates
- [[Distributed Auto Research]] — the scaled, decentralized version
- [[NanoGPT]] — the testbed
- [[Token Throughput]] — AutoResearch is the ultimate throughput maximizer
- [[Skill Issue]] — "researchers have way too much confidence"
- [[Claws]] — AutoResearch is a specialized claw
