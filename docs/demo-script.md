# Demo Script (2-minute video)

## Structure

1. **Problem (20–25 sec)**  
   Show a typical agent answering a live operational question.  
   **Concrete example (this recording, 24 Aug 2026):**  
   Query: “What is the current daily shipping activity through the main global chokepoints (Hormuz, Suez, Malacca, Panama)? Give the latest available ship/transit counts by type.”  
   - ChatGPT spends **2 minutes 17 seconds** searching 7+ websites  
   - Constant reconciliation of conflicting methodologies (AIS vs official canal counts vs Kpler vs UKMTO)  
   - Especially broken on Hormuz (data distorted, traffic ~90% below baseline, vessel categories diverge)  
   - Final answer: approximate table full of caveats and residual “Other”  
   → Classic confidence trap: fluent, slow, secondary-sourced, not continuously improvable.

2. **Solution (30 sec)**  
   Introduce the live primary-data layer + MCP tools.  
   Show one clean tool call returning structured, source-attributed, timestamped numbers from Sugra maritime endpoints.

3. **Before / After (40 sec)**  
   Side-by-side comparison:  
   - Baseline (web-search agent) – the recording above  
   - Same query grounded with Sugra MCP → instant structured primary data with attribution + timestamps  
   - Clear differences in latency, accuracy, citation quality, and usability

4. **Continuous Improvement (20 sec)**  
   Explain how live primary data creates a feedback loop:  
   the same signals used for answers become ground truth for the critic / evaluation system.  
   Because the primary data is the same source the critic uses for evaluation, every production query becomes a training/evaluation signal — closing the loop at individual, team and organizational level (exactly Kevin Scott’s challenge).

5. **Closing (10 sec)**  
   One-line summary + call to action for Continuous Agent Improvement.

## Key metrics to show

- Latency: 2m+ → <2s
- Accuracy uplift (example: web search ~71% vs live data layer ~97%)
- Presence of source attribution and timestamps
- Reduced hallucinations / residual uncertainty on factual live questions
