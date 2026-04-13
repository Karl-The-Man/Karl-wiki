---
type: concept
title: Agent Harness
created: 2026-04-12
updated: 2026-04-13
sources: [Your harness, your memory.md, Thin Harness, Fat Skills.md]
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

## The Thickness Debate

The wiki's central architectural tension: **how thick should the harness be?**

### Chase: The Harness Is the Product

[[Harrison Chase]] points to [[Claude Code]]'s 512k lines as evidence that harnesses are substantial, permanent infrastructure. Memory is inseparable from the harness. Choosing a harness is choosing a memory system. The key political question is ownership: open vs. closed. See [[Memory Lock-In]].

### Tan: Keep the Harness Thin

[[Garry Tan]] argues the opposite: the harness should be ~200 lines. It does four things — runs the model in a loop, reads/writes files, manages context, enforces safety — and nothing else. The value lives in [[Skill Files]] (portable markdown procedures) on top and deterministic tooling on the bottom. See [[Thin Harness, Fat Skills]].

The anti-pattern, per Tan: a fat harness with thin skills. 40+ tool definitions eating half the context window. God-tools with multi-second MCP round-trips. Three times the tokens, latency, and failure rate.

> [!note] The Paradox
> Tan himself uses Claude Code (512k lines) as his harness. The resolution: 200 lines describes the *user-built* harness layer. Claude Code is infrastructure beneath it. The question is whether your custom value should accumulate in portable skill files or in the harness's proprietary memory system.

Both agree: the harness layer is permanent. They disagree on its optimal thickness and where defensible value should accumulate.

## Related Concepts

- [[Agent Memory]] — inextricably tied to the harness (per Chase)
- [[Memory Lock-In]] — the risk of closed harnesses
- [[Thin Harness, Fat Skills]] — the counter-architecture
- [[Skill Files]] — where value lives in Tan's model
- [[Resolvers]] — context routing that keeps the harness thin
- [[The Bitter Lesson]] — the model needs tools and a system to manage them
- [[Claws]] — harnesses taken to their logical conclusion: persistent, autonomous entities
- [[Agentic Search]] — a concrete example of how the harness provides tools to the model
