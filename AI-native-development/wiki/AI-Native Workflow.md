---
type: concept
title: AI-Native Workflow
created: 2026-04-10
updated: 2026-04-13
sources: [Building-Claude-Code-with-Boris-Cherny.md, Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md, From Hierarchy to Intelligence.md, Thin Harness, Fat Skills.md]
tags: [methodology, workflow, ai-native]
---

# AI-Native Workflow

The emerging set of practices for software development where AI is the primary author of code and the human's role shifts to direction, review, and judgment. Best documented through [[Boris Cherny]]'s daily workflow at [[Anthropic]].

## Boris Cherny's Workflow (Most Documented Example)

- Ships **20–30 PRs per day** with zero hand-written code
- Uses **five terminal tabs**, each with a separate repo checkout, round-robining between parallel [[Claude Code]] sessions
- Starts almost every session in **plan mode** — getting the plan right before implementation
- Overflows to the **Claude desktop and iOS apps** — roughly a third to half of code written from his phone
- **Uninstalled his IDE** after Opus 4.5
- Writes no code manually; doesn't edit single lines

> "I'll be honest, it writes better code than I do." — Boris Cherny

## Key Principles

### Plan first, then execute
Boris uses plan mode (shift-tab twice in Claude Code) to align on approach before the model writes any code. The human's value is in direction, not implementation.

### Parallel context management
Running multiple Claude sessions simultaneously, context-switching between them as each works. Boris calls this "the year of ADHD" — the workflow rewards rapid context-switching over deep single-threaded focus.

### Code review, not code writing
Every PR at Anthropic goes through:
1. **AI review** — Claude (via [[Claude Agent SDK]] in CI) catches ~80% of bugs
2. **Human review** — an engineer must approve every change
The human's role is judgment and review, not authorship.

### Beginner's mindset
> "The model is improving so quickly that the ideas that worked with the old model might not work with the new model... you just always have to bring this beginner mindset." — Boris Cherny

It's now valid to **retry previously-failed ideas** every few months because model capability improves. New/junior engineers sometimes outperform experienced ones because they don't carry assumptions about what the model can't do.

### Low-cost experimentation
With near-zero cost of building, the workflow shifts from specification to experimentation. See [[Prototyping Over PRDs]].

## Tooling

- **[[Claude Code]]** — terminal-based agentic coding
- **[[Claude Co-Work]]** — same capabilities for non-engineers
- **[[Agent Teams]]** — swarms for complex tasks
- **[[Best of N]]** — parallel agents for determinism
- **[[Agentic Search]]** — grep/glob instead of RAG

## Andrej Karpathy's Workflow (Independent Confirmation)

[[Andrej Karpathy]] independently converged on the same pattern, providing external validation that this workflow generalizes beyond [[Anthropic]]:

- Went from 80/20 manual/agent to effectively **0/100 since December 2025**
- Hasn't typed a line of code since December
- Runs multiple agents in parallel ([[Claude Code]], [[Codex]]), switching between them
- Works in [[Macro Actions]] — assigning whole functionalities to agents, not writing functions
- Calls the resulting state "[[AI Psychosis]]" — perpetual awareness of infinite possibility
- Frames productivity as [[Token Throughput]] — "What token throughput do you command?"
- Built persistent autonomous agents ([[Claws]]) that run without his involvement

> "Literally, if you just find a random software engineer at their desk and what they're doing, their default workflow of building software is completely different as of basically December."

This is significant because Karpathy is not an Anthropic employee and uses competing tools — suggesting the AI-native workflow pattern is tool-agnostic.

## Who Can Use This Workflow

Not limited to engineers. At [[Anthropic]]:
- Designers code
- Data scientists code
- Finance people code
- Sales people code
- DevRel automates video generation

This supports the [[Generalist vs Specialist]] thesis — AI-native workflows dissolve traditional role boundaries.

## From Individual to Organization

The AI-native workflow pattern doesn't stop at individuals. [[Jack Dorsey]]'s [[From Hierarchy to Intelligence]] extends the same structural move to the organizational level:

- **Individual:** human orchestrates agents → agents write code → human reviews
- **Organization:** AI maintains [[World Model (Organizational)|world models]] → [[Intelligence Layer]] composes solutions → humans operate at the edge

Both share the same logic: AI takes over the coordination function that humans used to perform. At the individual level, it replaces the developer's manual coding. At the organizational level, it replaces [[Hierarchy as Information Routing|hierarchy's information routing]]. See [[Company as Intelligence]].

## The Compounding Workflow: Never Do One-Off Work

[[Garry Tan]] ([[Thin Harness, Fat Skills (Garry Tan)|"Thin Harness, Fat Skills"]]) adds a discipline layer to the AI-native workflow: **every recurring task must become a [[Skill Files|skill file]].**

> If I ask you to do something and it's the kind of thing that will need to happen again, you must: do it manually the first time on 3 to 10 items. Show me the output. If I approve, codify it into a skill file. If it should run automatically, put it on a cron. The test: if I have to ask you for something twice, you failed.

This transforms the workflow from *productive* to *compounding*. Each session doesn't just produce output — it produces a permanent capability upgrade. Skills never degrade, run at 3 AM, and automatically improve with each new model. Tan claims this discipline is how you reach [[Steve Yegge]]'s 100x productivity multiplier.

## Related Concepts

- [[Prototyping Over PRDs]] — a product development practice enabled by this workflow
- [[Generalist vs Specialist]] — the career implications
- [[The Printing Press Analogy]] — the historical frame for this transition
- [[Understand the Layer Under]] — what to learn to be effective in this workflow
- [[AI Psychosis]] — the emotional experience of this workflow
- [[Token Throughput]] — the productivity metric
- [[Macro Actions]] — the unit of work
- [[Claws]] — the next evolution: persistent autonomous agents
- [[Company as Intelligence]] — the organizational-level extension of this workflow
- [[Skill Files]] — the mechanism for compounding capability
- [[Thin Harness, Fat Skills]] — the architecture for the compounding workflow
