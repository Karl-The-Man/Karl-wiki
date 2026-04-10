---
type: concept
title: Agentic Web
created: 2026-04-11
updated: 2026-04-11
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [infrastructure, agents, future, apis]
---

# Agentic Web

The vision that the internet and software ecosystem will reconfigure so that **the customer is no longer the human — it's agents acting on behalf of humans**. Custom bespoke apps give way to exposed API endpoints, with agents as the intelligent glue.

## The Argument

[[Andrej Karpathy]] on smart home apps:

> "These apps that are in the App Store for using these smart home devices shouldn't even exist, kind of. Shouldn't it just be APIs, and shouldn't agents be just using it directly?"

An LLM can drive tools and make complex cross-system decisions that no individual app can. Karpathy's [[Claws|Dobby claw]] replaced six separate smart home apps with a single natural-language WhatsApp interface.

Another example: a treadmill app with a web UI and login flow. "All this should just be: make APIs available."

## The Reconfiguration

> "The industry just has to reconfigure in so many ways that the customer is not the human anymore. It's agents who are acting on behalf of humans, and this refactoring will probably be substantial."

This means:
- **Apps → APIs** — expose functionality for agents, not humans
- **UIs become optional** — agents generate interfaces as needed ("ephemeral software")
- **Agent-first design** — build for agent consumption first, human consumption second
- **Cross-system intelligence** — agents can do "all kinds of home automation stuff that any individual app will not be able to do"

## Relationship to Agentic Search

The wiki already covers [[Agentic Search]] — replacing RAG with model-driven grep/glob. The Agentic Web is the same principle applied at internet scale: instead of building human-facing interfaces, expose machine-friendly endpoints and let agents navigate them.

## Timeline

Karpathy acknowledges this requires vibe-coding today but predicts it becomes "table stakes" in 1–3 years — "even open-source models should be able to do this."

## Related Concepts

- [[Claws]] — the persistent agents that consume the agentic web
- [[Agentic Search]] — the same principle applied to code search
- [[Education Through Agents]] — documentation for agents, not humans
- [[Digital-Physical Interface]] — when agents need data from the physical world
