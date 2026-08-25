# Continuous Agent Grounding

**Microsoft Global Hackathon 2026**  
**Executive Challenge:** *Hack for Continuous Agent Improvement* (Kevin Scott, CTO)

Live primary-data grounding for AI agents via MCP tools.  
Agents stop guessing from web search and start standing on timestamped, structured data.

> Agents improve only when grounded in reliable real-world signals.

---

## The Problem

Most AI agents still answer the old way:

- Search the web
- Reconcile conflicting sources
- Calculate averages
- Keep searching

This is the **confidence trap** — fluent answers built on incomplete or outdated data. There is no durable ground truth, so the agent cannot systematically get better.

**Real example (24 Aug 2026):** a frontier model asked for current daily transit counts through Hormuz, Suez, Malacca and Panama spent **2 minutes 17 seconds** reconciling 7+ websites (AIS vs canal authorities vs Kpler vs UKMTO) and still returned approximate numbers with heavy caveats.

Details: [docs/example-chatgpt-chokepoints.md](docs/example-chatgpt-chokepoints.md)

---

## The Solution

A live primary-data layer that agents call as native MCP tools:

- **Sugra API** — 1500+ live endpoints (macro, maritime, markets, news, climate, entities…)
- **MCP Server** — turns the catalog into agent tools (`search`, `describe`, `call`)
- **Structured responses** — observation dates, ObjectIDs and full provenance on every payload
- **Critic / evaluation** — the same live feed is used as ground truth for continuous improvement

Result: the agent reaches for live data first instead of searching.

---

## Demo

Before / after comparison using the same question:

> “What is the current daily shipping activity through the main global chokepoints (Hormuz, Suez, Malacca, Panama)?”

| | Without live grounding | With Live-Grounding-Agent |
|---|---|---|
| Stack | Web search | Azure AI Foundry (`gpt-5-mini`) + Sugra MCP |
| Latency | 2 min 17 sec | Seconds |
| Output | Conflicting sources, averages, caveats | Exact vessel counts by type + timestamps |
| Provenance | Mixed secondary pages | Source, observation date, ObjectID |

The final demo video (1:29) is on the [Innovation Studio project page](https://url.sugra.ai/hack2026).

Demo script: [docs/demo-script.md](docs/demo-script.md)

---

## Architecture

```text
User Question
     ↓
Azure AI Foundry Agent (gpt-5-mini)
     ↓
MCP Tools  →  Sugra API (live primary data)
     ↓
Structured JSON with provenance
     ↓
Accurate, timestamped answer
     ↓
Same feed used as critic ground truth
     ↓
Continuous improvement signal
```

Full write-up: [docs/architecture.md](docs/architecture.md)

---

## Repository Structure

```text
.
├── docs/
│   ├── architecture.md
│   ├── demo-script.md
│   ├── example-chatgpt-chokepoints.md
│   └── problem.md
├── examples/
│   └── agent-demo/
├── resources/
│   └── links.md
├── LICENSE
└── README.md
```

---

## Links

- **Innovation Studio:** [https://url.sugra.ai/hack2026](https://url.sugra.ai/hack2026)
- **Sugra API:** [https://sugra.ai](https://sugra.ai)
- **API docs:** [https://docs.sugra.ai](https://docs.sugra.ai)
- **MCP endpoint:** [https://app.sugra.ai/mcp](https://app.sugra.ai/mcp)
- **MCP package:** [sugra-api-mcp](https://github.com/Sugra-Systems/sugra-api-mcp)

Blog posts:

- [The Confidence Trap](https://url.sugra.blog/conftrap)
- [AI Needs Live Data](https://url.sugra.blog/ailive)

---

**Team:** Arman Obosyan  
**Hackathon:** Microsoft Global Hackathon 2026  
**License:** MIT
