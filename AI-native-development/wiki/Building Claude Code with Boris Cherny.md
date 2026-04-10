---
type: source-summary
title: Building Claude Code with Boris Cherny
created: 2026-04-10
updated: 2026-04-10
sources: [Building-Claude-Code-with-Boris-Cherny.md]
tags: [claude-code, anthropic, agentic-ai, ai-native-workflow, podcast]
---

# Building Claude Code with Boris Cherny

## Summary

Long-form podcast interview on **The Pragmatic Engineer** (hosted by Gergely Orosz) with **[[Boris Cherny]]**, creator and engineering lead of **[[Claude Code]]** at **[[Anthropic]]**. Boris traces his path from freelancing as a teenager, through seven years at Meta (Facebook/Instagram), to building Claude Code from a personal side project into one of the fastest-growing developer tools. The conversation covers his daily workflow of shipping 20–30 PRs per day with zero hand-written code, Claude Code's architecture, safety engineering for agentic tools, and the recent launches of **[[Claude Co-Work]]** and **[[Agent Teams]]**.

The interview is especially rich on the practical realities of [[AI-Native Workflow]]: Boris describes round-robining between five terminal tabs with parallel Claude Code sessions, starting every task in plan mode, and overflowing to the Claude mobile app for phone-based coding. He discusses the decision to abandon RAG in favor of [[Agentic Search]] (grep/glob), why [[Prototyping Over PRDs]] has replaced document-driven development, and how Anthropic's flat organizational structure reflects a [[Generalist vs Specialist|generalist thesis]] about the future of engineering.

## Key Claims

### Claude Code origins and growth
- Claude Code originated as Boris's personal side project; he was the sole developer for the first three months
- Started as a simple chatbot hitting the Anthropic API in the terminal — the pivotal moment was adding tool use (bash tool), after which "the model just wants to use tools"
- Internal predecessor was called "Clyde" — a janky Python tool that took 40 seconds to start, not agentic, but could write working PRs if prompted carefully
- Boris's first PR at Anthropic was rejected by his ramp buddy Adam Wolf because he wrote it by hand — Wolf told him to use the Clyde tool instead
- Internal adoption at Anthropic grew organically — Dario Amodei asked if they were forcing people to use it; they were not
- Claude Code now writes approximately **80% of all code at Anthropic** on average, and **100% of Boris's code**
- Every technical employee at Anthropic uses Claude Code daily; non-technical adoption (sales, finance) is approaching 100%
- Externally, initial growth was slow; the first big inflection came with the release of Opus 4 and Sonnet 4

### Boris's daily workflow
- Ships **20–30 pull requests per day**, with zero hand-written code and zero manual line edits
- Uses five terminal tabs, each with a separate checkout, round-robining between parallel Claude Code sessions
- Starts almost every session in **plan mode** (shift-tab twice), focusing on getting the plan right before implementation
- Overflows to the Claude desktop app and iOS app — roughly a third to half of his code is written from his phone
- **Uninstalled his IDE** after Opus 4.5 shipped
- During a "coding vacation" in December traveling through Europe, Opus 4.5 wrote 100% of every PR; introduced ~2 bugs vs. an estimated ~20 if hand-written

### Code review in the AI era
- Every PR at Anthropic is first reviewed by Claude (via [[Claude Agent SDK]] in CI), catching approximately **80% of bugs**
- Claude automatically addresses some review comments; a human always does a second pass and must approve every change
- Claude Code tests itself by launching itself in a subprocess for end-to-end verification — this behavior emerged spontaneously with Opus 4/4.5
- For higher determinism: **[[Best of N]]** — launching parallel agents and deduplication agents to check for false positives

### Architecture and technical decisions
- Architecture is "very simple" — a core query loop, a few tools (bash, file edit, others constantly added/removed), a terminal UI layer, and extensive security code
- **Abandoned RAG** with a local vector database in favor of [[Agentic Search]] — just glob and grep. The model uses them the way Instagram engineers used Meta's global index when click-to-definition was broken
- RAG problems: code drifted out of sync, indexing permissions were complex, agentic search simply outperformed it
- The spinner alone went through ~100 iterations, with 10–20 landing in production
- Most code they write is thrown away because the cost of building is so low

### Safety and security
- External release was driven by Anthropic's core mission: studying safety in the wild makes the model safer
- Prompt injection handled via [[Swiss Cheese Model (Safety)|Swiss cheese model]]: (1) model-level alignment, (2) runtime classifiers blocking suspicious requests, (3) sub-agent summarization of web fetch results
- Permission system was in the very first version (September 2024), co-designed with Ben Mann (Anthropic co-founder)
- Few Unix utilities are pre-allowed because even `find` and `sed` can execute arbitrary code
- [[Claude Co-Work]] runs in a VM with additional classifiers and OS-level protections for non-technical users

### Claude Co-Work
- Built in approximately **10 days** by a small team, fully with Claude Code
- Designed for non-engineers who were already using Claude Code (a [[Latent Demand]] signal)
- Runs in the Claude desktop app (Electron/TypeScript), alongside code and chat tabs
- Boris uses it for weekly project management: reads a spreadsheet, identifies missing status updates, pings engineers on Slack

### Agent Teams (swarms)
- [[Agent Teams]] is Anthropic's implementation of swarms — multiple agents with [[Uncorrelated Context Windows]] working together
- Sub-agents start fresh and don't know what's in the parent context window, yielding better results for complex tasks
- This is a form of **test-time compute**
- The feature clicked specifically with Opus 4.6
- Plugins were built entirely by a swarm: an engineer set up a container in dangerous mode, let it run over a weekend, it spawned hundreds of agents, created 100 tasks on an Asana board, and implemented the feature

### The printing press analogy
- Boris compares the current AI moment to the [[The Printing Press Analogy|printing press]] in the 1400s
- Medieval scribes were a tiny literate elite; software engineers are the modern scribes
- After the printing press: cost dropped ~100x in 30–50 years; quantity increased ~10,000x in 50–100 years; literacy eventually reached ~70% but took 200–300 years
- Scribes didn't disappear — they became writers and authors; the market expanded enormously

### Skills that matter now
- **Less valuable**: strong opinions about code style, languages, frameworks — "the model can just rewrite it for you, so it just doesn't matter anymore"
- **Still valuable**: being methodical and hypothesis-driven; curiosity; willingness to work beyond your swim lane
- **Newly valuable**: short attention span / context-switching ("the year of ADHD"); multi-disciplinary thinking; [[Generalist vs Specialist|generalist]] orientation
- Boris believes the next trillion-dollar startup might be built by **one person** who thinks across engineering, product, business, design, and finance

### Engineering culture at Anthropic
- Everyone has the title "Member of Technical Staff" — encodes a [[Generalist vs Specialist|generalist]] expectation
- No formal PRDs; [[Prototyping Over PRDs|prototypes are preferred]] over documents
- No mandatory ticketing system; individuals choose their own tools
- Designers, data scientists, finance people, and sales people all code using Claude Code

## Entities Mentioned

- **[[Boris Cherny]]** — creator and engineering lead of Claude Code
- **[[Anthropic]]** — AI safety lab, maker of Claude
- **[[Claude Code]]** — Anthropic's agentic coding tool
- **[[Claude Co-Work]]** — product for non-engineers, runs Claude Code in a VM
- **[[Agent Teams]]** — swarm implementation with uncorrelated context windows
- **[[Claude Agent SDK]]** — powers Claude Code; used in CI for automated code review
- **Gergely Orosz** — host of The Pragmatic Engineer podcast
- **Dario Amodei** — CEO of Anthropic
- **Ben Mann** — Anthropic co-founder, co-designed the permission system
- **Mike Krieger** — former Instagram co-founder, now at Anthropic
- **Andrej Karpathy** — referenced for feeling "behind as a programmer" due to AI progress
- **Anders Hejlsberg** — creator of TypeScript, praised for type system design

## Concepts Discussed

- **[[Agentic Search]]** — replacing RAG with grep/glob driven by the model
- **[[The Bitter Lesson]]** — let the model do its thing; don't make it a component of a larger system
- **[[Prototyping Over PRDs]]** — build dozens of prototypes instead of writing documents
- **[[The Printing Press Analogy]]** — scribes → writers as the market for literature expanded
- **[[Uncorrelated Context Windows]]** — sub-agents with fresh context yield better results
- **[[Swiss Cheese Model (Safety)]]** — multiple overlapping safety layers
- **[[Generalist vs Specialist]]** — AI rewards multi-disciplinary generalists
- **[[AI-Native Workflow]]** — parallel agents, plan-first, phone-based coding
- **[[Best of N]]** — launching parallel agents for determinism
- **[[Latent Demand]]** — when non-target users adopt your tool, build for them
- **[[Understand the Layer Under]]** — always understand the abstraction layer below yours

## Notable Quotes

> "Now we're at the point where Claude Code writes, I think something like 80% of the code at Anthropic on average." — Boris Cherny

> "I'll be honest, it writes better code than I do." — Boris Cherny

> "The model just wants to use tools. That's just what I realized — like, if you give it a tool it will figure out how to use it to get the thing done." — Boris Cherny

> "Agentic search... this is a fancy word for glob and grep. That's all it is." — Boris Cherny

> "We don't really write stuff. We just show." — Boris Cherny, on the Claude Code team's culture

> "The cost of building is very low. But also we don't know where we're aiming. So we just have to try and we have to see what feels good." — Boris Cherny

> "Personally I'm wrong like half the time. At least half of my ideas are bad. And I don't know which half until I try it." — Boris Cherny

> "One metaphor I have for this moment in time is the printing press in the 1400s... there was a group of scribes that knew how to write... and if you think about what happened to the scribes, they ceased to become scribes, but now there's a category of writers and authors." — Boris Cherny

> "I can't wait to get past these endless language debates and framework debates... the model can just use whatever language and framework and if you don't like it it can just rewrite it for you. So it just doesn't matter anymore." — Boris Cherny

> "[Daisy] set up a container and she set up Claude in dangerous mode. And she let it run for the entire weekend. It spawned a couple hundred agents. They made 100 tasks on the Asana board. And then they implemented it." — Boris Cherny

> "Safety... it was kind of an important thing for me. Now it's just the most important thing for me — how do we make sure this thing goes well." — Boris Cherny

## Source Assessment

**Strengths:** First-person practitioner account from the creator of Claude Code who is also one of its most intensive users. Extraordinary specificity — concrete numbers (80% AI-written code, 20–30 PRs/day, 2 bugs vs. 20, plugins built by swarms over a weekend). Covers the full stack: architecture, safety, product process, org culture, career skills, and historical analogies.

**Weaknesses:** Single-perspective bias — an Anthropic insider talking about Anthropic's product with no competitive context (no comparison to Cursor, Copilot, Windsurf). Key quantitative claims (80% bug catch rate, productivity impact) lack methodology. Boris is an unusually productive senior engineer at the company that makes the tool — his workflow may not generalize. Raw podcast transcript with speech artifacts.
