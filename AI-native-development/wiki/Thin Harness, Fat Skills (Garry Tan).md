---
type: source-summary
title: "Thin Harness, Fat Skills (Garry Tan)"
created: 2026-04-13
updated: 2026-04-13
sources: [Thin Harness, Fat Skills.md]
tags: [architecture, skills, harness, agents, yc]
---

# Thin Harness, Fat Skills (Garry Tan)

**Source:** Long-form post by [[Garry Tan]], president of Y Combinator, published 2026-04-11 via X. Opens with a [[Steve Yegge]] quote claiming AI coding agent users are "10x to 100x as productive as engineers using Cursor and chat today, and roughly 1000x as productive as Googlers were back in 2005."

## Summary

Argues that the productivity gap between 2x and 100x AI users is not about model intelligence — it's about **architecture**. The 2x people and the 100x people use the same models. The difference is the wrapper: what Tan calls the [[Agent Harness|harness]]. He proposes a specific architecture — [[Thin Harness, Fat Skills]] — built on five definitions: [[Skill Files]], the harness, [[Resolvers]], [[Latent vs Deterministic]], and [[Diarization]]. Illustrates all five working together in a detailed case study of YC's Startup School matching system. Claims skills are "permanent upgrades" that compound over time, improve automatically with each new model, and can rewrite themselves through feedback loops.

## Key Claims

- **The productivity multiplier is architectural, not model-dependent.** Same models, radically different outcomes. The wrapper — the harness — is the secret. (Confirmed by reading [[Claude Code]]'s leaked 512k-line source.)
- **The harness should be thin (~200 lines).** It does four things: runs the model in a loop, reads and writes files, manages context, enforces safety. That's it.
- **The value lives in fat skills.** [[Skill Files]] are reusable markdown procedures that encode judgment, process, and domain knowledge. 90% of the value sits here, not in the harness.
- **Skills work like method calls.** A skill takes parameters. The same `/investigate` skill with different arguments becomes a medical research analyst or a forensic investigator.
- **[[Resolvers]] are routing tables for context.** When task type X appears, load document Y first. Claude Code's skill description field is a built-in resolver. Tan's CLAUDE.md was 20,000 lines; the fix was ~200 lines of pointers with resolvers loading the right document on demand.
- **[[Latent vs Deterministic]] is the most important boundary in agent design.** Latent space is for judgment and synthesis. Deterministic space is for SQL, compiled code, arithmetic. The worst systems put the wrong work on the wrong side.
- **[[Diarization]] makes AI useful for real knowledge work.** The model reads everything about a subject and writes a structured profile — a single page of judgment distilled from dozens of documents. No SQL query or RAG pipeline produces this.
- **The anti-pattern is a fat harness with thin skills.** 40+ tool definitions eating half the context window, god-tools with multi-second MCP round-trips, REST API wrappers per endpoint. Three times the tokens, latency, and failure rate.
- **Purpose-built tooling beats generic MCP.** A Playwright CLI at 100ms per operation vs. a Chrome MCP at 15 seconds per screenshot-find-click-wait-read — 75x faster.
- **Skills are permanent upgrades.** They never degrade, never forget, run at 3 AM, and automatically improve when the next model drops (latent steps get smarter, deterministic steps stay reliable).
- **Skills can rewrite themselves.** A feedback loop reads post-event surveys, diarizes mediocre responses, extracts patterns, and writes new rules back into the skill file. "OK" ratings dropped from 12% to 4% without anyone touching code.
- **"Never do one-off work."** If something will need to happen again: do it manually on 3–10 items, show output, codify into a skill, put on a cron if it should be automatic. "If I have to ask you for something twice, you failed."

## The Three-Layer Architecture

| Layer | What | Examples |
|---|---|---|
| **Fat skills** (top) | Markdown procedures encoding judgment, process, domain knowledge | `/investigate`, `/enrich-founder`, `/match-breakout`, `/improve` |
| **Thin CLI harness** (middle) | ~200 lines. JSON in, text out. Read-only by default | The loop, file I/O, context management, safety |
| **Deterministic application** (bottom) | Same input, same output. Every time | QueryDB, ReadDoc, Search, Timeline, SQL, compiled code |

The principle is directional: push intelligence **up** into skills, push execution **down** into deterministic tooling, keep the harness thin.

## The YC Startup School Case Study

Chase Center, July 2026. Six thousand founders. The system demonstrates all five definitions:

**Enrichment:** `/enrich-founder` pulls all sources, runs enrichments, diarizes, highlights the gap between what founders say and what they're actually building. Deterministic layer handles SQL, GitHub stats, browser tests, social signals. Runs nightly on cron.

> FOUNDER: Maria Santos COMPANY: Contrail (contrail.dev) SAYS: "Datadog for AI agents" ACTUALLY BUILDING: 80% of commits are in billing module. She's building a FinOps tool disguised as observability.

That gap requires reading GitHub commit history, application, and advisor transcript simultaneously. No embedding search or keyword filter finds it — the model has to read the full profile and make a judgment. A perfect [[Latent vs Deterministic|latent space]] problem.

**Matching (skill-as-method-call):** Three invocations of the same matching skill, three strategies:
- `/match-breakout` — 1,200 founders, sector clusters, 30 per room (embedding + deterministic assignment)
- `/match-lunch` — 600 founders, serendipity matching, 8 per table (LLM invents themes → deterministic seat assignment)
- `/match-live` — whoever's in the building, nearest-neighbor embedding, 200ms, 1:1 pairs

**The learning loop:** `/improve` reads NPS surveys, diarizes "OK" responses (not bad ones — the ones where the system *almost* worked), extracts patterns, writes new rules back into the matching skills. Skills rewrite themselves. 12% "OK" → 4% at the next event.

## Entities Mentioned

- [[Garry Tan]] — author, YC president
- [[Steve Yegge]] — cited for the 10x/100x/1000x productivity claim
- [[Claude Code]] — cited for leaked source confirming the harness thesis
- [[Anthropic]] — maker of Claude Code
- [[OpenClaw]] — Tan references "my OpenClaw"

## Concepts Discussed

- [[Thin Harness, Fat Skills]] — the central architecture
- [[Skill Files]] — reusable markdown procedures (the "fat" layer)
- [[Resolvers]] — context routing tables
- [[Latent vs Deterministic]] — the design boundary
- [[Diarization]] — structured synthesis from documents
- [[Agent Harness]] — the "thin" layer
- [[Agent Memory]] — implicitly: context management is a harness function, but should be minimal
- [[Claws]] — skills on cron are claws by another name
- [[AutoResearch]] — the learning loop is the same pattern

## Quotes Worth Preserving

> The 2x people and the 100x people are using the same models. The difference isn't intelligence. It's architecture — and it fits on an index card.

> A skill file works like a method call. It takes parameters. You invoke it with different arguments. The same procedure produces radically different capabilities depending on what you pass in.

> This is not prompt engineering. This is software design, using markdown as the programming language and human judgment as the runtime.

> My CLAUDE.md was 20,000 lines. Every quirk, every pattern, every lesson I'd ever encountered. Completely ridiculous. The model's attention degraded. Claude Code literally told me to cut it back.

> Every skill you write is a permanent upgrade to your system. It never degrades. It never forgets. It runs at 3 AM while you sleep.

> If I have to ask you for something twice, you failed.

## Strength/Weakness Assessment

**Strengths:**
- The most concrete architectural framework in the wiki — five named definitions that compose into a three-layer stack. Easy to teach, easy to apply.
- The YC Startup School case study is the most detailed end-to-end example of a real AI system across all sources. Not hypothetical.
- The skill-as-method-call framing is genuinely novel — elevates skills from "prompt templates" to a programming paradigm.
- The self-rewriting skill loop (12% → 4% "OK" ratings) is the most compelling evidence of autonomous improvement outside [[AutoResearch]].
- The 20,000-line CLAUDE.md confession is brutally honest and practically useful — a concrete lesson about context management.

**Weaknesses:**
- The "~200 lines" harness claim is aspirational and somewhat misleading. Tan himself uses [[Claude Code]] (512k lines) as his harness. The 200-line figure describes the *user-built* thin wrapper, not the full stack.
- Doesn't engage with [[Harrison Chase]]'s [[Memory Lock-In]] argument. If skills are portable but the harness manages memory, you still lose cross-session context when switching. Skills and memory are separate concerns.
- The Steve Yegge "1000x" opening is hyperbolic and the article doesn't substantiate it — the case study shows impressive capability but not measured productivity multiples.
- The anti-MCP argument (Playwright CLI at 100ms vs. Chrome MCP at 15 seconds) compares a purpose-built tool to a generic one — this is always true, regardless of architecture. The trade-off is development cost vs. runtime speed.
- No discussion of failure modes. When do fat skills go wrong? What happens when a skill encodes bad judgment?

> [!warning] Contradicts Harrison Chase
> This source directly opposes the central thesis of [[Your harness, your memory (Harrison Chase)|"Your harness, your memory"]]. Chase argues the harness is the critical layer (512k lines, memory inseparable). Tan argues the harness should be deliberately thin (~200 lines) and that **skills, not the harness**, are where value accumulates. If Tan is right, [[Memory Lock-In]] matters less than Chase claims — because the valuable artifacts (skill files) are portable markdown, not trapped in the harness. See [[Thin Harness, Fat Skills]] for the full concept treatment.
