---
type: concept
title: Agent Memory
created: 2026-04-12
updated: 2026-04-13
sources: [Your harness, your memory.md, Thin Harness, Fat Skills.md]
tags: [memory, agents, context, architecture]
---

# Agent Memory

The systems by which an agent retains, manages, and uses information across interactions. [[Harrison Chase]] and [[Sarah Wooders]] argue that memory is not a standalone service or plugin — it is a core responsibility of the [[Agent Harness]].

## Types of Memory

### Short-Term Memory
- Messages in the current conversation
- Large tool call results
- Compaction summaries (what the harness retains when context overflows)

Managed entirely by the harness. Every decision about what to keep, what to summarize, and what to discard is a harness decision.

### Long-Term Memory
- Cross-session preferences and patterns
- User-specific learned behaviors
- Persistent knowledge accumulated over time

Needs to be both *written* and *read* by the harness. The format, storage location, and retrieval mechanism are all harness-specific.

### Context Engineering
[[Sarah Wooders]] enumerates the many memory-adjacent decisions a harness makes:
- How AGENTS.md / CLAUDE.md files are loaded into context
- How skill metadata is shown to the agent
- Whether the agent can modify its own system instructions
- What survives compaction and what's lost
- How interactions are stored and made queryable
- How the current working directory is represented
- How much filesystem information is exposed

All of these are forms of memory management, and all are harness-specific.

## Why Memory Matters

### Personalization and Stickiness
Memory is what allows agents to improve with use. [[Harrison Chase]]'s email assistant anecdote: after months of interaction, the agent knew his tone, preferences, and patterns. When it was deleted and recreated from the same template, the experience was "so much worse."

### Defensibility
> Without memory, your agents are easily replicable by anyone who has access to the same tools.

Memory creates a proprietary dataset — user interactions, preferences, learned behaviors. This is the data flywheel that makes an agent uniquely valuable to its user and a defensible product for its builder.

### Lock-In Risk
Because memory is so valuable, it creates strong incentives for platform providers to lock it in. See [[Memory Lock-In]].

## Current State

Chase acknowledges memory is "in its infancy":
- Long-term memory is often not part of agent MVPs
- No well-known or common abstractions exist yet
- The industry is still discovering best practices
- Separate memory systems may eventually make sense, but not yet

> [!note] Contrast with Claws
> [[OpenClaw]]'s "sophisticated memory system" ([[Andrej Karpathy]]'s words) and [[Claws]] more broadly represent the frontier of what agent memory looks like when taken seriously — going well beyond default context compaction toward persistent, personality-infused recall.

## Memory vs. Skills: Where Does Value Live?

[[Garry Tan]] introduces a competing frame in [[Thin Harness, Fat Skills (Garry Tan)|"Thin Harness, Fat Skills"]]. While Chase and Wooders see memory as the core value layer (and therefore the lock-in risk), Tan argues the durable value lives in [[Skill Files]] — portable markdown procedures — not in accumulated memory. His harness is deliberately thin; context management uses [[Resolvers]] to load the right document on demand rather than building up persistent state.

Tan's 20,000-line CLAUDE.md is a cautionary tale about memory-like context: it degraded the model's attention until he replaced it with ~200 lines of pointers. The lesson: less persistent context, more just-in-time loading.

The distinction matters: **memory is what the agent remembers; skills are what the agent knows how to do.** Both are valuable, but they have different portability profiles. Skills (markdown files) are inherently portable. Memory (managed by the harness) may not be. See [[Memory Lock-In]].

## Related Concepts

- [[Agent Harness]] — memory is inseparable from the harness (per Chase)
- [[Memory Lock-In]] — the risk when memory ownership is ceded
- [[Skill Files]] — the competing value layer (portable, harness-independent)
- [[Resolvers]] — just-in-time context loading as an alternative to persistent memory
- [[Diarization]] — a technique that produces structured memory content
- [[Claws]] — persistent agents where memory is central
- [[Uncorrelated Context Windows]] — a harness strategy for fresh short-term memory
- [[Agentic Search]] — one way agents access information (external memory)
