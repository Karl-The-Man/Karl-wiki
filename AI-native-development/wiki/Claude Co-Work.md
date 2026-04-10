---
type: entity
title: Claude Co-Work
created: 2026-04-10
updated: 2026-04-10
sources: [Building-Claude-Code-with-Boris-Cherny.md]
tags: [tool, anthropic, agentic-ai, non-engineers]
---

# Claude Co-Work

**[[Anthropic]]**'s product that brings [[Claude Code]]'s agentic capabilities to non-engineers. Runs in the Claude desktop app (Electron/TypeScript) as a tab alongside code and chat.

## Origins

- Built in approximately **10 days** by a small team, entirely with [[Claude Code]]
- Emerged from a [[Latent Demand]] signal: non-engineers at Anthropic (finance, sales, data scientists) were already jumping through hoops to use Claude Code
- Growth trajectory is steeper than Claude Code's initial trajectory — described as "an instant hit"

## Architecture and Safety

Runs [[Claude Code]] inside a **virtual machine** with additional safety layers beyond what Claude Code itself provides:

- VM isolation
- Additional classifiers
- OS-level integrations to prevent accidental file deletion
- Chrome extension with its own permission model

This layered approach reflects the [[Swiss Cheese Model (Safety)]] — extra protections are needed because non-technical users may not recognize risky operations.

## Use Cases

[[Boris Cherny]] uses Co-Work for **weekly project management**: it reads a spreadsheet, identifies missing status updates, and pings engineers on Slack.

Other non-engineer uses at [[Anthropic]]:
- DevRel automating video generation for launches
- Finance team coding with Claude Code
- Sales team using agentic tools daily

## Platform

- Launched Mac-only first (Windows planned), following Anthropic's pattern of launching early and iterating
- Built on Electron by Felix, an early Electron contributor
