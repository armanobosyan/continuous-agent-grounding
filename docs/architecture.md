# Architecture

## High-level view

```
User / Agent
    ↓
MCP Client (Azure AI Foundry / Copilot Studio / custom agent)
    ↓
Sugra MCP Server
    ↓
Sugra Live Primary Data API
    ↓
Primary Sources (markets, macro, climate, maritime, news, entities...)
```

## Key components

1. **Live Primary Data API**
   - 1500+ endpoints
   - Consistent LLM-ready JSON envelope
   - Source + timestamp on every response

2. **MCP Server**
   - Native tool discovery and calling
   - Works with Claude, GPT, Gemini, xAI and any MCP-compatible client

3. **Critic / Evaluation Layer** (hackathon focus)
   - Uses the same live data as ground truth
   - Measures accuracy and confidence calibration
   - Creates continuous improvement signal

## Continuous Improvement Loop

1. Agent makes a claim about the real world
2. Live data is retrieved with source + timestamp
3. Critic compares agent output vs primary data
4. Feedback is logged and can be used for future improvement
