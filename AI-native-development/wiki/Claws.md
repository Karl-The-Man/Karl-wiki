---
type: concept
title: Claws
created: 2026-04-11
updated: 2026-04-13
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md, Thin Harness, Fat Skills.md]
tags: [agents, autonomy, persistence, paradigm]
---

# Claws

[[Andrej Karpathy]]'s term for the next evolution beyond interactive coding agents — **persistent, looping, sandboxed autonomous entities** that operate on your behalf even when you're not watching.

## What Distinguishes a Claw from an Agent

| | Agent | Claw |
|---|---|---|
| **Interaction** | Interactive, in-session | Runs independently |
| **Persistence** | Session-scoped | Keeps looping |
| **Sandbox** | Shares your environment | Has its own little sandbox/setup |
| **Memory** | Context window (compaction) | Sophisticated memory systems |
| **Identity** | Tool | Entity with personality |

> "When I say a claw, I mean this layer that kind of takes persistence to a whole new level. It's something that keeps looping. It's not something that you are interactively in the middle of."

## Karpathy's "Dobby" Claw

Karpathy built a claw called Dobby (the elf) that manages his home:

- **Discovery:** Agents scanned his local network, found Sonos speakers, reverse-engineered the API, and played music — all from "Can you find my Sonos?"
- **Lighting:** Hacked into the lighting system, created APIs, built a command center dashboard
- **Full home control:** Lights, HVAC, shades, pool/spa
- **Security:** Camera with change detection → Qwen vision model → WhatsApp alerts ("Hey, a FedEx truck just pulled up")
- **Interface:** Natural language via WhatsApp. "Dobby, it's sleepy time" → all lights off
- **Replaced six apps** with a single natural language interface

## Peter Steinberger's OpenClaw

[[Peter Steinberger]] built [[OpenClaw]], which Karpathy credits with innovating in:
- Soul/demeanor document (crafted personality)
- Sophisticated memory (beyond default compaction)
- WhatsApp as single portal
- Making the experience fun and compelling

## Apps → APIs

The claw paradigm implies that many consumer apps **shouldn't exist as apps**:

> "These apps that are in the App Store for using these smart home devices shouldn't even exist. Shouldn't it just be APIs, and shouldn't agents be just using it directly?"

This points toward the [[Agentic Web]] — where the customer is no longer the human but agents acting on behalf of humans.

## The Accessibility Trajectory

Karpathy acknowledges that today, building claws requires vibe-coding and technical skill. But he predicts:

> "This kind of stuff should be free in a year or two or three. There's no vibe-coding involved. This is trivial. This is table stakes."

## Skills on Cron: Claws by Another Name

[[Garry Tan]]'s [[Thin Harness, Fat Skills (Garry Tan)|"Thin Harness, Fat Skills"]] describes a pattern that is functionally a claw: [[Skill Files]] running on a cron schedule, operating autonomously, producing results while you sleep.

In the YC Startup School case study, an `/enrich-founder` skill runs nightly across 6,000 founder profiles — pulling sources, running enrichments, [[Diarization|diarizing]] each profile. An `/improve` skill reads post-event surveys and rewrites matching skills based on feedback. These are claws in Karpathy's sense: persistent, looping, autonomous.

Tan's framing adds a creation pathway: every recurring task should be codified into a skill, and if it should run automatically, put on a cron. The claw isn't designed top-down — it *emerges* from the discipline of never doing one-off work.

## Related Concepts

- [[Agentic Web]] — the industry reconfiguration claws point toward
- [[AI Psychosis]] — claws add another layer of infinite possibility
- [[OpenClaw]] — the leading open-source claw project
- [[AutoResearch]] — a specialized claw for ML experimentation
- [[Token Throughput]] — claws maximize throughput by removing you from the loop
- [[Skill Files]] — the building blocks of claws in Tan's model
- [[Thin Harness, Fat Skills]] — the architecture that produces claws as a natural consequence
