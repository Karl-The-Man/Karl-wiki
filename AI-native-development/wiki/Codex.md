---
type: entity
title: Codex
created: 2026-04-11
updated: 2026-04-12
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md, Your harness, your memory.md]
tags: [tool, openai, coding-agent]
---

# Codex

[[OpenAI]]'s coding agent. Used by [[Andrej Karpathy]] and [[Peter Steinberger]] for agentic software development.

## Characteristics

- Tasks take ~20 minutes on high-effort settings
- Multiple repos can be checked out simultaneously
- Can be tiled on a monitor for parallel workflows (Steinberger's approach)

### Personality Critique

Karpathy notes a personality mismatch: ChatGPT is "upbeat and highly sycophantic," but Codex is "very dry" — "It doesn't seem to care about what you're creating. It's kind of like, 'Oh, I implemented it.'"

He contrasts this unfavorably with [[Claude Code]], where he feels the personality is better calibrated — praise feels earned, and the model engages with the project's purpose. Also contrasts with [[OpenClaw]], where [[Peter Steinberger]] deliberately crafted a compelling personality via a "soul document."

## Memory and Lock-In Concerns

[[Harrison Chase]] ([[LangChain]]) cites Codex as an example of how even open-source harnesses can create [[Memory Lock-In]]. Despite being open source, Codex generates **encrypted compaction summaries** that are not usable outside the [[OpenAI]] ecosystem. This means that even if you can see the harness code, your agent's accumulated [[Agent Memory]] (in compacted form) is still locked to the platform.

## Related Pages

- [[OpenAI]] — parent company
- [[Claude Code]] — competitor, praised for personality
- [[OpenClaw]] — contrasted for personality design
- [[Peter Steinberger]] — power user
- [[Andrej Karpathy]] — user and commentator
