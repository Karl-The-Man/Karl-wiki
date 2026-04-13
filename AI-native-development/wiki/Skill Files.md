---
type: concept
title: Skill Files
created: 2026-04-13
updated: 2026-04-13
sources: [Thin Harness, Fat Skills.md]
tags: [architecture, skills, markdown, agents]
---

# Skill Files

A reusable markdown document that teaches an LLM how to do something. Not *what* to do — the user supplies that. The skill supplies the **process**. Central to [[Garry Tan]]'s [[Thin Harness, Fat Skills]] architecture, where skill files are the "fat" layer containing 90% of the system's value.

## Skills as Method Calls

The key insight: **a skill file works like a method call.** It takes parameters. You invoke it with different arguments. The same procedure produces radically different capabilities.

**Example:** A skill called `/investigate` has seven steps: scope the dataset, build a timeline, diarize every document, synthesize, argue both sides, cite sources. It takes three parameters: TARGET, QUESTION, DATASET.

- Point it at a safety scientist + 2.1 million discovery emails → medical research analyst determining if a whistleblower was silenced
- Point it at a shell company + FEC filings → forensic investigator tracing coordinated campaign donations

Same skill. Same seven steps. Same markdown file. The skill describes a **process of judgment**. The invocation supplies the world.

## What a Skill Is Not

> This is not prompt engineering. This is software design, using markdown as the programming language and human judgment as the runtime.

Tan distinguishes skill files from prompt templates. A prompt template fills in blanks. A skill file encodes a multi-step process with judgment at each step, decisions about what's [[Latent vs Deterministic|latent vs. deterministic]], and domain knowledge about how to approach a class of problems.

## Markdown as a Programming Language

Tan argues markdown is "a more perfect encapsulation of capability than rigid source code" because it describes process, judgment, and context in the language the model already thinks in. Skills are:
- Human-readable and human-editable
- Portable (just files — no framework dependency)
- Version-controllable (git)
- Composable (skills can invoke other skills)

## Skills That Rewrite Themselves

The most ambitious pattern: a feedback loop where skills improve autonomously.

In the [[Thin Harness, Fat Skills (Garry Tan)#The YC Startup School Case Study|YC Startup School case study]], an `/improve` skill reads post-event NPS surveys, diarizes the mediocre responses (not the bad ones — the "OK" ones where the system almost worked), extracts patterns, and writes new rules back into the matching skills:

> When attendee says "AI infrastructure" but startup is 80%+ billing code: → Classify as FinTech, not AI Infra.

"OK" ratings: 12% → 4% at the next event. The skill file learned what "OK" actually meant.

## The "Never Do One-Off Work" Rule

Tan's instruction to his [[OpenClaw]]:

> If I ask you to do something and it's the kind of thing that will need to happen again, you must: do it manually the first time on 3 to 10 items. Show me the output. If I approve, codify it into a skill file. If it should run automatically, put it on a cron. The test: if I have to ask you for something twice, you failed.

Every skill is a permanent upgrade. It never degrades, never forgets, runs at 3 AM, and automatically improves when the next model drops.

## Relationship to Existing Concepts

Skills connect to several existing wiki concepts:

- **[[Education Through Agents]]** — Karpathy's vision of writing "skills" that script how an agent should teach a curriculum is the same concept. Skills as the new medium of instruction.
- **[[Claws]]** — a skill on a cron is a claw by another name. The enrichment skill running nightly on 6,000 founder profiles is functionally a persistent autonomous agent.
- **[[AutoResearch]]** — Karpathy's ML experimentation loop is a specialized skill: scope → run experiments → measure → iterate.
- **[[Resolvers]]** — the routing layer that loads the right skill at the right time.

## Related Concepts

- [[Thin Harness, Fat Skills]] — the architecture they're central to
- [[Resolvers]] — how skills get invoked
- [[Latent vs Deterministic]] — the boundary skills must respect
- [[Diarization]] — a canonical skill pattern
- [[Agent Harness]] — the thin layer that runs skills
