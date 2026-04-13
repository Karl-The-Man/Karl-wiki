---
type: concept
title: Resolvers
created: 2026-04-13
updated: 2026-04-13
sources: [Thin Harness, Fat Skills.md]
tags: [architecture, context, routing, agents]
---

# Resolvers

A routing table for context. When task type X appears, load document Y first. Introduced by [[Garry Tan]] as one of the five definitions in the [[Thin Harness, Fat Skills]] architecture.

[[Skill Files]] tell the model *how*. Resolvers tell it *what to load and when*.

## How They Work

A developer changes a prompt. Without the resolver, they ship it. With the resolver, the model reads `docs/EVALS.md` first — which says: run the eval suite, compare scores, if accuracy drops more than 2%, revert and investigate. The developer didn't know the eval suite existed. The resolver loaded the right context at the right moment.

## Claude Code's Built-In Resolver

[[Claude Code]] has a native resolver mechanism: every skill has a `description` field, and the model matches user intent to skill descriptions automatically. You never have to remember that `/ship` exists. The description *is* the resolver.

## The 20,000-Line CLAUDE.md

Tan's cautionary tale:

> My CLAUDE.md was 20,000 lines. Every quirk, every pattern, every lesson I'd ever encountered. Completely ridiculous. The model's attention degraded. Claude Code literally told me to cut it back.

The fix: ~200 lines of pointers. The resolver loads the right document when it matters. Twenty thousand lines of knowledge, accessible on demand, without polluting the context window.

This is resolvers in practice: instead of front-loading all context (which degrades model attention), you create a thin routing layer that loads context just-in-time.

## Relationship to Context Engineering

Resolvers address the same problem [[Sarah Wooders]] ([[Letta]]) identifies as context engineering — how CLAUDE.md files are loaded, what survives compaction, how much filesystem information is exposed. But while Wooders frames this as a core harness responsibility (supporting [[Harrison Chase]]'s thesis that the [[Agent Harness]] is the key layer), Tan frames it as a thin routing layer that keeps the harness deliberately minimal.

## Related Concepts

- [[Skill Files]] — what resolvers route to
- [[Thin Harness, Fat Skills]] — the architecture resolvers enable
- [[Agent Harness]] — where resolvers live
- [[Agentic Search]] — a complementary approach: resolvers load known context; agentic search finds unknown context
