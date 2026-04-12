---
type: entity
title: Claude Agent SDK
created: 2026-04-10
updated: 2026-04-12
sources: [Building-Claude-Code-with-Boris-Cherny.md, Your harness, your memory.md]
tags: [tool, anthropic, sdk]
---

# Claude Agent SDK

**[[Anthropic]]**'s SDK that powers [[Claude Code]]. Also used independently in CI pipelines for automated code review.

## Use in Code Review

At [[Anthropic]], every PR is first reviewed by Claude via the Agent SDK running in CI (referred to internally as "claudep"). This automated review catches approximately **80% of bugs** before a human reviewer sees the code. Claude automatically addresses some review comments; others are left for the human reviewer.

## Relationship to Claude Code

[[Claude Code]] is built on top of the Agent SDK. The SDK provides the underlying agentic capabilities — tool use, context management, conversation loops — while Claude Code adds the terminal UI, permission system, and developer-focused tooling.

## External Criticism: Closed Harness

[[Harrison Chase]] ([[LangChain]]) cites the Claude Agent SDK as a "Level 2" [[Memory Lock-In]] risk — a closed [[Agent Harness]] that interacts with [[Agent Memory]] in unknown, non-transferable ways. Because it uses [[Claude Code]] under the hood (which is not open source), Chase argues that any memory artifacts it creates are opaque: "What is the shape of those, and how should a harness use those? That is unknown, and therefore non-transferable from one harness to another."

## Related Entities

- [[Claude Code]] — the primary consumer of the SDK
- [[Agent Teams]] — swarm orchestration built on SDK primitives
- [[Anthropic]] — the company that develops it
