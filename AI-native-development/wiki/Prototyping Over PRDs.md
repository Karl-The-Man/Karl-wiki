---
type: concept
title: Prototyping Over PRDs
created: 2026-04-10
updated: 2026-04-10
sources: [Building-Claude-Code-with-Boris-Cherny.md]
tags: [methodology, product-development, ai-native]
---

# Prototyping Over PRDs

The practice of building working prototypes instead of writing product requirement documents (PRDs), enabled by the near-zero cost of building with AI tools.

> "We don't really write stuff. We just show." — [[Boris Cherny]]

## How It Works at Anthropic

The [[Claude Code]] team's development culture:

- **Prototypes over documents**: When someone has an idea, they build it rather than write about it
- Product lead Cat Woo's philosophy: "better send a PR"
- For the condensed file read view feature: ~30 prototypes were built, followed by a month of internal dogfooding, then iterative external feedback
- Most code is thrown away because the cost of building is so low

## Why This Works Now

The key enabler is the **collapse of prototyping cost**:

> "The cost of building is very low. But also we don't know where we're aiming. So we just have to try and we have to see what feels good." — [[Boris Cherny]]

When building a prototype takes minutes instead of days, the ROI of writing a detailed specification document drops. It's faster to build three versions and compare them than to debate which version to build.

Boris also notes: "Personally I'm wrong like half the time. At least half of my ideas are bad. And I don't know which half until I try it." Cheap prototyping makes this uncertainty manageable.

## Implications

- **PRDs assume you know what to build** — prototyping assumes you don't and need to discover it
- **Shifts product development from specification to experimentation**
- **Reduces the gap between idea and feedback** — stakeholders react to working software, not documents
- Enabled by tools like [[Claude Code]] that make building extremely fast
- Reflects a broader [[AI-Native Workflow]] principle: leverage AI's speed to explore rather than specify

## Related Concepts

- [[AI-Native Workflow]] — prototyping culture is a core component
- [[Generalist vs Specialist]] — prototyping rewards people who can think across disciplines
