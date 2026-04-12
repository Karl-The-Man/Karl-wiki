---
type: entity
title: Deep Agents
created: 2026-04-12
updated: 2026-04-12
sources: [Your harness, your memory.md]
tags: [tool, agent-harness, open-source, langchain]
---

# Deep Agents

[[LangChain]]'s open-source [[Agent Harness]], positioned as the open alternative to closed systems like [[Claude Agent SDK]] and [[Codex]].

## Key Properties

- **Open source** — full code visibility and modifiability
- **Model agnostic** — not locked to any single model provider
- **Open standards** — uses agents.md and skills specifications
- **Pluggable memory** — integrations with MongoDB, Postgres, Redis for storing [[Agent Memory]]
- **Deployable** — via LangSmith Deployment (self-hostable, any cloud, bring your own database) or behind any standard web hosting framework

## Why It Exists

[[Harrison Chase]] argues that [[Memory Lock-In]] is the dominant risk in the agent ecosystem. Model providers ([[Anthropic]], [[OpenAI]]) are incentivized to pull memory behind their APIs because memory creates stickier lock-in than the model itself. Deep Agents is the structural response: if the harness is open and the memory store is yours, you maintain ownership of the proprietary dataset that makes your agent valuable.

## In Context

Deep Agents represents [[LangChain]]'s third generation of tooling:
1. **LangChain** (2023) — RAG chains
2. **LangGraph** — complex agentic flows
3. **Deep Agents** — full agent harness for the current era

## Related Pages

- [[LangChain]] — parent company
- [[Harrison Chase]] — creator/advocate
- [[Agent Harness]] — the architectural pattern
- [[Memory Lock-In]] — the problem it addresses
- [[Claude Code]] — competitor (closed)
- [[Codex]] — competitor (open source, but encrypted compaction)
- [[OpenClaw]] — cited alongside as an example harness
