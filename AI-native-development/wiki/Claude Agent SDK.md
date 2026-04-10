---
type: entity
title: Claude Agent SDK
created: 2026-04-10
updated: 2026-04-10
sources: [Building-Claude-Code-with-Boris-Cherny.md]
tags: [tool, anthropic, sdk]
---

# Claude Agent SDK

**[[Anthropic]]**'s SDK that powers [[Claude Code]]. Also used independently in CI pipelines for automated code review.

## Use in Code Review

At [[Anthropic]], every PR is first reviewed by Claude via the Agent SDK running in CI (referred to internally as "claudep"). This automated review catches approximately **80% of bugs** before a human reviewer sees the code. Claude automatically addresses some review comments; others are left for the human reviewer.

## Relationship to Claude Code

[[Claude Code]] is built on top of the Agent SDK. The SDK provides the underlying agentic capabilities — tool use, context management, conversation loops — while Claude Code adds the terminal UI, permission system, and developer-focused tooling.

## Related Entities

- [[Claude Code]] — the primary consumer of the SDK
- [[Agent Teams]] — swarm orchestration built on SDK primitives
- [[Anthropic]] — the company that develops it
