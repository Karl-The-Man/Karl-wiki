---
type: concept
title: Token Throughput
created: 2026-04-11
updated: 2026-04-11
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [metric, productivity, ai-native]
---

# Token Throughput

[[Andrej Karpathy]]'s framing of developer productivity in the agent era: your output is a function of how many tokens you can command per second, not how fast you type.

> "What is your token throughput? And what token throughput do you command?"

## The GPU Utilization Analogy

Karpathy draws a direct parallel to his PhD days:

- **Then:** You felt nervous when your GPUs weren't running. Productivity = maximizing available FLOPs.
- **Now:** You feel nervous when your agent subscriptions have unused capacity. Productivity = maximizing available tokens.

The industry had at least 10 years where "people just didn't feel compute-bound." Now everyone feels it again — but it's not compute access that's scarce, it's *your ability to direct the compute*.

## You Are the Bottleneck

The key insight: the binding constraint is **you**, not the machine. If you're waiting for an agent and not spinning up another, you're wasting capacity. This drives:

- Parallel agent sessions ([[Macro Actions]])
- Switching between [[Codex]] and [[Claude Code]] when one subscription runs out
- Persistent autonomous agents ([[Claws]]) that run without your involvement
- [[AutoResearch]] — removing yourself from the loop entirely

## Implications

Token throughput creates a new kind of stress — the awareness that you could always be doing more. See [[AI Psychosis]]. It also creates a new kind of skill — orchestrating many parallel streams of AI work. See [[Skill Issue]].

## Related Concepts

- [[AI Psychosis]] — the emotional experience of maximizing throughput
- [[Skill Issue]] — everything that limits throughput feels like your fault
- [[Macro Actions]] — working at the right granularity to maximize throughput
- [[AutoResearch]] — the ultimate throughput play: remove yourself entirely
