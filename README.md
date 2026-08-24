# Continuous Agent Grounding

**Microsoft Global Hackathon 2026**  
Executive Challenge: *Hack for Continuous Agent Improvement*

> Agents improve only when grounded in reliable real-world signals.

## Problem

Most AI agents still rely on:
- Static training data (knowledge cut-off)
- Noisy and inconsistent web search

This creates the **confidence trap** — fluent answers that are outdated, incomplete, or confidently wrong.

Without continuous real-world signals, agents cannot meaningfully improve over time.

## Solution

We provide a **live primary-data grounding layer** that agents can use as a continuous improvement signal.

### Key components

- **Live Primary Data API** — 1500+ endpoints across markets, macroeconomics, climate, maritime, news, entity screening and more
- **MCP Server** — turns the entire catalog into native agent tools (search, describe, call)
- **LLM-ready responses** — consistent envelope with source attribution + timestamps
- **Critic / Evaluation pattern** — uses the same live data as ground truth

## What we are building during the Hackathon

1. Clear before/after demonstration of agent quality with vs without live grounding
2. Lightweight critic & evaluation layer based on live primary data
3. Integration patterns with Microsoft agent surfaces (Azure AI Foundry / Copilot Studio style)
4. Measurable continuous improvement loop

## Repository Structure
