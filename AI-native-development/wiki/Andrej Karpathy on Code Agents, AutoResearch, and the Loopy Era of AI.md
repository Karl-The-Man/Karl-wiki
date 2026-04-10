---
type: source-summary
title: Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of AI
created: 2026-04-11
updated: 2026-04-11
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md]
tags: [podcast, no-priors, karpathy, agents, auto-research, claws]
---

# Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of AI

Long-form interview on the **No Priors** podcast with [[Andrej Karpathy]], covering his daily experience with code agents, the [[AutoResearch]] paradigm, [[Claws]] as persistent autonomous agents, the future of open source vs closed models, and the trajectory from digital to physical AI.

## Summary

Karpathy describes a "December flip" — going from 80/20 manual/agent coding to effectively 0/100 since December 2025. He calls this state "[[AI Psychosis]]" — an overwhelming awareness of what's now possible combined with the feeling that everything is [[Skill Issue]]. His framework: maximize your [[Token Throughput]], remove yourself as the bottleneck, work in [[Macro Actions]] over your codebase. The podcast covers his [[AutoResearch]] system (autonomous ML experimentation that beat his hand-tuning on [[NanoGPT]]), his "Dobby" [[Claws|claw]] that manages his smart home, the [[Jevons Paradox]] for software, [[Jaggedness]] of current models, [[Model Speciation]], [[Recursive Self-Improvement]], and a vision for [[Distributed Auto Research]] via untrusted compute pools.

## Key Claims

- Hasn't typed a line of code since December 2025; the shift happened almost overnight
- Everything that doesn't work feels like [[Skill Issue]] — the capability is there, you just haven't found the right prompting/orchestration
- [[Token Throughput]] is the new GPU utilization — "What token throughput do you command?"
- [[AutoResearch]] found improvements in a well-tuned [[NanoGPT]] repo overnight that Karpathy missed after two decades of experience (weight decay on value embeddings, Adam beta tuning, joint interactions)
- Research organizations can be described as markdown files ([[program.md]]); you can meta-optimize these
- Current models are simultaneously "an extremely brilliant PhD student who's been a systems programmer for their entire life, and a 10-year-old" — the [[Jaggedness]]
- RL-trained capabilities (verifiable domains) advance rapidly; non-verifiable capabilities stagnate (the atoms joke hasn't changed in years)
- Expects [[Model Speciation]] — specialized models like the animal kingdom, not a monoculture oracle
- Open-source models lag closed frontier by ~6–8 months (down from 18 months), and that's a healthy dynamic; draws Linux analogy
- [[Jevons Paradox]]: cheaper software → more demand → more engineering jobs (ATM/bank teller precedent)
- Digital transformation will massively outpace physical; atoms are "a million times harder"
- Apps should become APIs; agents are the intelligent glue; the customer is no longer the human but agents acting on behalf of humans ([[Agentic Web]])
- Education is being redirected through agents — explain to agents, not to humans; documentation should be markdown for agents, not HTML for humans ([[Education Through Agents]])
- Frontier labs have systemic concentration risk; being inside one limits your independence; ideal is going back and forth

## Entities Mentioned

- [[Andrej Karpathy]] — interviewee, independent AI researcher and educator
- [[Peter Steinberger]] — famous for parallelized [[Codex]] agent workflow; creator of [[OpenClaw]]
- [[OpenClaw]] — Peter's claw project with sophisticated memory, personality ("soul document"), WhatsApp portal
- [[NanoGPT]] / [[microGPT]] — Karpathy's projects for boiling LLM training to bare essence
- [[Codex]] — OpenAI's coding agent, mentioned alongside [[Claude Code]]
- [[Claude Code]] — Anthropic's coding agent, praised for personality calibration
- [[OpenAI]] — frontier lab; Karpathy's former employer
- [[Anthropic]] — frontier lab; maker of Claude

## Concepts Discussed

- [[AI Psychosis]] — the overwhelming state of possibility awareness
- [[Token Throughput]] — the new productivity metric
- [[Skill Issue]] — when failure feels like user error, not capability limitation
- [[Macro Actions]] — working in units of "new functionality" not "new function"
- [[Claws]] — persistent, looping, sandboxed autonomous agents
- [[AutoResearch]] — autonomous ML experimentation loops
- [[Recursive Self-Improvement]] — LLMs improving LLMs; the core game frontier labs are playing
- [[Distributed Auto Research]] — SETI@home for AI research; untrusted compute pools
- [[Agentic Web]] — agent-first tools, APIs over apps
- [[Jevons Paradox]] — cheaper software creates more demand
- [[Jaggedness]] — uneven AI capabilities across domains
- [[Model Speciation]] — specialized models vs monoculture
- [[Digital-Physical Interface]] — sensors/actuators as the next frontier
- [[Education Through Agents]] — teaching agents instead of people

## Notable Quotes

> "I kind of went from 80/20 of writing code by myself versus delegating to agents, to like 20/80. And I don't even think it's 20/80 by now... I don't think I've typed a line of code probably since December."

> "What is your token throughput? And what token throughput do you command?"

> "I simultaneously feel like I'm talking to an extremely brilliant PhD student who's been a systems programmer for their entire life, and a 10-year-old. And it's so weird."

> "The agent part is now taken for granted. Now the claw-like entities are taken for granted. And now you can have multiple of them, and now you can have instructions to them, and now you can have optimization over the instructions... this is infinite and everything is skill issue."

> "Code is now ephemeral, and it can change, and it can be modified."

> "I'm not explaining to people anymore. I'm explaining it to agents."

> "A research organization is a set of markdown files that describe all the roles and how the whole thing connects."

## Source Assessment

**Strengths:** Karpathy is one of the most credible voices in AI — founding member of OpenAI, former Tesla AI director, two decades of hands-on ML research. His experience with [[AutoResearch]] is first-person and empirical, not theoretical. The "December flip" claim is consistent with [[Boris Cherny]]'s account from the same timeframe. The conversation is wide-ranging and produces several original frameworks (token throughput, the loopy era, jaggedness).

**Weaknesses:** Much of the forward-looking commentary (model speciation, distributed auto research, agentic web) is speculative. The podcast is conversational — claims aren't backed by data beyond Karpathy's personal experience. Some important details are vague (e.g., exactly what AutoResearch's architecture looks like). The interviewers from Conviction (a VC firm) occasionally nudge toward their own portfolio framing.
