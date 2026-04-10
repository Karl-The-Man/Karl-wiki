---
type: concept
title: Jaggedness
created: 2026-04-11
updated: 2026-04-11
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [ai-capabilities, limitations, rl]
---

# Jaggedness

[[Andrej Karpathy]]'s term for the wildly uneven capability profile of current AI models — simultaneously superhuman in some domains and childlike in others.

> "I simultaneously feel like I'm talking to an extremely brilliant PhD student who's been a systems programmer for their entire life, and a 10-year-old. And it's so weird."

## The On-Rails / Off-Rails Dichotomy

The underlying cause is **reinforcement learning**:

- **On rails** (verifiable domains): code correctness, unit tests, math proofs — models excel because these have clear reward signals. "You're part of the superintelligence circuits."
- **Off rails** (non-verifiable domains): humor, nuance, intent, when to ask clarifying questions — models stagnate because these lack clear optimization targets. "Everything kind of meanders."

### The Atoms Joke Test

> "If today you go to state-of-the-art ChatGPT and ask it, 'Tell me a joke,' do you know what joke you're going to get? 'Why do scientists not trust atoms? Because they make everything up.' This is the joke you would get three or four years ago, and this is the joke you still get today."

Despite massive improvements in agentic capability, joke quality hasn't changed — because it's outside the RL optimization loop.

## Why It Matters

1. **Frustration:** "I get so frustrated with the agents all the time still" — the power is real, but models still do "nonsensical things once in a while"
2. **You can't fully let go:** "Even though the progression is obvious... you can't let it fully go there yet because it doesn't fully work"
3. **Transfer doesn't happen cleanly:** The premise that being smarter at code → being better at everything is "not exactly fundamentally what's going on"
4. **[[Skill Issue]] ambiguity:** Sometimes it's skill issue, sometimes it's genuine capability limitation — "it's hard to tell"

## Humans Are Jagged Too — But Less So

> "Jaggedness exists in humans. You can be very, very good at math and still tell a really bad joke."

But models have "a lot more" jaggedness than humans. Human capabilities are more coupled; model capabilities are more decoupled across domains.

## Implications for [[Model Speciation]]

Jaggedness suggests that the monoculture approach (one model good at everything) may be structurally limited. If different capabilities require different optimization, perhaps models should speciate — specializing in domains where RL can be applied effectively.

## Related Concepts

- [[Model Speciation]] — the structural response to jaggedness
- [[Skill Issue]] — when jaggedness masquerades as user error
- [[AutoResearch]] — works best in verifiable (on-rails) domains
- [[The Bitter Lesson]] — models improve where RL can be applied; not everywhere
