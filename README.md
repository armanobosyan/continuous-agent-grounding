# Continuous Agent Grounding

**Microsoft Global Hackathon 2026**  
Executive Challenge: *Hack for Continuous Agent Improvement* (Kevin Scott, CTO)

> Agents improve only when grounded in reliable real-world signals.

## Problem

Most AI agents still rely on:
- Static training data (knowledge cut-off)
- Noisy and inconsistent web search

This creates the **confidence trap** — fluent answers that are outdated, incomplete, or confidently wrong.

**Real example (24 Aug 2026):** A frontier model asked for current daily transit counts through Hormuz / Suez / Malacca / Panama spent 2 minutes 17 seconds reconciling conflicting web sources and still returned approximate numbers with heavy caveats. Without clean primary signals there is no durable ground truth for continuous improvement.

## Solution

We provide a **live primary-data grounding layer** that agents can use as a continuous improvement signal.

### Key components

- **Live Primary Data API** — 1500+ endpoints across markets, macroeconomics, climate, maritime, news, entity screening and more
- **MCP Server** — turns the entire catalog into native agent tools (search, describe, call)
- **LLM-ready responses** — consistent envelope with source attribution + timestamps
- **Critic / Evaluation pattern** — uses the same live data as ground truth

## What we are building during the Hackathon

1. Clear before/after demonstration of agent quality with vs without live grounding (using real live queries such as maritime chokepoints)
2. Lightweight critic & evaluation layer based on live primary data
3. Integration patterns with Microsoft agent surfaces (Azure AI Foundry / Copilot Studio style)
4. Measurable continuous improvement loop

## Repository Structure

```text
.
|   LICENSE
|   README.md
|
+---docs
|       architecture.md
|       demo-script.md
|       example-chatgpt-chokepoints.md
|       problem.md
|
+---examples
|   \---agent-demo
|           README.md
|
\---resources
        links.md
```

## Links

- Project page on Innovation Studio: *(add link after creation)*
- [Sugra API](https://sugra.ai)
- [Sugra MCP](https://github.com/Sugra-Systems/sugra-api-mcp)
- Blog posts:
  - [The Confidence Trap](https://sugra.systems/blog/the-confidence-trap)
  - [AI Needs Live Data](https://sugra.systems/blog/ai-needs-live-data)

## Team

- Arman Obosyan

## License

This repository is created for Microsoft Global Hackathon 2026.
