---
type: entity
title: NanoGPT
created: 2026-04-11
updated: 2026-04-11
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [project, karpathy, ml-training, open-source]
---

# NanoGPT

[[Andrej Karpathy]]'s open-source GPT training codebase — a minimal, readable implementation used as a "little playground for training LLMs." The testbed for [[AutoResearch]].

## Role in AutoResearch

Karpathy had hand-tuned NanoGPT extensively using traditional research methods over two decades of experience. He then let [[AutoResearch]] run overnight against it. The autonomous system found improvements he'd missed:

- **Weight decay on value embeddings** was wrong
- **Adam betas** were not sufficiently tuned
- These parameters **jointly interact** — tuning one changes the optimal value of the other

> "I was surprised that it found these things in a repo that was already fairly well tuned."

This result is significant because it demonstrates that autonomous experimentation can surpass expert human tuning, even in a domain where the expert has "earned confidence" from thousands of training runs.

## Related Projects

- [[microGPT]] — Karpathy's even more minimal 200-line implementation (educational focus)
- [[AutoResearch]] — the paradigm that used NanoGPT as its playground
- [[Recursive Self-Improvement]] — the broader concept NanoGPT serves as a testbed for
