---
type: entity
title: Anthropic
created: 2026-04-10
updated: 2026-04-11
sources: [Building-Claude-Code-with-Boris-Cherny.md, Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [company, ai-safety, claude]
---

# Anthropic

AI safety research lab and maker of Claude. Described by [[Boris Cherny]] as a "research/safety lab with product tacked on." Enterprise-focused.

## Engineering Culture

- **Flat titles**: everyone is "Member of Technical Staff" — encodes a [[Generalist vs Specialist|generalist]] expectation and removes assumptions about specialization
- **No formal PRDs**: [[Prototyping Over PRDs|prototypes preferred]] over documents. Product lead Cat Woo's attitude: "better send a PR"
- **No mandatory ticketing system**: individuals choose their own tools (Asana, Notes, nothing)
- **Everyone codes**: engineers, engineering managers, designers, data scientists, finance, and sales people all use [[Claude Code]]
- Culture of "we don't really write stuff — we just show"

## Claude Code Adoption

- [[Claude Code]] writes approximately **80% of all code at Anthropic**
- Every technical employee uses Claude Code daily; non-technical adoption approaching 100%
- Adoption was organic — Dario Amodei asked if people were being forced; they were not
- Non-engineers using Claude Code (finance, sales, data scientists) signaled [[Latent Demand]] for [[Claude Co-Work]]

## Safety Philosophy

- Core mission: studying safety in the wild by observing real user behavior, which makes models safer
- This mission drove the decision to release [[Claude Code]] externally
- Cannot see user data due to enterprise privacy commitments; significant engineering goes into privacy-preserving logging
- Safety framed as [[Swiss Cheese Model (Safety)|Swiss cheese model]] — multiple overlapping layers, "counting nines"

## Key People (from sources)

- **Dario Amodei** — CEO
- **Ben Mann** — co-founder, hired Boris, co-designed the Claude Code permission system, started the labs team
- **Mike Krieger** — former Instagram co-founder, now at Anthropic
- **[[Boris Cherny]]** — creator and engineering lead of Claude Code
- **Fiona Fun** — manager of the Claude Code team
- **Cat Woo** — product lead on Claude Code team
