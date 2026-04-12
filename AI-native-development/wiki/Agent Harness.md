---
type: concept
title: Agent Harness
created: 2026-04-12
updated: 2026-04-12
sources: [Your harness, your memory.md]
tags: [architecture, agents, infrastructure]
---

# Agent Harness

The system that wraps an LLM to make it an agent — managing tool use, context, [[Agent Memory|memory]], permissions, UI, and orchestration. The term is used by [[Harrison Chase]] and the [[LangChain]] ecosystem, but the concept applies universally. An agent, by definition, is an LLM interacting with tools and data sources. The harness is everything that facilitates that interaction.

## Examples of Agent Harnesses

| Harness | Creator | Open Source | Model-Agnostic |
|---|---|---|---|
| [[Claude Code]] | [[Anthropic]] | No | No (Claude only) |
| [[Deep Agents]] | [[LangChain]] | Yes | Yes |
| [[OpenClaw]] / Pi | [[Peter Steinberger]] | Yes | Yes |
| [[Codex]] | [[OpenAI]] | Yes | No (OpenAI only) |
| Letta Code | [[Letta]] | Yes | Yes |
| OpenCode | — | Yes | Yes |

## Why Harnesses Are Permanent

There is a recurring sentiment that models will "absorb" the scaffolding — that as models improve, the harness layer will shrink to nothing. Chase argues this is wrong:

- Old scaffolding gets replaced by *new* scaffolding, not by *no* scaffolding
- Even [[Claude Code]] — built by the makers of the best model — has **512k lines of harness code** (revealed when its source was leaked)
- When "web search is built into the API," it's actually a lightweight harness behind the API orchestrating tool calls — the scaffolding just moved, it didn't disappear

This aligns with [[The Bitter Lesson]] as observed in practice: you need general-purpose tools around the model, and the system managing those tools is the harness.

## The Harness-Memory Relationship

The central thesis from [[Sarah Wooders]] ([[Letta]]) and [[Harrison Chase]]:

> Asking to plug memory into an agent harness is like asking to plug driving into a car.

The harness manages all forms of [[Agent Memory]]:

- **Short-term memory:** messages in the conversation, large tool call results, compaction
- **Long-term memory:** cross-session memory, user preferences, learned behaviors
- **Context loading:** how AGENTS.md / CLAUDE.md files get into the system prompt
- **State decisions:** what survives compaction, what's lost, how interactions are stored

Because memory is inseparable from the harness, choosing a harness is choosing a memory system. See [[Memory Lock-In]].

## The Evolution of Scaffolding

Chase traces three generations, each matching model capability:

1. **RAG chains** (2023) — simple retrieval-augmented generation ([[LangChain]])
2. **Complex flows** — multi-step agentic pipelines (LangGraph)
3. **Agent harnesses** (current) — full agentic loops with tools, memory, and persistence ([[Deep Agents]], [[Claude Code]], [[Codex]])

> [!note] Contrast with Boris Cherny
> [[Boris Cherny]]'s account of [[Claude Code]]'s architecture tells the same evolution story from the inside: it started as "a simple chatbot hitting the API," then adding tool use was the pivotal moment. The harness grew *because* the model became capable enough to use it.

## Related Concepts

- [[Agent Memory]] — inextricably tied to the harness
- [[Memory Lock-In]] — the risk of closed harnesses
- [[The Bitter Lesson]] — the model needs tools and a system to manage them
- [[Claws]] — harnesses taken to their logical conclusion: persistent, autonomous entities
- [[Agentic Search]] — a concrete example of how the harness provides tools to the model
