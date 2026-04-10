---
type: concept
title: Macro Actions
created: 2026-04-11
updated: 2026-04-11
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [workflow, agents, productivity]
---

# Macro Actions

[[Andrej Karpathy]]'s framing for the unit of work in agent-first development: you operate in **whole functionalities**, not lines of code or individual functions.

> "You can move in much larger macro actions. It's not just like, 'Here's a line of code, here's a new function.' It's like, 'Here's a new functionality,' and delegate it to agent one. 'Here's a new functionality that's not going to interfere with the other one,' give it to agent two."

## The Workflow

1. Decompose your goal into independent functionalities
2. Assign each to a separate agent
3. Other agents do research, planning, or parallel tasks
4. Review their work "depending on how much you care about that code"
5. Develop **muscle memory** for this decomposition

> "Everything just happens in these macro actions over your repository, and you're just trying to become really good at it and develop a muscle memory for it."

## Parallel to Boris Cherny's Workflow

This mirrors [[Boris Cherny]]'s practice of running five parallel [[Claude Code]] sessions, round-robining between them — documented in [[AI-Native Workflow]]. Both practitioners independently converged on the same pattern: human as orchestrator of parallel agent streams, working at the level of whole features.

## Key Skill: Decomposition

The new core skill is **identifying independent chunks** that won't interfere with each other. This is a planning/architecture skill, not a coding skill — consistent with the [[Generalist vs Specialist]] thesis that strategic thinking trumps implementation ability.

## Related Concepts

- [[AI-Native Workflow]] — the broader practice context
- [[Token Throughput]] — macro actions maximize token utilization
- [[AI Psychosis]] — the pressure to always be assigning the next macro action
- [[Agent Teams]] — Anthropic's implementation of parallel agents
