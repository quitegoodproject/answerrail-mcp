# AnswerRail MCP Server (`answerrail-mcp`)

[![npm version](https://img.shields.io/npm/v/answerrail-mcp.svg)](https://www.npmjs.com/package/answerrail-mcp)
[![Glama MCP Score](https://glama.ai/mcp/servers/quitegoodproject/answerrail-mcp/badges/score.svg)](https://glama.ai/mcp/servers/quitegoodproject/answerrail-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

Official Model Context Protocol (MCP) server for **AnswerRail** ([https://answerrail.com](https://answerrail.com)) — available both as a **local stdio server** (`npx -y answerrail-mcp`) and a **zero-install Remote Streamable HTTP server** (`https://answerrail.com/mcp`).

Audit any domain or URL directly inside Claude Desktop, Claude Code, Cursor, Windsurf, or any MCP client for:
- **AI Crawler Readiness** (`PerplexityBot`, `OAI-SearchBot`, `GPTBot`, `ClaudeBot`, `Google-Extended`)
- **25,000-Token RAG Truncation Cliff** detection & dropped pricing token diagnostics
- **`/llms.txt` & `/llms-full.txt` Documentation Index** verification & compilation
- **Google Lighthouse 13.5 `agentic-browsing`** (`/.well-known/ai-catalog.json` ARD 1.0 schema & `robots.txt` `Agentmap:` directive)
- **Byte-0 AST De-bloating** (converting heavy React/Next.js/Shopify DOM bloat into clean GitHub-Flavored Markdown)

---

## Tools Included (v1.0.2)

### 1. `audit_ai_readiness`
Perform a live, read-only diagnostic audit of a website URL or domain for AI search readiness, measuring HTML token weight against the 25,000-token RAG truncation limit, `/llms.txt` manifest availability, Google Lighthouse 13.5 `/.well-known/ai-catalog.json` (ARD 1.0) conformance, `robots.txt` `Agentmap:` directives, and Schema.org JSON-LD entities.
- **Input:** `url` (string, e.g. `https://stripe.com/pricing` or `example.com`)

### 2. `generate_ai_manifests`
Generate ready-to-deploy `/llms.txt` Markdown and Google Lighthouse 13.5 `/.well-known/ai-catalog.json` (ARD 1.0) JSON manifests for a target domain, plus `robots.txt` `Agentmap:` and HTML `<head>` discovery `<link>` tags.
- **Input:** `domain` (string, e.g. `example.com`)

### 3. `extract_byte0_markdown`
Fetch a live web page, strip React/Next.js hydration chunks, Shopify Liquid DOM bloat, scripts, and navigation cruft, and return clean Byte-0 GitHub-Flavored Markdown (GFM) alongside before/after token telemetry.
- **Input:** `url` (string, e.g. `https://example.com/pricing`)

### 4. `query_truncation_benchmark`
Query empirical data from the 2026 50-Site B2B SaaS Pricing Page Truncation Benchmark (`87%` publish `/llms.txt`, yet `74%` still truncate `/pricing` HTML past 25,000 tokens).
- **Input:** `domain` (optional string, e.g. `vercel.com`, `supabase.com`, or omit for full cohort summary)

---

## Quickstart & Installation

### Option A: Zero-Install Remote HTTP Server (`https://answerrail.com/mcp`)

**Claude Code CLI:**
```bash
claude mcp add --transport http answerrail https://answerrail.com/mcp
```

**Cursor / Windsurf / Remote HTTP Clients:**
```json
{
  "mcpServers": {
    "answerrail": {
      "url": "https://answerrail.com/mcp"
    }
  }
}
```

### Option B: Local Stdio Server (`npx -y answerrail-mcp`)

**Claude Desktop (`claude_desktop_config.json`) / Cursor / Windsurf:**
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

## Links & Technical Implementation Guides
- **Official Website:** [https://answerrail.com](https://answerrail.com)
- **Remote MCP Endpoint:** [https://answerrail.com/mcp](https://answerrail.com/mcp)
- **Glama Registry:** [https://glama.ai/mcp/servers/quitegoodproject/answerrail-mcp](https://glama.ai/mcp/servers/quitegoodproject/answerrail-mcp)
- **How to Pass Google Lighthouse 13.5 `agentic-browsing` (`llms-txt` & `ard-schema` / `ai-catalog.json`):** [https://answerrail.com/geo/lighthouse-agentic-browsing-ai-catalog-json-llms-txt](https://answerrail.com/geo/lighthouse-agentic-browsing-ai-catalog-json-llms-txt)
- **50-Site Empirical SaaS Truncation Benchmark:** [https://answerrail.com/research/2026-saas-50-truncation-benchmark](https://answerrail.com/research/2026-saas-50-truncation-benchmark)
- **Shopify, Webflow & WordPress `/llms.txt` Cloudflare Worker Guide:** [https://answerrail.com/geo/generate-llms-txt-shopify-wordpress-webflow](https://answerrail.com/geo/generate-llms-txt-shopify-wordpress-webflow)
- **GA4 Custom Channel Group Regex for AI Search Traffic:** [https://answerrail.com/geo/track-chatgpt-perplexity-referral-traffic-ga4](https://answerrail.com/geo/track-chatgpt-perplexity-referral-traffic-ga4)
- **2026 AEO & GEO Tools Matrix:** [https://answerrail.com/geo/best-generative-engine-optimization-tools](https://answerrail.com/geo/best-generative-engine-optimization-tools)
- **In-Repo Lighthouse 13.5 ARD 1.0 Guide:** [docs/LIGHTHOUSE_13_5_AGENTIC_BROWSING_GUIDE.md](./docs/LIGHTHOUSE_13_5_AGENTIC_BROWSING_GUIDE.md)

License: MIT
