---
type: concept
title: Memory Lock-In
created: 2026-04-12
updated: 2026-04-13
sources: [Your harness, your memory.md, Thin Harness, Fat Skills.md]
tags: [lock-in, memory, vendor, risk, open-source]
---

# Memory Lock-In

The phenomenon where an agent's accumulated [[Agent Memory]] becomes trapped in a proprietary platform, creating vendor lock-in that is stronger than model lock-in alone. Articulated by [[Harrison Chase]] in [[Your harness, your memory (Harrison Chase)|"Your harness, your memory"]].

## The Core Argument

Models have been relatively easy to swap. They have similar APIs, and prompt changes are manageable. But models are stateless. As soon as state — memory — enters the picture, switching becomes costly because **you lose what your agent has learned.**

Memory is what makes agents personalized, sticky, and defensible. Model providers know this. They are incentivized to pull memory behind their APIs because it creates lock-in that the model alone does not provide.

## Three Levels of Lock-In

Chase identifies a spectrum of severity:

### Level 1: Stateful APIs (Mild)
Using stateful APIs like [[OpenAI]]'s Responses API or [[Anthropic]]'s server-side compaction. State is stored on provider servers. If you want to swap models and resume previous threads, you can't.

### Level 2: Closed Harnesses (Bad)
Using a closed [[Agent Harness]] like [[Claude Agent SDK]]. The harness interacts with memory in ways that are unknown and non-transferable. Maybe it creates artifacts client-side, but their shape and intended usage are opaque.

### Level 3: Everything Behind an API (Worst)
The entire harness *and* long-term memory behind an API — e.g., Anthropic's Claude Managed Agents. Zero ownership. Zero visibility. The provider controls what's exposed and what isn't.

## The Incentive Structure

When people say "models will absorb the harness," what they really mean is that memory-related functionality will move behind provider APIs. Model providers are incentivized to do this:

- Memory creates stickier lock-in than model quality alone
- Users who accumulate memory in a platform are much harder to lose
- The data flywheel (more usage → better memory → better experience → more usage) compounds the lock-in over time

Chase's examples of this already happening:
- [[Anthropic]] launched Claude Managed Agents — "literally everything behind an API"
- [[Codex]] (open source) generates **encrypted compaction summaries** not usable outside OpenAI's ecosystem

## The Open Alternative

Chase advocates for open harnesses where:
- The harness code is open source and inspectable
- Memory is stored in databases you own (Mongo, Postgres, Redis)
- The harness is model-agnostic — you can swap providers without losing memory
- Standards are open (agents.md, skills specifications)

[[Deep Agents]] is [[LangChain]]'s implementation of this vision.

> [!warning] Consider the source
> This framework is articulated by the CEO of [[LangChain]], whose business model depends on the harness layer remaining independent of model providers. The argument is sound, but the motivation is commercial. It's also worth noting that tight integration between harness and model can produce better developer experiences — lock-in may be a rational trade in some cases.

## The "Fat Skills" Counter-Argument

[[Garry Tan]] ([[Thin Harness, Fat Skills (Garry Tan)|"Thin Harness, Fat Skills"]]) challenges the premise of the lock-in argument from a different angle than the "tight integration is worth it" trade-off:

If the valuable artifacts in your system are [[Skill Files]] — portable markdown procedures — rather than memory accumulated inside the harness, then harness lock-in matters less. Skills are just files. They work with any harness. The value is inherently portable.

This doesn't fully resolve the tension. Cross-session memory (what [[Harrison Chase|Chase]] worries about) and skill files (what [[Garry Tan|Tan]] values) are different things. You can have portable skills and still lose your memory when switching harnesses. But it does reframe the question: **is the durable value in what the agent remembers, or in what it knows how to do?**

## Related Concepts

- [[Agent Memory]] — what gets locked in
- [[Agent Harness]] — the layer that controls memory
- [[Deep Agents]] — the open-source response
- [[Thin Harness, Fat Skills]] — the counter-architecture where value lives in portable skills
- [[Skill Files]] — the portable alternative to harness-bound memory
- [[Jevons Paradox]] — cheaper software creates more demand; memory lock-in is how providers capture value from that expanded demand
