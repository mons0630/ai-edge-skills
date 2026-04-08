---
name: web-search
description: Search the internet for up-to-date information, recent news, current events, or any topic that may have changed after the model's training cutoff. Use this when the user asks about recent or real-time facts.
metadata:
  homepage: https://github.com/mons0630/ai-edge-skills/tree/main/web-search
---

# Web Search

## Instructions

Call the `run_js` tool using `index.html` and a JSON string for `data` with the following fields:

- **query**: Required. A concise, keyword-focused search query. Strip conversational words. Example: user asks "what is the latest iPhone model?" → query should be `latest iPhone model 2025`.
- **top_k**: Optional. Number of results to return. Default is 5. Use 3 for simple lookups, up to 10 for broad research topics.

**Constraints:**
- Always use this skill for time-sensitive questions (news, prices, sports scores, current events).
- Summarize the returned results in a concise answer. Do not list all raw results verbatim.
- If the search returns no relevant results, tell the user and suggest a refined query.
- Respond in the same language as the user's original prompt.
- If the user's question can be answered more deeply by fetching one of the result URLs, suggest using the `web-fetch` skill with that URL.
