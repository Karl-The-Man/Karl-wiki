---
type: concept
title: Thin Harness, Fat Skills
created: 2026-04-13
updated: 2026-04-13
sources: [Thin Harness, Fat Skills.md]
tags: [architecture, principle, agents, skills]
---

# Thin Harness, Fat Skills

An architectural principle for building AI agent systems, articulated by [[Garry Tan]]. The claim: the productivity gap between 2x and 100x AI users is not about model intelligence — it's about where you put the value. The answer: **push intelligence up into skills, push execution down into deterministic tooling, keep the harness thin.**

## The Three Layers

| Layer | What It Does | Characteristics |
|---|---|---|
| **[[Skill Files]]** (top) | Encode judgment, process, domain knowledge | Markdown procedures. Reusable. Parameterized. Where 90% of value lives |
| **Harness** (middle) | Runs model in loop, file I/O, context management, safety | ~200 lines. JSON in, text out. Read-only by default |
| **Application** (bottom) | Deterministic execution | SQL, compiled code, arithmetic. Same input → same output. Always |

The principle is directional. Every improvement to the model automatically improves every skill (the latent steps get smarter), while the deterministic layer stays perfectly reliable.

## The Anti-Pattern: Fat Harness, Thin Skills

What Tan warns against:

- 40+ tool definitions eating half the context window
- God-tools with 2-to-5-second MCP round-trips
- REST API wrappers that turn every endpoint into a separate tool
- Three times the tokens, three times the latency, three times the failure rate

The fix: purpose-built tooling that's fast and narrow. A Playwright CLI at 100ms per browser operation, not a Chrome MCP at 15 seconds for a screenshot-find-click-wait-read cycle.

## Contrast with "Your Harness, Your Memory"

This is the central tension in the wiki's architecture debate.

| | [[Your harness, your memory (Harrison Chase)\|Harrison Chase]] | [[Garry Tan]] |
|---|---|---|
| **Where value lives** | In the harness (memory, context management) | In the skills (markdown procedures) |
| **Harness size** | 512k lines is evidence harnesses are permanent | ~200 lines; harness should be thin |
| **Lock-in concern** | Closed harnesses trap your [[Agent Memory\|memory]] | Skills are portable markdown — lock-in is less relevant |
| **Key risk** | [[Memory Lock-In]] | Fat harnesses that bloat context and latency |

> [!warning] The paradox
> Tan himself uses [[Claude Code]] (512k lines) as his harness. The resolution: the 200-line figure describes the *user-built* harness layer. Claude Code is infrastructure beneath it. The question is whether your *custom value* lives in portable skill files or in the harness's proprietary memory system.

Both agree on one thing: the harness layer is permanent and important. They disagree on its optimal thickness and where the defensible value should accumulate.

## Why Skills Compound

- Skills never degrade, never forget
- They run at 3 AM on a cron while you sleep
- When the next model drops, every skill instantly improves — latent steps get smarter, deterministic steps stay reliable
- Skills can [[Thin Harness, Fat Skills (Garry Tan)#The YC Startup School Case Study|rewrite themselves]] through feedback loops

> Every skill you write is a permanent upgrade to your system.

## Related Concepts

- [[Skill Files]] — the "fat" layer
- [[Resolvers]] — context routing that keeps the harness thin
- [[Latent vs Deterministic]] — the design boundary between layers
- [[Diarization]] — a canonical skill pattern
- [[Agent Harness]] — the "thin" layer
- [[Memory Lock-In]] — the competing concern from Chase
- [[The Bitter Lesson]] — let the model do its thing; skills enable this
- [[Claws]] — skills on cron are claws by another name
