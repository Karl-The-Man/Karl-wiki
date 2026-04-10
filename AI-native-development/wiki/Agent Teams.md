---
type: entity
title: Agent Teams
created: 2026-04-10
updated: 2026-04-11
sources: [Building-Claude-Code-with-Boris-Cherny.md, Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [tool, anthropic, swarms, agentic-ai]
---

# Agent Teams

**[[Anthropic]]**'s implementation of agent swarms — multiple agents with [[Uncorrelated Context Windows]] working together on complex tasks. A feature of [[Claude Code]].

## How It Works

- Multiple sub-agents are spawned, each with a **fresh context window** that doesn't know what's in the parent context
- This "uncorrelated context windows" design yields better results than correlated context for complex tasks
- This is a form of **test-time compute** — throwing more tokens at a problem through independent perspectives
- The feature clicked specifically with **Opus 4.6**

## The Plugins Story

The most dramatic example of Agent Teams in action: engineer Daisy set up a container with Claude in "dangerous mode," let it run for an entire weekend:

> "[Daisy] set up a container and she set up Claude in dangerous mode. And she let it run for the entire weekend. It spawned a couple hundred agents. They made 100 tasks on the Asana board. And then they implemented it. And that's pretty much the version of plugins that we shipped." — [[Boris Cherny]]

## When to Use

- Best for **complex tasks**, not every task
- Uses a lot of tokens
- Implementation can be as simple as asking Claude to "start three agents to do this"
- Also used with [[Best of N]] for higher determinism: parallel agents + deduplication agents checking for false positives

## External Validation: Karpathy's Parallel Agents

[[Andrej Karpathy]] independently converged on the same pattern outside Anthropic — running multiple agents ([[Claude Code]], [[Codex]]) in parallel, assigning whole functionalities as [[Macro Actions]]. His workflow differs in tooling (uses Codex alongside Claude Code) but matches the core principle: human as orchestrator of parallel agent streams. [[Peter Steinberger]] takes this further with a tiled monitor of many simultaneous [[Codex]] agents.

Karpathy also envisions the next level: [[Distributed Auto Research]], where parallel agents collaborate asynchronously at internet scale.

## Relationship to Other Concepts

- Implements the principle of [[Uncorrelated Context Windows]]
- Exemplifies [[The Bitter Lesson]] — letting multiple models work independently rather than engineering a sophisticated coordination system
- Related to test-time compute scaling
- [[Macro Actions]] — the granularity at which parallel agents are assigned work
- [[Distributed Auto Research]] — parallel agents scaled to untrusted internet compute
