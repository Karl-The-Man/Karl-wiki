---
type: entity
title: Garry Tan
created: 2026-04-13
updated: 2026-04-13
sources: [Thin Harness, Fat Skills.md]
tags: [person, yc, investor, ai-native]
---

# Garry Tan

President of Y Combinator. Author of the [[Thin Harness, Fat Skills (Garry Tan)|"Thin Harness, Fat Skills"]] framework — the most concrete architectural prescription in the wiki for how to build systems around LLMs.

## Key Contributions

### The Thin Harness, Fat Skills Architecture

Tan proposes a three-layer architecture: [[Skill Files|fat skills]] (markdown procedures encoding judgment) on top, a [[Thin Harness, Fat Skills|thin CLI harness]] (~200 lines) in the middle, and a deterministic application layer (SQL, compiled code) on the bottom. Push intelligence up, push execution down, keep the middle thin.

### Five Definitions

Tan's vocabulary for agent system design: [[Skill Files]], the harness, [[Resolvers]], [[Latent vs Deterministic]], and [[Diarization]]. These compose into the three-layer architecture.

### YC Startup School System

Building an AI system at YC to manage 6,000 founders at Chase Center (July 2026) — enrichment, diarization, matching, and self-improving feedback loops. The most detailed end-to-end case study in the wiki.

### "Never Do One-Off Work"

An instruction to his [[OpenClaw]]: if a task will recur, codify it into a [[Skill Files|skill file]]. If it should be automatic, put it on a cron. "If I have to ask you for something twice, you failed."

## Context

Tan read [[Claude Code]]'s leaked source code (512k lines) and concluded it confirmed his thesis: the secret isn't the model, it's the wrapper. He teaches this framework at YC and has been building it into the Startup School operations.

His CLAUDE.md grew to 20,000 lines before the model's attention degraded and Claude Code told him to cut it back. The fix: ~200 lines of pointers, with [[Resolvers]] loading the right document on demand.

## Related Pages

- [[Thin Harness, Fat Skills (Garry Tan)]] — source summary
- [[Thin Harness, Fat Skills]] — the architecture
- [[Skill Files]] — the central concept
- [[OpenClaw]] — his claw
- [[Steve Yegge]] — cited in his article
