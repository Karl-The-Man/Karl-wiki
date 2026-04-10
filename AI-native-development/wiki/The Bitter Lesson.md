---
type: concept
title: The Bitter Lesson
created: 2026-04-10
updated: 2026-04-10
sources: [Building-Claude-Code-with-Boris-Cherny.md]
tags: [principle, architecture, ai-philosophy]
---

# The Bitter Lesson

Originally articulated by Rich Sutton: the biggest lesson from AI research is that general methods that leverage computation are ultimately the most effective, and engineering clever domain-specific solutions tends to lose out.

## Boris Cherny's Corollary

[[Boris Cherny]] extends the Bitter Lesson with a practical corollary for building AI-native tools:

> "The model is its own thing. You give it tools. You let it run programs. You let it write programs. But you don't make it a component of this larger system... This is one of the corollaries — just let the model do its thing. Don't try to put it in a box."

The wrong approach: stubbing out a module and saying "this is now AI" — making the model a component in an engineered pipeline. The right approach: give the model tools and autonomy, and let it figure out how to accomplish the task.

## Concrete Examples

### Agentic Search over RAG
The [[Claude Code]] team abandoned RAG (an engineered retrieval pipeline) in favor of [[Agentic Search]] (just giving the model grep and glob). The less-engineered approach won because the model could search more flexibly and adaptively than a fixed retrieval system.

### Agent Teams
[[Agent Teams]] / [[Uncorrelated Context Windows]]: rather than engineering a sophisticated coordination protocol between agents, they spawn independent agents with fresh contexts and let them work. More compute, less engineering.

### Tool use emergence
When Claude Code was given a bash tool, "the model just wants to use tools" — it figured out how to accomplish tasks the developers hadn't anticipated (e.g., writing AppleScript to query the music player).

## Implications for AI-Native Development

- **Don't over-engineer around the model** — give it tools and get out of the way
- **Expect to be surprised** — the model will use tools in ways you didn't anticipate
- **Retry failed ideas periodically** — what didn't work with an older model may work with a newer one, because the general capability improved
- **Favor simple, general tools** over domain-specific retrieval systems

## Related Concepts

- [[Agentic Search]] — concrete example of the Bitter Lesson in action
- [[Uncorrelated Context Windows]] — more compute beats more engineering
- [[Agent Teams]] — swarms as a Bitter Lesson application
