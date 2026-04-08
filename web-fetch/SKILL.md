---
name: web-fetch
description: Fetch and read the text content of any public URL on the internet. Use this when the user asks to read, summarize, or extract information from a specific web page or article link.
metadata:
  homepage: https://github.com/mons0630/ai-edge-skills/tree/main/web-fetch
---

# Web Fetch

## Instructions

Call the `run_js` tool using `index.html` and a JSON string for `data` with the following fields:

- **url**: Required. The full URL (including https://) of the web page to fetch and read.
- **max_chars**: Optional. Maximum number of characters to return. Default is 4000. Use a lower value like 1500 for very long pages to save context.

**Constraints:**
- Always pass a complete, valid URL starting with `https://` or `http://`.
- Summarize the returned content concisely. Do not repeat the raw text verbatim.
- If the page requires login or is paywalled, inform the user that the page could not be fully read.
- Respond in the same language as the user's original prompt.
