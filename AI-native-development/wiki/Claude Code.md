---
type: entity
title: Claude Code
created: 2026-04-10
updated: 2026-04-11
sources: [Building-Claude-Code-with-Boris-Cherny.md, Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [tool, anthropic, agentic-ai, coding]
---

# Claude Code

**[[Anthropic]]**'s agentic coding tool. Terminal-based, also available on iOS, Android, desktop app, web (claude.ai/code), and IDE extensions (VS Code, JetBrains). Created by [[Boris Cherny]] as a personal side project; now one of the fastest-growing developer tools.

## Origins

- Predecessor was "Clyde" — a janky internal Python tool that took 40 seconds to start, was not agentic, but could write working PRs if prompted carefully
- Boris started Claude Code as a simple chatbot hitting the Anthropic API in the terminal
- The pivotal moment was adding **tool use** (the bash tool): "the model just wants to use tools — if you give it a tool it will figure out how to use it"
- With Sonnet 3.5, it one-shotted an AppleScript to query what music Boris was listening to
- Boris was the sole developer for the first three months
- Permission system was in the very first version (September 2024), co-designed with Ben Mann

## Architecture

The architecture is described as "very simple":

- A core **query loop**
- A few **tools** (bash, file edit, others constantly added/removed)
- A **terminal UI** layer
- Extensive **security code**

### Agentic Search over RAG

A defining architectural decision: they **abandoned RAG** (retrieval-augmented generation with a local vector database) in favor of [[Agentic Search]] — which is "a fancy word for glob and grep." The model uses these tools the way Instagram engineers used Meta's global index when click-to-definition was broken. RAG failed because code drifted out of sync and indexing permissions were complex. This is a concrete example of [[The Bitter Lesson]] — letting the model search on its own outperformed engineering a retrieval system around it.

## Adoption

- Writes approximately **80% of all code at Anthropic** on average
- Every technical employee uses it daily; non-technical adoption (sales, finance) is approaching 100%
- Dario Amodei asked if people were being forced to adopt it — they were not; people "voted with their feet"
- External growth was initially slow; the first big inflection came with Opus 4 and Sonnet 4
- [[Claude Co-Work]]'s growth trajectory is steeper than Claude Code's initial trajectory

## Development Culture

- The spinner alone went through ~100 iterations, with 10–20 landing in production
- Most code is thrown away because the cost of building is so low
- The team practices [[Prototyping Over PRDs]]: "we don't really write stuff — we just show"
- For the condensed file read view: ~30 prototypes, a month of internal dogfooding, then iterative external feedback
- Designed for **hackability** — session start hooks, configurable permissions, allow lists, plugins, and skills let users customize behavior

## Safety

Safety uses a [[Swiss Cheese Model (Safety)|Swiss cheese model]] with multiple layers:

1. **Model-level alignment** (Opus 4.6 described as "the most aligned model")
2. **Runtime classifiers** blocking suspicious requests
3. **Sub-agent summarization** of web fetch results before returning to the main agent
4. **Permission prompts** — asking the human when uncertain
5. Few Unix utilities pre-allowed because even `find` and `sed` can execute arbitrary code

## Code Review

- Every PR at Anthropic is first reviewed by Claude (via [[Claude Agent SDK]] in CI), catching ~80% of bugs
- Claude automatically addresses some review comments; a human always does a second pass
- Claude Code tests itself by launching itself in a subprocess for end-to-end verification — emerged spontaneously with Opus 4/4.5
- [[Best of N]] used for higher determinism: parallel agents + deduplication

## External Perspective: Karpathy on Personality

[[Andrej Karpathy]] — who uses both Claude Code and [[Codex]] — praises Claude's personality calibration as superior:

> "I think they dialed the psychopathy fairly well, where when Claude gives me praise, I do feel like I slightly deserve it."

He describes a feedback loop where he tries to "earn its praise" — when he gives a half-baked idea, Claude responds mildly; when the idea is genuinely good, Claude rewards it more. This contrasts with [[Codex]]'s dry, disengaged personality and ChatGPT's excessive sycophancy.

Karpathy also notes he uses Claude Code alongside [[Codex]], switching between them to maximize [[Token Throughput]] — using one when the other's subscription is exhausted.

## Key Models

- **Sonnet 3.5** — first model that demonstrated tool use potential
- **Opus 4 / Sonnet 4** — drove the first external growth inflection
- **Opus 4.5** — the model that made Boris uninstall his IDE
- **Opus 4.6** — "most aligned model"; made [[Agent Teams]] click
