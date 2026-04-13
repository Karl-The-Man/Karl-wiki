---
type: concept
title: Latent vs Deterministic
created: 2026-04-13
updated: 2026-04-13
sources: [Thin Harness, Fat Skills.md]
tags: [architecture, principle, design, agents]
---

# Latent vs Deterministic

The most important boundary in agent system design, per [[Garry Tan]]. Every step in an AI system is one or the other, and confusing them is the most common mistake.

## Definitions

**Latent space** is where intelligence lives. The model reads, interprets, decides. Judgment. Synthesis. Pattern recognition.

**Deterministic** is where trust lives. Same input, same output. Every time. SQL queries. Compiled code. Arithmetic.

## The Dinner Table Test

> An LLM can seat 8 people at a dinner table, accounting for personalities and social dynamics. Ask it to seat 800 and it will hallucinate a seating chart that looks plausible but is completely wrong.

Seating 800 is a combinatorial optimization problem — deterministic. Forcing it into latent space produces confident-looking garbage. The worst systems put the wrong work on the wrong side of this line. The best systems are ruthless about it.

## How It Maps to the Architecture

In the [[Thin Harness, Fat Skills]] three-layer stack:

- **[[Skill Files]]** (top) operate primarily in latent space — judgment, synthesis, decision-making
- **Application layer** (bottom) operates in deterministic space — SQL, search, compiled code
- **The harness** (middle) manages the boundary between them

A well-designed skill knows which steps are latent and which are deterministic. In the [[Thin Harness, Fat Skills (Garry Tan)#The YC Startup School Case Study|YC Startup School]] example:
- **Latent:** reading a founder's profile and judging the gap between what they say vs. what they're actually building
- **Deterministic:** SQL lookups, GitHub stats, embedding-based seat assignment
- **Latent:** inventing lunch table themes based on serendipity
- **Deterministic:** assigning seats with no-repeat constraints

## Relationship to Existing Wiki Concepts

### Jaggedness
[[Jaggedness]] ([[Andrej Karpathy]]) describes the same boundary from the capability side: models are brilliant in verifiable domains (deterministic-adjacent) and mediocre in non-verifiable ones. Latent vs. Deterministic is the *design response* to Jaggedness — put verifiable work in deterministic code, reserve latent space for judgment that benefits from flexibility.

### The Bitter Lesson
[[The Bitter Lesson]] says: don't over-engineer around the model; give it tools and get out of the way. Latent vs. Deterministic adds precision: get out of the way *in latent space*, but don't put deterministic work there. The model should judge; it shouldn't do arithmetic.

### Diarization
[[Diarization]] is the canonical latent-space operation: read everything about a subject, hold contradictions in mind, synthesize. No deterministic process produces this output.

## Related Concepts

- [[Thin Harness, Fat Skills]] — the architecture this boundary enables
- [[Skill Files]] — skills must respect this boundary at each step
- [[Jaggedness]] — the capability observation behind this design principle
- [[The Bitter Lesson]] — the philosophical foundation
- [[Diarization]] — pure latent-space work
