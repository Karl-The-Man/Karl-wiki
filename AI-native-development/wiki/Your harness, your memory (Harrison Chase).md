---
type: source-summary
title: "Your harness, your memory (Harrison Chase)"
created: 2026-04-12
updated: 2026-04-12
sources: [Your harness, your memory.md]
tags: [agent-harness, memory, lock-in, open-source, langchain]
---

# Your harness, your memory (Harrison Chase)

**Source:** Blog post / X thread by [[Harrison Chase]], CEO of [[LangChain]], published 2026-04-03.

## Summary

Argues that [[Agent Harness|agent harnesses]] are the permanent scaffolding layer around LLMs, that harnesses are inextricably tied to [[Agent Memory]], and that using a closed or proprietary harness means surrendering ownership of your memory to a third party. Since memory is what makes agents personalized, sticky, and defensible, this creates dangerous [[Memory Lock-In|vendor lock-in]]. The solution: use open-source, model-agnostic harnesses like [[Deep Agents]].

## Key Claims

- **Agent harnesses are not going away.** The sentiment that "models will absorb the scaffolding" is wrong. Old scaffolding gets replaced by new scaffolding, not by no scaffolding. Even [[Claude Code]] has 512k lines of harness code. When web search is "built into" APIs, it's actually a lightweight harness behind the API orchestrating tool calls.
- **Memory is not a plugin — it's the harness.** Short-term memory (messages, tool results) and long-term memory (cross-session) are both managed by the harness. Cites [[Sarah Wooders]] (CTO of [[Letta]]): "Asking to plug memory into an agent harness is like asking to plug driving into a car."
- **Closed harnesses = lost memory ownership.** Three levels of severity:
  1. *Mildly bad:* Stateful APIs (OpenAI's Responses API, [[Anthropic]]'s server-side compaction) store state on provider servers — can't swap models and resume threads.
  2. *Bad:* Closed harnesses ([[Claude Agent SDK]]) interact with memory in unknown, non-transferable ways.
  3. *Worst:* Entire harness + long-term memory behind an API (Anthropic's Claude Managed Agents) — zero ownership or visibility.
- **"Models absorbing the harness" really means memory going behind provider APIs.** Model providers are incentivized to do this because memory creates lock-in that the model alone doesn't.
- **Memory is what makes agents defensible.** Without memory, agents are easily replicable by anyone with the same tools. With memory, you build a proprietary dataset of user interactions and preferences.
- **Memory is still in its infancy.** No well-known abstractions yet. Long-term memory is often not part of MVPs. The industry is still figuring out best practices.
- **Even open-source harnesses aren't immune.** [[Codex]] (open source) generates encrypted compaction summaries not usable outside OpenAI's ecosystem.

## Entities Mentioned

- [[Harrison Chase]] — author, CEO of [[LangChain]]
- [[LangChain]] — company behind [[Deep Agents]], LangGraph, LangSmith
- [[Deep Agents]] — open-source, model-agnostic agent harness (the advocated solution)
- [[Sarah Wooders]] — CTO of [[Letta]], cited for "memory isn't a plugin" thesis
- [[Letta]] — company at the forefront of stateful agents
- [[Claude Code]] — cited as example harness (512k lines leaked)
- [[Anthropic]] — cited for server-side compaction and Claude Managed Agents
- [[Claude Agent SDK]] — cited as closed harness example
- [[Codex]] — cited for encrypted compaction
- [[OpenClaw]] — cited as example harness (powered by Pi)
- [[OpenAI]] — cited for Responses API stateful storage

## Concepts Discussed

- [[Agent Harness]] — the central subject
- [[Agent Memory]] — why it's tied to harnesses
- [[Memory Lock-In]] — the core argument
- [[The Bitter Lesson]] — implicitly relevant: the claim that harnesses won't be absorbed mirrors the lesson that scaffolding persists

## Quotes Worth Preserving

> Asking to plug memory into an agent harness is like asking to plug driving into a car. Managing context, and therefore memory, is a core capability and responsibility of the agent harness. — Sarah Wooders

> Without memory, your agents are easily replicable by anyone who has access to the same tools.

> Memory — and therefore harnesses — should be open, so that you own your own memory.

## Strength/Weakness Assessment

**Strengths:**
- Clear, well-structured argument with a concrete threat model (three levels of lock-in)
- Grounded in real examples: Claude Code's leaked 512k lines, Codex's encrypted compaction, Anthropic's Managed Agents
- The personal anecdote (deleted email assistant, lost memory, degraded experience) makes the lock-in argument tangible
- Sarah Wooders' "driving into a car" framing is the most memorable articulation of the harness-memory relationship

**Weaknesses:**
- Transparently self-interested: the entire piece is a lead-up to pitching [[Deep Agents]], LangChain's product. The argument is sound, but the motivation is commercial.
- Doesn't address whether open harnesses can match the developer experience of tightly integrated closed systems. The lock-in may be a rational trade for a better product.
- "Memory is in its infancy" somewhat undercuts the urgency — if we don't know what memory looks like yet, is it premature to worry about lock-in?
- Doesn't engage with the counter-argument that model providers may have legitimate reasons for managing memory (safety, privacy, consistency).
- The claim that Claude Agent SDK is "closed" and its memory interaction is "unknown" may be somewhat overstated — the SDK is documented, and CLAUDE.md / memory files are local and inspectable.
