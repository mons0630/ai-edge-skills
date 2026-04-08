---
name: web-fetch
description: Fetch and read the full text content of any public URL on the internet. Use this when the user asks to read, summarize, or extract information from a specific web page, article, or link.
metadata:
  homepage: https://github.com/mons0630/ai-edge-skills/tree/main/web-fetch
---

# Web Fetch

## Instructions

Call the `run_js` tool using `index.html` and a JSON string for `data` with the following fields:

- **url**: Required. The full URL (including https://) of the web page to fetch and read.
- **max_chars**: Optional. Maximum number of characters to return. Default is 4000. Use 1500 for a quick summary, up to 8000 for a deep read.

**Constraints:**
- Always pass a complete, valid URL starting with `https://` or `http://`.
- Summarize or answer from the returned content. Do not repeat raw text verbatim unless the user asks.
- If the page requires login, is paywalled, or returns an error, inform the user clearly.
- Respond in the same language as the user's original prompt.
- For finding URLs to fetch, first use the `web-search` skill, then fetch the most relevant result URL.
