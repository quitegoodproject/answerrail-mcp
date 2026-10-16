# AnswerRail MCP Server (`answerrail-mcp`)

[![quitegoodproject/answerrail-mcp MCP server](https://glama.ai/mcp/servers/quitegoodproject/answerrail-mcp/badges/score.svg)](https://glama.ai/mcp/servers/quitegoodproject/answerrail-mcp)
[![npm version](https://img.shields.io/npm/v/answerrail-mcp.svg)](https://www.npmjs.com/package/answerrail-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

Official **Model Context Protocol (MCP)** server for [AnswerRail](https://answerrail.com) — audit any URL for **Perplexity / ChatGPT 25,000-token HTML truncation**, **`/llms.txt` discovery**, **Google Lighthouse 13.5 `ard-schema` (`/.well-known/ai-catalog.json` ARD 1.0)**, and compile clean **Byte-0 Markdown** directly inside Claude Desktop, Cursor, Windsurf, or any MCP client.

## Quick Start (`npx`)

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

## Exposed MCP Tools, Resources & Prompts

### Tools
1. **`audit_ai_readiness`** — Audits any URL for 25,000-token RAG HTML truncation, visible price omission past byte 100,000, `/llms.txt`, Google Lighthouse 13.5 `ard-schema` (`/.well-known/ai-catalog.json`), and JSON-LD Schema.org entities.
2. **`generate_llms_txt_and_ard_catalog`** — Generates ready-to-save `/llms.txt` and `/.well-known/ai-catalog.json` (ARD 1.0) manifests for any website.
3. **`fetch_byte0_markdown`** — Compiles a webpage into clean Byte-0 Markdown via the AnswerRail Edge Engine.

### Resources
- `https://answerrail.com/api/benchmark/2026-saas-50` — 2026 50-Site SaaS Truncation & `/llms.txt` Paradox Empirical Benchmark JSON.
- `https://answerrail.com/llms.txt` — Official AnswerRail AI documentation index.

### Prompts
- `audit-website-ai-readiness` — Structured prompt to audit any domain's 25k-token RAG window and Lighthouse 13.5 ARD 1.0 compliance.

## License
MIT © [The Quite Good Project](https://answerrail.com)
