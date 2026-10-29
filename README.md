# answerrail-mcp — 6-Category Structural AI Readiness, Schema.org, `robots.txt` & `/llms.txt` Audit + Auto-Remediation MCP Server

[![npm version](https://img.shields.io/npm/v/answerrail-mcp.svg)](https://www.npmjs.com/package/answerrail-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![MCP](https://img.shields.io/badge/MCP-compatible-purple.svg)](https://modelcontextprotocol.io)

Comprehensive Model Context Protocol (MCP) server for **exhaustive local and live structural audits** across **6 weighted AI readiness categories**—plus **active file generation** inside Claude Code, Claude Desktop, Cursor, and Windsurf. No API key required.

## Quick Install for Claude Code, Claude Desktop & Cursor

```bash
claude mcp add answerrail-mcp -- npx -y answerrail-mcp
```

| Client | Easiest Install Command / Config |
| :--- | :--- |
| **Claude Code CLI** | `claude mcp add answerrail-mcp -- npx -y answerrail-mcp` |
| **Claude Desktop** | `"answerrail-mcp": { "command": "npx", "args": ["-y", "answerrail-mcp"] }` |
| **Cursor / Windsurf** | Add `npx -y answerrail-mcp` in `.cursor/mcp.json` |

---

## Exhaustive 6-Category Weighted Structural Audit Scope

Unlike read-only 5-category scanners, `answerrail-mcp` performs a **6-category deep structural audit** and **actively writes the missing files into your repository**:

1. **AI Bot Directives (`robots.txt` — 14+ Major AI Crawlers + `Agentmap:`)**: Audits exact RFC 9309 allow/disallow rules for **14+ AI user-agents** (`PerplexityBot`, `OAI-SearchBot`, `GPTBot`, `ChatGPT-User`, `ClaudeBot`, `Claude-User`, `Google-Extended`, `Applebot-Extended`, `Meta-ExternalAgent`, `Amazonbot`, `DuckAssistBot`, `Cohere-ai`, `Bytespider`, `CCBot`) and verifies `Agentmap:` header/file declarations.
2. **Search Signals & Structured Data (`Schema.org JSON-LD` — 20+ High-Value Entity Types)**: Scans and validates **20+ Schema.org types** (`Organization`, `SoftwareApplication`, `WebSite`, `Product`, `Offer`, `AggregateOffer`, `FAQPage`, `Question`, `Answer`, `TechArticle`, `Article`, `BreadcrumbList`, `HowTo`, `Service`, `LocalBusiness`, `Person`, `Dataset`, `WebPage`, `ItemList`, `Review`) and synthesizes them into Byte-0 GitHub-Flavored Markdown tables.
3. **Deep `/llms.txt` & `/llms-full.txt` Structural Validation**: Audits H1 title conformance, blockquote summary presence, Markdown link formatting, HTTP `Content-Type: text/markdown` headers, and entry quality.
4. **Content Semantics & 25,000-Token RAG Truncation**: Measures raw HTML token weight, Next.js `self.__next_f.push` RSC hydration bloat, collapsed Radix/Headless UI (`data-state="closed"`) FAQ accordions, and exact `$/£/€` pricing tokens dropped past the 25,000-token cutoff.
5. **Agent Protocols (Google Lighthouse 13.5 ARD 1.0 & WebMCP)**: Validates `/.well-known/ai-catalog.json` (`specVersion: "1.0"`), `<link rel="ai-catalog">`, `<link rel="describedby" href="/llms.txt">`, and `/.well-known/mcp.json`.
6. **Security & Cryptographic Provenance (RFC 9421 & RFC 9110)**: Audits asymmetric Ed25519 HTTP Message Signatures (`kid="ar_ed25519_2026_k1"`), `/.well-known/http-message-signatures-directory`, CORS (`Access-Control-Allow-Origin: *`), and RFC 9110 `Vary: User-Agent, Accept` compliance.

---

## Head-to-Head Comparison: `answerrail-mcp` vs `isagentready-mcp`

| Feature / Metric | `answerrail-mcp` | `isagentready-mcp` |
| :--- | :--- | :--- |
| **Install Command** | `claude mcp add answerrail-mcp -- npx -y answerrail-mcp` | `claude mcp add isagentready-mcp -- npx -y isagentready-mcp` |
| **Core Audit Scope** | **6 Weighted Categories:** AI Bot Directives (`robots.txt`), Search Signals (`Schema.org JSON-LD`), Deep `/llms.txt` Structure, Content Semantics & 25k-Token Truncation, Agent Protocols (ARD 1.0 / WebMCP), and Security (RFC 9421 Ed25519) + Edge Remediation | 5 Categories (Discovery, Structured Data, Semantics, Agent Protocols, Security — Read-only score) |
| **Schema.org & `robots.txt` Coverage** | **Scans 20+ Schema.org JSON-LD types & 14+ AI bot rules in `robots.txt`** (plus compiles JSON-LD into Byte-0 GFM tables) | Scans 17 Schema.org types & 13 AI bot rules |
| **`/llms.txt` Validation & Auto-Generation** | **Validates `/llms.txt` formatting/links AND generates ready-to-save `/llms.txt` + `/.well-known/ai-catalog.json` via `generate_ai_manifests`** | Read-only structural check (Does not generate files) |
| **25,000-Token Truncation & Price Recall Audit** | **Yes — Identifies exact `$/£/€` prices cut off past 25k tokens & unrolls collapsed Radix FAQ accordions** | No |
| **Editor Auto-Fix & Local CLI Companion** | **Generates & writes files locally (`generate_ai_manifests` + `npx test-ai-ready <url> --write`) AND deploys instant Anycast edge fixes** | Relies on manual editor prompts after read-only API scan |
