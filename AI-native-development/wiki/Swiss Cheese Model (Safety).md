---
type: concept
title: Swiss Cheese Model (Safety)
created: 2026-04-10
updated: 2026-04-10
sources: [Building-Claude-Code-with-Boris-Cherny.md]
tags: [safety, security, agentic-ai]
---

# Swiss Cheese Model (Safety)

The safety philosophy used by [[Claude Code]] and [[Claude Co-Work]]: no single safety mechanism is sufficient. Multiple overlapping layers each catch different failure modes, and the probability of catching issues goes up with more layers. [[Boris Cherny]] frames safety thinking in terms of "counting nines."

## Layers in Claude Code

1. **Model-level alignment** — Opus 4.6 described as "the most aligned model ever released"
2. **Runtime classifiers** — block suspicious requests in real-time
3. **Sub-agent summarization** — web fetch results are summarized by a sub-agent before returning to the main agent, preventing prompt injection from external content
4. **Permission prompts** — asking the human when uncertain (in the product since the very first version, September 2024)
5. **Restricted tool allowlists** — few Unix utilities are pre-allowed because even `find` and `sed` can execute arbitrary code

## Additional Layers for Co-Work

[[Claude Co-Work]] adds extra layers for non-technical users who may not recognize risky operations:

- **Virtual machine isolation** — Claude runs in a VM, not directly on the user's machine
- **Additional classifiers** beyond Claude Code's baseline
- **OS-level integrations** to prevent accidental file deletion
- **Chrome extension permission model** for web interactions

## Design Philosophy

> "Safety... it was kind of an important thing for me. Now it's just the most important thing for me — how do we make sure this thing goes well." — [[Boris Cherny]]

The Swiss cheese metaphor: each layer has holes (failure modes), but stacking layers makes it unlikely that holes align. This is borrowed from aviation and nuclear safety, applied to agentic AI.

The external release of Claude Code was itself driven by [[Anthropic]]'s safety mission — observing real user behavior in the wild makes models safer than lab testing alone.

## Related Concepts

- [[Claude Code]] — the primary tool implementing this model
- [[Claude Co-Work]] — extends it with additional layers for non-engineers
- [[Agent Teams]] — safety considerations scale with agent autonomy
