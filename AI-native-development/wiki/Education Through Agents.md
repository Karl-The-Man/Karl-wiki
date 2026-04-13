---
type: concept
title: Education Through Agents
created: 2026-04-11
updated: 2026-04-13
sources: [Andrej Karpathy on Code Agents, AutoResearch, and the Loopy Era of Al.md, Thin Harness, Fat Skills.md]
tags: [education, agents, future]
---

# Education Through Agents

[[Andrej Karpathy]]'s thesis that education is being redirected through AI agents — teachers explain to agents, and agents explain to humans with infinite patience, at their level, in their language.

> "I'm not explaining to people anymore. I'm explaining it to agents. If you can explain it to agents, then agents can be the router."

## How It Works

Traditional: Teacher → Student (one explanation, one pace, one language)

New: Teacher → Agent → Student (agent adapts explanation to the individual)

- If a student doesn't understand a function, they ask the agent to explain it three different ways
- The agent targets the explanation to the human's capability level and language
- The teacher's job shifts to: (1) creating the artifact, (2) writing "skills" — hints that script the curriculum an agent should follow

## The microGPT Example

Karpathy initially planned to make an explanatory video for [[microGPT]] (his traditional approach). He realized this was unnecessary:

- The code is already simple enough (200 lines)
- Anyone can ask their agent to explain it in various ways
- Instead, he envisions writing a "skill" — a progression the agent should take someone through

## What Humans Still Contribute

> "I tried to get an agent to write microGPT. I told it: try to boil down neural networking to the simplest thing. It can't do it."

The **creative reduction** — the few bits of insight that produce a uniquely simplified artifact — is still the human's domain. Everything downstream (explanation, teaching, adaptation) is the agent's domain.

> "The things that agents can't do is your job now. The things that agents can do, they can probably do better than you, or very soon."

## Documentation Implications

- Library documentation should shift from **HTML for humans** to **markdown for agents**
- If agents understand the documentation, they can explain all parts of it to any user
- This is "redirection through agents" — an intermediate layer between creator and consumer

## Skill Files as the New Medium

[[Garry Tan]]'s [[Skill Files]] concept gives concrete form to Karpathy's vision. When Karpathy says he'd write a "skill" that scripts a curriculum, Tan has the architecture: a markdown file with steps, parameters, and judgment encoded. The skill-as-method-call pattern (same procedure, different arguments) maps directly to Karpathy's idea of an agent adapting explanation to the individual — the skill defines the process, the invocation adapts to the learner.

Tan's framing: "This is software design, using markdown as the programming language and human judgment as the runtime." This is exactly what Karpathy describes when he says his job is now creating the artifact (the creative reduction) and writing skills that agents use to teach it.

## Related Concepts

- [[microGPT]] — the case study for education through agents
- [[Agentic Web]] — documentation for agents is part of the broader agent-first shift
- [[Generalist vs Specialist]] — agents handle the specialist explanation; humans contribute the generalist insight
- [[Skill Files]] — the concrete implementation of education-through-agents
- [[Resolvers]] — how the right educational skill gets loaded for the right learner
