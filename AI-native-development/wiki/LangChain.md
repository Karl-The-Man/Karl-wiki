---
type: entity
title: LangChain
created: 2026-04-12
updated: 2026-04-12
sources: [Your harness, your memory.md]
tags: [company, framework, open-source, agents]
---

# LangChain

AI framework company led by [[Harrison Chase]]. Has evolved through multiple generations of agent-building tools, tracking the capability curve of LLMs.

## Product Evolution

Chase describes three eras of agent scaffolding, each matching model capability:

1. **LangChain** (2023) — simple RAG chains, the first era when ChatGPT launched
2. **LangGraph** — more complex agentic flows as models improved
3. **[[Deep Agents]]** — the current [[Agent Harness]] era, as models became capable enough for full agentic loops

## Current Products

- **[[Deep Agents]]** — open-source, model-agnostic agent harness. The flagship open-source product.
- **LangSmith / Fleet** — enterprise platform for deploying agents (self-hostable, bring your own database). Includes no-code agent building ("Enterprise ready OpenClaws").
- **LangGraph** — graph-based agent orchestration framework

## Position on Open Harnesses

[[LangChain]] is the loudest advocate for [[Agent Harness|open harnesses]] and against [[Memory Lock-In]]. Chase argues that model providers ([[Anthropic]], [[OpenAI]]) are incentivized to lock [[Agent Memory]] behind proprietary APIs, and that the antidote is open-source, model-agnostic infrastructure. This is both a genuine philosophical position and a commercial strategy — LangChain's business depends on the harness layer remaining independent of model providers.

## Related Pages

- [[Harrison Chase]] — CEO
- [[Deep Agents]] — current flagship product
- [[Agent Harness]] — the architectural pattern they advocate
- [[Memory Lock-In]] — the problem they position against
