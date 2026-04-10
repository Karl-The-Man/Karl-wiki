---
type: concept
title: Recursive Self-Improvement
created: 2026-04-11
updated: 2026-04-11
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [research, frontier-labs, meta-optimization]
---

# Recursive Self-Improvement

The idea that LLMs can improve LLMs — and that this is the core game all frontier labs are playing. [[Andrej Karpathy]] frames his [[AutoResearch]] work as a "little playpen" for this concept.

> "Fundamentally, what I'm more interested in is this idea of recursive self-improvement, and to what extent you can actually have LLMs improving LLMs. Because I think all the frontier labs — this is the thing, for obvious reasons — and they're all trying to recursively self-improve, roughly speaking."

## Layers of Recursion

1. **Single loop:** One agent tries experiments in sequence, keeping what works ([[AutoResearch]])
2. **Parallel loops:** Multiple auto researchers working through a common system
3. **Meta-optimization:** Optimizing the `program.md` that defines how the auto researcher works
4. **Research org as code:** "A research organization is a set of markdown files" — different orgs (more risk-taking, fewer standups, different strategies) can compete
5. **Optimization over optimization:** Having a model analyze which program.mds produced the best results and write a better one

## The Vision for Frontier Labs

> "The most interesting project: you experiment on the smaller models, you try to make it as autonomous as possible, remove researchers from the loop — they have way too much confidence."

The workflow:
- Researchers (or automated scientists scanning papers and GitHub) contribute **ideas** to a queue
- Automated **workers** pull items and try them
- Successful experiments land on a **feature branch**
- Humans occasionally **monitor and merge** to main

Scaling laws let you extrapolate from smaller models to frontier-scale training.

## The Candid Admission

Karpathy, while at [[OpenAI]]:

> "You guys realize if we're successful, we're all out of job. We're just building automation for Sam or something like that."

Frontier lab researchers are "automating themselves away actively."

## Related Concepts

- [[AutoResearch]] — the concrete implementation
- [[Distributed Auto Research]] — the decentralized version
- [[NanoGPT]] — the testbed for recursive self-improvement experiments
- [[The Bitter Lesson]] — recursive self-improvement is the Bitter Lesson applied to AI research itself
