---
type: concept
title: Agentic Search
created: 2026-04-10
updated: 2026-04-10
sources: [Building-Claude-Code-with-Boris-Cherny.md]
tags: [architecture, rag, code-search, bitter-lesson]
---

# Agentic Search

The approach used by [[Claude Code]] for code understanding: instead of building a RAG (retrieval-augmented generation) pipeline with a local vector database, the model is given **glob and grep as tools** and searches the codebase itself.

> "Agentic search... this is a fancy word for glob and grep. That's all it is." — [[Boris Cherny]]

## Why RAG Was Abandoned

The [[Claude Code]] team initially built RAG with a local vector database but found it inferior:

- **Code drifted out of sync** — the index became stale as the codebase changed
- **Indexing permissions were complex** — especially in enterprise environments
- **Agentic search simply outperformed it** — the model searching on its own was more effective

## How It Works

The model uses glob (file pattern matching) and grep (content search) as tools within its agentic loop. It decides what to search for, reads results, refines its queries, and builds understanding iteratively — the same way a human developer would navigate an unfamiliar codebase.

Boris compares this to how Instagram engineers searched code when click-to-definition was broken in their tooling: they fell back to searching, and it worked well enough.

## Significance

This is a concrete example of [[The Bitter Lesson]]: rather than engineering a sophisticated retrieval system, they gave the model simple tools and let it search. The less-engineered approach won.

It also reflects the principle that AI-native architecture should avoid making the model "a component of a larger system" — instead, give it tools and let it write and run its own programs.

## Related Concepts

- [[The Bitter Lesson]] — let the model do its thing rather than constraining it
- [[AI-Native Workflow]] — agentic search is a building block of the AI-native development experience
- [[Claude Code]] — the tool that implements this approach
