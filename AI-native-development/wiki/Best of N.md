---
type: concept
title: Best of N
created: 2026-04-10
updated: 2026-04-10
sources: [Building-Claude-Code-with-Boris-Cherny.md]
tags: [technique, determinism, agentic-ai]
---

# Best of N

A technique for increasing determinism in non-deterministic LLM outputs. Launch **N parallel agents** for the same task, then deduplicate or compare results to identify the correct answer and filter out false positives.

## How It Works

In [[Claude Code]], implementation is straightforward: ask Claude to "start three agents to do this." The framework spawns parallel agents with [[Uncorrelated Context Windows]], each working independently. A deduplication agent then checks for consistency across results.

Used by the [[Claude Code]] team to reduce false positives in automated code review and testing.

## Relationship to Agent Teams

[[Best of N]] is a simpler application of the same principle behind [[Agent Teams]]: multiple independent agents with uncorrelated context produce more reliable results than a single agent. Where Agent Teams tackle complex multi-part tasks, Best of N applies the pattern to a single task for higher confidence.

## Related Concepts

- [[Uncorrelated Context Windows]] — the underlying principle
- [[Agent Teams]] — the broader swarm implementation
- [[The Bitter Lesson]] — more compute (N agents) beats more engineering
