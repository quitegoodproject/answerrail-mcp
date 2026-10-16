# AnswerRail MCP Server (`answerrail-mcp`)

[![npm version](https://img.shields.io/npm/v/answerrail-mcp.svg)](https://www.npmjs.com/package/answerrail-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

Official Model Context Protocol (MCP) stdio server for **AnswerRail** ([https://answerrail.com](https://answerrail.com)).
Audit any domain or URL directly inside Claude Desktop, Cursor, Windsurf, or any MCP client for:
- 🤖 **AI Crawler Readiness** (PerplexityBot, SearchGPT, GPTBot, ClaudeBot)
- ⚠️ **25,000-Token RAG Truncation Cliff** detection
- 📑 **/llms.txt Documentation Index** verification & generation
- 🔍 **Schema.org JSON-LD Entities** extraction
- 🏛️ **Google Lighthouse 13.5 Agentic Browsing** (`/.well-known/ai-catalog.json` ARD 1.0 schema)
- 🚀 **Byte-0 AST De-bloating** (converting heavy React/Next.js/Shopify DOM bloat into pristine GFM Markdown)

---

## 🛠️ Tools Included

### 1. `audit_ai_readiness`
Audit any website URL or domain for AI crawler readiness, 25k-token RAG truncation cliff, /llms.txt manifest presence, Schema.org JSON-LD entities, and Google Lighthouse 13.5 ARD 1.0 schema.
- **Input:** `url` (string, e.g. `https://stripe.com` or `example.com`)
- **Returns:** Detailed diagnostic report, token count, grade (A+ through F), and remediation links.

### 2. `generate_llms_txt_and_ard_catalog`
Generate a ready-to-deploy `/llms.txt` documentation index and Google Lighthouse 13.5 `/.well-known/ai-catalog.json` (ARD 1.0) manifest for any domain.
- **Input:** `domain` (string, e.g. `example.com`)
- **Returns:** Copy-paste Markdown `/llms.txt`, JSON `ai-catalog.json`, and HTML head links.

### 3. `fetch_byte0_markdown`
Strip React/Next.js hydration chunks, Shopify Liquid DOM bloat, and CSS cruft from any URL and return clean, Byte-0 GitHub-Flavored Markdown (GFM).
- **Input:** `url` (string, e.g. `https://example.com/pricing`)
- **Returns:** Clean GFM markdown representation.

---

## 🚀 Quickstart & Installation

### Claude Desktop
Add to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "answerrail": {
      "command": "npx",
      "args": ["-y", "answerrail-mcp"]
    }
  }
}
```

### Cursor
Add to Cursor Settings -> Features -> MCP Servers:
- **Name:** `answerrail`
- **Type:** `command`
- **Command:** `npx -y answerrail-mcp`

### Windsurf
Add to `~/.codeium/windsurf/mcp_config.json`:

```json
{
  "mcpServers": {
    "answerrail": {
      "command": "npx",
      "args": ["-y", "answerrail-mcp"]
    }
  }
}
```

---

## 🌐 Links
- **Official Website:** [https://answerrail.com](https://answerrail.com)
- **Lighthouse 13.5 ARD 1.0 Spec Guide:** [https://answerrail.com/geo/lighthouse-agentic-browsing-ai-catalog-json-llms-txt](https://answerrail.com/geo/lighthouse-agentic-browsing-ai-catalog-json-llms-txt)
- **GitHub Repository:** [https://github.com/quitegoodproject/answerrail-mcp](https://github.com/quitegoodproject/answerrail-mcp)

License: MIT
