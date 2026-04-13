---
type: concept
title: Diarization
created: 2026-04-13
updated: 2026-04-13
sources: [Thin Harness, Fat Skills.md]
tags: [technique, knowledge-work, synthesis, agents]
---

# Diarization

The step that makes AI useful for real knowledge work. The model reads everything about a subject and writes a structured profile — a single page of judgment distilled from dozens or hundreds of documents. Introduced by [[Garry Tan]] as one of the five definitions in [[Thin Harness, Fat Skills]].

## What It Produces

No SQL query produces this. No RAG pipeline produces this. The model has to actually read, hold contradictions in mind, notice what changed and when, and synthesize structured intelligence. It's the difference between a database lookup and an analyst's brief.

## Example: Founder Enrichment

In the [[Thin Harness, Fat Skills (Garry Tan)#The YC Startup School Case Study|YC Startup School case study]], the `/enrich-founder` skill diarizes 6,000 founder profiles nightly:

> FOUNDER: Maria Santos COMPANY: Contrail (contrail.dev) SAYS: "Datadog for AI agents" ACTUALLY BUILDING: 80% of commits are in billing module. She's building a FinOps tool disguised as observability.

This requires reading the GitHub commit history, the application, and the advisor transcript, and holding all three in mind at once. No embedding similarity search finds this gap. No keyword filter finds it. The model has to read the full profile and make a judgment.

## Why It's Pure Latent Space

Diarization is the canonical [[Latent vs Deterministic|latent-space]] operation. The deterministic layer (SQL, GitHub API, social signal pulls) gathers the raw inputs. The latent step synthesizes them into a structured profile with judgment. This is exactly the division of labor that [[Thin Harness, Fat Skills]] prescribes.

## Relationship to Existing Concepts

- **[[Agent Memory]]** — diarization produces the *content* of what an agent remembers about a subject. It's a write operation to the agent's knowledge base.
- **[[AutoResearch]]** — Karpathy's autonomous ML experimentation includes a similar synthesis step: the agent reads experiment results and produces structured analysis.
- **[[Agentic Search]]** — agentic search finds information; diarization synthesizes it into judgment.

## Related Concepts

- [[Thin Harness, Fat Skills]] — the architecture diarization fits into
- [[Latent vs Deterministic]] — diarization is pure latent space
- [[Skill Files]] — diarization is typically a step within a skill
- [[Agent Memory]] — diarization produces structured memory
