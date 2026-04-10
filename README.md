# Karl-wiki

Personal knowledge base: articles, podcasts, essays, anything worth keeping.
An LLM builds cross-references across everything ingested; you query against the full corpus.

Built on the [LLM Wiki](PROMPT.md) pattern. Each wiki has three layers:

- **`raw/`** - immutable source documents (articles, transcripts, PDFs)
- **`wiki/`** - LLM-generated markdown pages (entities, concepts, summaries, index, log)
- **`CLAUDE.md`** - schema defining structure, conventions, and workflows

Browsed in [Obsidian](https://obsidian.md).

## Usage

1. Fork this repo (or start fresh with [PROMPT.md](PROMPT.md))
2. Open a wiki directory in Obsidian
3. Point your LLM agent at the directory. It reads `CLAUDE.md` for conventions.
4. Drop sources into `raw/` and tell the LLM to ingest

See [PROMPT.md](PROMPT.md) for the full pattern description.

All credit to Andrej Karpathy:
https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

