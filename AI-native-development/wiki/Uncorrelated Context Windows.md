---
type: concept
title: Uncorrelated Context Windows
created: 2026-04-10
updated: 2026-04-10
sources: [Building-Claude-Code-with-Boris-Cherny.md]
tags: [architecture, swarms, test-time-compute]
---

# Uncorrelated Context Windows

The key design principle behind [[Agent Teams]]: sub-agents start with **fresh context windows** that don't know what's in the parent context. This yields better results for complex tasks than sharing context across agents.

## How It Works

When a task is decomposed across multiple agents:
- Each sub-agent begins with a clean context — no knowledge of what other agents are doing or what the parent has seen
- The agents work independently, producing results from different "perspectives"
- Results are then combined, compared, or deduplicated

This is a form of **test-time compute**: throwing more tokens at a problem through independent windows produces better results than a single large context.

## Why It Works

Correlated context windows share biases — if the parent context contains a wrong assumption or a misleading framing, all agents that inherit it will reproduce the error. Uncorrelated windows avoid this by starting fresh, increasing the chance that at least one agent will find the right approach.

This is analogous to ensemble methods in machine learning, where independent models outperform a single model because their errors are uncorrelated.

## Implementation

In [[Claude Code]], implementation can be as simple as asking Claude to "start three agents to do this." The framework handles spawning sub-agents with fresh contexts.

Related technique: [[Best of N]] — launching N parallel agents for the same task and deduplicating results to increase determinism.

## Related Concepts

- [[Agent Teams]] — the feature built on this principle
- [[Best of N]] — a simpler application of the same idea
- [[The Bitter Lesson]] — using more compute (uncorrelated windows) rather than more engineering
