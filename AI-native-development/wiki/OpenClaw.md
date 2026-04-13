---
type: entity
title: OpenClaw
created: 2026-04-11
updated: 2026-04-13
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md, Your harness, your memory.md, Thin Harness, Fat Skills.md]
tags: [tool, claw, agents, open-source]
---

# OpenClaw

A [[Claws|claw]] project created by [[Peter Steinberger]]. Praised by [[Andrej Karpathy]] for innovating in multiple dimensions simultaneously.

## Key Innovations

1. **Soul and demeanor document** — a carefully crafted personality for the agent. Karpathy contrasts this with [[Codex]] (which is "very dry" and "doesn't seem to care about what you're creating") and [[Claude Code]] (which "dialed the psychopathy fairly well" with calibrated praise). Peter cares deeply about personality, and Karpathy argues most tools don't appreciate this enough.

2. **Sophisticated memory system** — goes well beyond the default context compaction that standard agents offer. "OpenClaw has a lot more sophisticated memory than what you would get by default."

3. **WhatsApp portal** — a single messaging interface to all automation. Collapses multiple tools and systems into a natural-language conversation.

## As Agent Harness

[[Harrison Chase]] ([[LangChain]]) cites OpenClaw as one of the emerging [[Agent Harness|agent harnesses]], noting it is powered by Pi (the underlying framework). In the context of the [[Memory Lock-In]] debate, OpenClaw represents the open, model-agnostic approach that Chase advocates — in contrast to closed systems like [[Claude Code]] or API-locked systems like Anthropic's Managed Agents.

## Garry Tan's OpenClaw

[[Garry Tan]] also runs an OpenClaw and references it in [[Thin Harness, Fat Skills (Garry Tan)|"Thin Harness, Fat Skills"]]. His instruction to it:

> If I ask you to do something and it's the kind of thing that will need to happen again, you must: do it manually the first time on 3 to 10 items. Show me the output. If I approve, codify it into a [[Skill Files|skill file]]. If it should run automatically, put it on a cron. The test: if I have to ask you for something twice, you failed.

This positions OpenClaw not just as a personal assistant but as a system that compounds — every interaction potentially produces a permanent [[Skill Files|skill]] upgrade.

## Significance

OpenClaw represents what [[Claws]] look like when taken seriously as a paradigm — not just a coding agent, but a persistent entity with personality, memory, and a unified interface. It embodies the next layer up from basic code agents.

## Related Pages

- [[Peter Steinberger]] — creator
- [[Claws]] — the paradigm it implements
- [[Andrej Karpathy]] — commentary source
- [[Codex]] — contrasted for personality
- [[Claude Code]] — contrasted for personality
