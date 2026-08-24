# Real-world example: ChatGPT on live shipping chokepoints (24 Aug 2026)

## Query

> What is the current daily shipping activity through the main global chokepoints (Hormuz, Suez, Malacca, Panama)? Give the latest available ship/transit counts by type.

## What happened (observed)

- ChatGPT spent **2 minutes 17 seconds** searching and reconciling data.
- Queried 7+ websites (suezcanal.gov.eg, pancanal.com, Reuters, FT, ishormuzopen.info, financialports.com, etc.).
- Continuously reconciled conflicting methodologies:
  - AIS vs official canal authority counts
  - Different vessel category definitions
  - Different time windows (single-day vs 7-day averages)
- Especially difficult on Hormuz (highly volatile, UKMTO vs AIS/Kpler diverging sharply, traffic ~90% below pre-crisis baseline).
- Final output: approximate daily rates table + many caveats + residual "Other" category.

## Why this is the Confidence Trap

The agent produces a fluent, well-structured answer with numbers, yet:

- Latency is high (real-time operational decisions cannot wait 2+ minutes)
- Numbers remain approximate and methodology-dependent
- Source quality and coverage vary dramatically by chokepoint
- No durable primary-data ground truth that can be reused or used for continuous evaluation

This is exactly the failure mode that prevents continuous agent improvement.

## How Continuous Agent Grounding changes the outcome

With a live primary-data layer + MCP tools:

1. Agent discovers and calls a structured maritime / chokepoint tool.
2. Receives consistent, timestamped, source-attributed numbers in seconds.
3. Critic / evaluation layer can treat the same live feed as ground truth.
4. Over time the agent (and the evaluation system) improves from real usage signals instead of noisy web search.

This example is one of many domains covered by Sugra's 1500+ live endpoints (markets, macro, climate, maritime, news, entities...).

## Relevance to Microsoft Global Hackathon 2026

Kevin Scott's *Hack for Continuous Agent Improvement* explicitly asks for agents that learn and adapt from real-world signals, telemetry, and evaluation systems.

Live primary data is the missing continuous signal.
