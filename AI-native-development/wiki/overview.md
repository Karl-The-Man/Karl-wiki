---
type: overview
title: AI-Native Development — Overview
created: 2026-04-10
updated: 2026-04-10
sources: [Building-Claude-Code-with-Boris-Cherny.md]
tags: [overview]
---

# AI-Native Development — Overview

This wiki tracks the emerging landscape of **AI-native development** — building software, products, workflows, and organizations that are designed from the ground up to leverage AI capabilities.

## Current State

The wiki contains one deeply sourced interview: [[Building Claude Code with Boris Cherny]], a long-form podcast with the creator of [[Claude Code]] at [[Anthropic]]. This source provides the most detailed first-person account available of what a fully AI-native engineering workflow looks like in practice — including concrete numbers (80% of code AI-written, 20–30 PRs/day, zero hand-written code) and architectural decisions (abandoning RAG for [[Agentic Search]], [[Prototyping Over PRDs]]).

## Key Themes

### The workflow is here, and it's radical
[[Boris Cherny]] ships 20–30 PRs daily with zero hand-written code, manages five parallel [[Claude Code]] sessions, and codes from his phone. He uninstalled his IDE. This isn't theoretical — it's his documented daily practice. See [[AI-Native Workflow]].

### Simpler architectures win
The [[Claude Code]] team abandoned RAG in favor of [[Agentic Search]] (grep/glob), embodying [[The Bitter Lesson]]: give the model simple tools and get out of the way. The architecture is described as "very simple" — a query loop, a few tools, a UI, and security code.

### Safety requires layered defense
[[Swiss Cheese Model (Safety)|Swiss cheese model]]: model alignment, runtime classifiers, sub-agent summarization, permission prompts, and VM isolation. No single layer is sufficient. Safety is described as "the most important thing."

### The generalist is ascendant
Strong opinions about languages and frameworks are losing value. [[Generalist vs Specialist|Multi-disciplinary generalists]] who can think across engineering, product, business, and design are rising. [[Anthropic]]'s flat "Member of Technical Staff" title encodes this belief.

### Building replaces specifying
[[Prototyping Over PRDs]]: when building costs near zero, it's faster to make 30 prototypes than to write a requirements document. "We don't really write stuff — we just show."

### The printing press parallel
[[The Printing Press Analogy]]: software engineers are modern scribes; AI is the printing press. Scribes became writers and authors in a vastly larger market. The effects took centuries to fully manifest.

## Key Questions to Explore

- How does Boris's workflow generalize beyond Anthropic? Is this specific to the company that makes the tool?
- What do competing tools (Cursor, Copilot, Windsurf) look like through the same analytical lens?
- How do organizations outside AI labs adopt AI-native workflows?
- What are the failure modes and limits of the AI-native approach?
- How do [[Agent Teams]] and swarms change the economics of software development at scale?

## Thesis (Evolving)

AI-native development is not an incremental improvement to existing workflows — it's a qualitative shift in what developers do. The human role moves from code authorship to direction, judgment, and review. The tools are simple (grep, not RAG); the safety is layered (Swiss cheese, not single-gate); the culture is experimental (prototypes, not PRDs). The historical parallel is the printing press: the skill of "writing" (coding) gets democratized, the market for "literature" (software) explodes, and the practitioners evolve from scribes to authors.
