---
type: overview
title: AI-Native Development — Overview
created: 2026-04-10
updated: 2026-04-13
sources: [Building-Claude-Code-with-Boris-Cherny.md, Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md, From Hierarchy to Intelligence.md, Your harness, your memory.md, Thin Harness, Fat Skills.md]
tags: [overview]
---

# AI-Native Development — Overview

This wiki tracks the emerging landscape of **AI-native development** — building software, products, workflows, and organizations that are designed from the ground up to leverage AI capabilities.

## Current State

The wiki draws on five sources:

1. **[[Building Claude Code with Boris Cherny]]** — Pragmatic Engineer podcast with the creator of [[Claude Code]] at [[Anthropic]]. The most detailed first-person account of a fully AI-native engineering workflow inside a frontier lab — including concrete numbers (80% of code AI-written, 20–30 PRs/day, zero hand-written code) and architectural decisions (abandoning RAG for [[Agentic Search]], [[Prototyping Over PRDs]]).

2. **[[Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of AI]]** — No Priors podcast with one of the most credible voices in AI. Provides independent external validation of the AI-native workflow pattern, plus original frameworks: [[AutoResearch]] (autonomous ML experimentation), [[Claws]] (persistent autonomous agents), [[Token Throughput]] as the new productivity metric, and a vision for the trajectory from digital to physical AI.

3. **[[From Hierarchy to Intelligence]]** — [[Jack Dorsey]]'s manifesto on replacing organizational hierarchy with AI at [[Block]]. Extends the AI-native thesis from individual developer workflow to company-wide organizational design. Argues hierarchy is an [[Hierarchy as Information Routing|information routing protocol]] constrained by human span-of-control limits for 2,000 years, and that AI can finally break this constraint through [[World Model (Organizational)|world models]] and an [[Intelligence Layer]].

4. **[[Your harness, your memory (Harrison Chase)]]** — [[Harrison Chase]] ([[LangChain]] CEO) on the relationship between [[Agent Harness|agent harnesses]] and [[Agent Memory]], arguing that closed harnesses create dangerous [[Memory Lock-In|vendor lock-in]] because memory is inseparable from the harness. The first source to introduce a critical external perspective on the infrastructure layer — not just how agents are used, but who owns what they learn.

5. **[[Thin Harness, Fat Skills (Garry Tan)]]** — [[Garry Tan]] (YC president) on the architecture that separates 2x from 100x AI users. Proposes a specific three-layer stack: fat [[Skill Files]] (markdown procedures encoding judgment) on top, a thin harness (~200 lines) in the middle, deterministic tooling on the bottom. Introduces five definitions — [[Skill Files]], the harness, [[Resolvers]], [[Latent vs Deterministic]], and [[Diarization]] — and illustrates all five in a detailed case study of YC's Startup School matching system. **Directly contradicts** source 4: where Chase says the harness is the key layer (512k lines, memory inseparable), Tan says the harness should be thin and the value lives in portable skills.

The first two sources are strikingly convergent: Boris Cherny (inside Anthropic) and Andrej Karpathy (independent, using multiple tools) independently describe the same fundamental shift — humans no longer write code; they orchestrate agents in parallel. The third source extends this pattern to the organizational level: if AI can replace individual code authorship, it can also replace the information routing that justifies management hierarchy.

## Key Themes

### The workflow revolution is confirmed by multiple sources
[[Boris Cherny]] ships 20–30 PRs daily with zero hand-written code. [[Andrej Karpathy]] hasn't typed a line of code since December 2025. Both run parallel agent sessions and describe a qualitative shift in what developers do. See [[AI-Native Workflow]], [[Macro Actions]].

### Simpler architectures win
The [[Claude Code]] team abandoned RAG for [[Agentic Search]]. Karpathy's [[AutoResearch]] uses simple loops with objective metrics rather than sophisticated pipelines. Both embody [[The Bitter Lesson]]: give the model tools and get out of the way.

### The "loopy era" — persistent autonomous agents
Beyond interactive coding agents, [[Claws]] represent persistent, looping entities with their own sandboxes, memory, and personality. Karpathy's Dobby manages his home; [[Peter Steinberger]]'s [[OpenClaw]] innovates in memory and personality design. [[AutoResearch]] is a specialized claw for ML experimentation.

### Safety requires layered defense
[[Swiss Cheese Model (Safety)|Swiss cheese model]]: model alignment, runtime classifiers, sub-agent summarization, permission prompts, and VM isolation. Karpathy also expresses caution about giving agents full access to his digital life — "I'm still a little suspicious."

### The generalist is ascendant
Both sources agree: strong opinions about languages and frameworks are losing value. [[Generalist vs Specialist|Multi-disciplinary generalists]] who can think across domains are rising. Karpathy embodies this — his work spans research, education, tools, and public commentary.

### Cheaper software creates more demand
[[Jevons Paradox]]: as AI makes software cheaper to produce, demand explodes rather than contracts. This is the economic mechanism underlying [[The Printing Press Analogy]] — scribes became authors in a larger market; engineers become orchestrators in a larger market.

### AI capabilities are jagged
[[Jaggedness]]: models are simultaneously brilliant in verifiable domains (code, math) and stagnant in non-verifiable ones (humor, nuance). This is a structural consequence of RL optimization. It suggests [[Model Speciation]] — specialized models rather than one monoculture oracle.

### The trajectory: digital → interface → physical
[[Digital-Physical Interface]]: digital transformation first (massive, fast), then sensors/actuators as the interface, then full physical world (biggest TAM, slowest). Atoms are "a million times harder."

### Education is being redirected through agents
[[Education Through Agents]]: teachers explain to agents; agents explain to humans. Documentation shifts from HTML for humans to markdown for agents. "I'm not explaining to people anymore."

### The harness layer is permanent — and politically contested
[[Harrison Chase]] argues that [[Agent Harness|agent harnesses]] are not going away — even [[Claude Code]] has 512k lines of harness code. But who controls the harness controls [[Agent Memory]], and memory is what makes agents personalized, sticky, and defensible. [[Garry Tan]] agrees the harness is permanent but makes the opposite architectural prescription: keep it **thin** (~200 lines), and put the value in [[Skill Files]] — portable markdown procedures that encode judgment. This creates a three-way debate:

1. **Chase:** the harness is fat and critical; the risk is [[Memory Lock-In]]
2. **Tan:** the harness should be thin; the value is in portable skills, not harness-bound memory
3. **Anthropic (implicit):** tight model-harness integration produces the best product; Claude Code's local-first design (CLAUDE.md, local memory files) mitigates the lock-in concern

The unresolved question: **is the durable value in what the agent remembers (memory), or in what it knows how to do (skills)?** See [[Thin Harness, Fat Skills]], [[Memory Lock-In]].

### Skills as the unit of value — and the mechanism for compounding
[[Garry Tan]]'s [[Skill Files]] are reusable markdown procedures that work like method calls — same skill, different parameters, radically different capabilities. The "never do one-off work" discipline means every recurring task becomes a skill, and skills on cron become [[Claws]] by another name. Skills can even rewrite themselves through feedback loops (YC's matching skills improved from 12% to 4% "OK" ratings without code changes). This connects to [[Andrej Karpathy]]'s [[AutoResearch]] (autonomous experimentation loops) and [[Education Through Agents]] (skills as curriculum). The architecture: push intelligence up into skills, push execution down into deterministic tooling ([[Latent vs Deterministic]]), keep the harness thin.

### From individual workflow to organizational design
[[Jack Dorsey]]'s [[From Hierarchy to Intelligence]] extends the AI-native thesis from how individuals work to how companies are structured. [[Block]] is attempting to replace the management hierarchy — an [[Hierarchy as Information Routing|information routing protocol]] unchanged for 2,000 years — with a [[Company as Intelligence|company organized as an intelligence]]. Two [[World Model (Organizational)|world models]] (company + customer) replace managers' contextual knowledge. An [[Intelligence Layer]] composes atomic capabilities into proactive customer solutions, replacing the PM-driven roadmap. Three roles (ICs, DRIs, player-coaches) replace the traditional management pyramid. This is the logical extension of the workflow revolution: if AI can replace code authorship, it can replace the coordination layer too.

## Key Questions to Explore

- How does the AI-native workflow generalize to organizations outside AI labs and beyond power users like Karpathy?
- What do competing tools (Cursor, Copilot, Windsurf) look like through the same analytical lens?
- What are the failure modes and limits of [[AutoResearch]] — where does autonomous experimentation break down?
- How does [[Distributed Auto Research]] actually work in practice? Can untrusted compute pools really compete with frontier labs?
- What is the right architecture for [[Claws]] — memory systems, personality, interface?
- How does [[Jaggedness]] evolve as models improve — does it narrow or persist?
- When does [[Model Speciation]] actually happen at scale?
- Can [[Block]]'s [[Company as Intelligence]] model survive contact with reality? What breaks first?
- Does the organizational intelligence model generalize beyond fintech, where transaction data provides uniquely rich signal?
- What governance layer prevents the [[Intelligence Layer]] from composing harmful or unwanted solutions?
- Is [[Memory Lock-In]] a real structural risk, or does the better developer experience of integrated systems justify the trade-off? Does the [[Thin Harness, Fat Skills]] model dissolve the concern by putting value in portable skills instead of harness-bound memory?
- Will open standards (agents.md, skills) create enough interoperability to make harness switching practical, or will memory formats fragment?
- How does [[Agent Memory]] evolve as it matures past its "infancy" — do common abstractions emerge that make memory portable?
- When do self-rewriting [[Skill Files]] go wrong? What happens when a skill encodes bad judgment and compounds it through feedback loops?
- Is "~200 lines" a realistic harness, or is Claude Code's 512k lines the honest answer? Where is the real boundary between infrastructure and harness?

## Thesis (Evolving)

AI-native development is not an incremental improvement to existing workflows — it's a qualitative shift in what developers do, and ultimately in how companies are organized. The human role moves from code authorship to direction, judgment, and review. This shift is now confirmed by multiple independent sources: an Anthropic insider (Boris Cherny), an independent researcher (Andrej Karpathy), and a CEO redesigning a major company around it (Jack Dorsey/Block).

The pattern operates at two levels. At the **individual level**: [[Claws]] that loop without human involvement, [[AutoResearch]] that optimizes overnight, agents that manage physical infrastructure. The tools are simple (grep, not RAG; loops, not pipelines); the safety is layered (Swiss cheese); the culture is experimental (prototypes, not PRDs). At the **organizational level**: [[Block]] is attempting to replace the management hierarchy itself with AI — [[World Model (Organizational)|world models]] that replace managers' contextual knowledge, an [[Intelligence Layer]] that composes solutions without PM roadmaps, and a flat structure of three roles with no permanent middle management.

The economic trajectory follows [[Jevons Paradox]]: cheaper software production creates more demand, not less. The capability trajectory follows [[Digital-Physical Interface]]: digital first (fast), then sensors/actuators (medium), then full physical (slow, big). The intelligence trajectory faces [[Jaggedness]]: brilliant on-rails, mediocre off-rails, with [[Model Speciation]] as the potential structural response. The organizational trajectory follows [[Company as Intelligence]]: if AI is just cost optimization, you get absorbed; the durable advantage is compounding understanding.

The historical parallel remains [[The Printing Press Analogy]]: scribes became authors; the market for literature exploded. Engineers will become orchestrators; the market for software will explode. And as [[Jack Dorsey]] argues, [[Hierarchy as Information Routing|hierarchy]] — the organizational form that has governed every large institution for 2,000 years — may finally have an alternative. But as Karpathy notes, if you're not pushing the frontier of what's possible, "everything is [[Skill Issue]]."

A structural tension has emerged that now has **two opposing frameworks**:

**Framework 1 — "Your harness, your memory" ([[Harrison Chase]]):** [[Agent Harness|Agent harnesses]] are permanent, [[Agent Memory]] is inseparable from the harness, and closed harnesses create [[Memory Lock-In]] that model providers are incentivized to exploit. The open harness movement ([[Deep Agents]], [[OpenClaw]], [[Letta]]) is the alternative.

**Framework 2 — "Thin harness, fat skills" ([[Garry Tan]]):** The harness should be deliberately thin (~200 lines). The value lives in [[Skill Files]] — portable markdown procedures encoding judgment and process. Skills are inherently portable (they're just files), so harness lock-in matters less. The real architecture question is not who owns the harness, but whether you're putting intelligence in the right layer: skills for judgment, deterministic code for execution, a thin harness in between.

These frameworks aren't fully contradictory — Chase worries about cross-session memory, Tan focuses on procedural knowledge — but they prescribe opposite architectures. Chase says the harness is fat and critical; Tan says it should be thin and replaceable. The unresolved question: **is the durable value in what the agent remembers, or in what it knows how to do?** This may be the defining architectural question of the agent era — and the answer may vary by use case.
