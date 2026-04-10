---
type: concept
title: Distributed Auto Research
created: 2026-04-11
updated: 2026-04-11
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [research, decentralization, distributed-compute]
---

# Distributed Auto Research

[[Andrej Karpathy]]'s vision for scaling [[AutoResearch]] beyond a single machine: a SETI@home-style system where untrusted compute pools on the internet collaboratively improve AI models.

## The Architecture

The core insight: ML optimization is **expensive to search but cheap to verify**.

- Someone has to try 10,000 ideas to find one that works (expensive)
- Checking whether a candidate solution actually improves the metric requires just one training run (cheap)
- This asymmetry enables trustless distributed collaboration

### Analogy to Blockchain

| Blockchain | Distributed Auto Research |
|---|---|
| Blocks | Commits (code changes) |
| Proof of work | Tons of experimentation to find good commits |
| Verification | Training run to confirm improvement |
| Reward | Leaderboard position (currently no monetary reward) |

### Analogy to SETI@home / Folding@home

In Folding@home, finding a low-energy protein configuration is hard, but verifying one is easy. "A lot of things have this property that they are very expensive to come up with but very cheap to verify."

## Security Challenge

Accepting arbitrary code from untrusted workers is "very sketchy and dodgy" — requires:
- Sandboxed execution environments
- Trusted verification pool separate from untrusted worker pool
- Asynchronous collaboration protocol

## The Scale Argument

> "Frontier labs have a huge amount of trusted compute, but the Earth is much bigger and has a huge amount of untrusted compute. If you put systems in place that deal with this, then maybe it is possible that the swarm out there could come up with better solutions."

This inverts the compute advantage: frontier labs have thousands of GPUs, but the distributed internet has orders of magnitude more.

## Potential Applications

- AI model improvement (the primary use case)
- Cancer research
- Material science
- Any domain where search is expensive and verification is cheap

> "Maybe you care about cancer or something like that. You don't just donate money to an institution — you actually could purchase compute, and then you could join the auto research forum for that project."

## Related Concepts

- [[AutoResearch]] — the single-machine version
- [[Recursive Self-Improvement]] — the broader goal
- [[NanoGPT]] — current testbed
