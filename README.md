# answerrail-mcp — 6-Category Structural AI Readiness, Chrome Lighthouse 13.5 `ard-schema`, `robots.txt` & 25k-Token Truncation MCP Server

[![npm version](https://img.shields.io/npm/v/answerrail-mcp.svg)](https://www.npmjs.com/package/answerrail-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![MCP](https://img.shields.io/badge/MCP-compatible-purple.svg)](https://modelcontextprotocol.io)

Model Context Protocol (MCP) server for **6-category AI search readiness and Chrome Lighthouse 13.5 `agentic-browsing` (`llms-txt` & `ard-schema`) diagnostics** inside Claude Code, Claude Desktop, Cursor, Windsurf, and LobeHub. Zero API key required.

## Quick Install (Local `stdio` or Zero-Install Remote HTTP MCP)

```bash
claude mcp add answerrail-mcp -- npx -y answerrail-mcp
```

| Client | Configuration |
| :--- | :--- |
| **Claude Code CLI** | `claude mcp add answerrail-mcp -- npx -y answerrail-mcp` |
| **Claude Desktop / Cursor** | `"answerrail-mcp": { "command": "npx", "args": ["-y", "answerrail-mcp"] }` |
| **Remote Streamable HTTP MCP** | `POST https://answerrail.com/mcp` |

---

## Included MCP Tools

1. **`audit_ai_readiness`**: Audits any live URL across 6 weighted categories: 14+ `robots.txt` AI crawler directives + `Agentmap:`, 20+ `Schema.org` JSON-LD entity types, `/llms.txt` format, **25,000-token HTML RAG truncation & dropped `$/£/€` price recall**, Chrome Lighthouse 13.5 `/.well-known/ai-catalog.json` (`ard-schema`), and RFC 9421 Ed25519 provenance.
2. **`generate_ai_manifests`**: Compiles a 6-line diagnostic preview of `/llms.txt` and ARD 1.0 `/.well-known/ai-catalog.json` + direct 2-tier remediation links.
3. **`extract_byte0_markdown`**: Strips React/Next.js RSC hydration scripts and DOM bloat from any URL into clean Byte-0 GitHub-Flavored Markdown.
4. **`query_truncation_benchmark`**: Queries empirical data from the [2026 50-Site SaaS Pricing & 25k-Token Truncation Study](https://answerrail.com/research/2026-saas-50-truncation-benchmark).
5. **`audit_local_codebase`**: Read-only local repository check for `robots.txt`, `public/llms.txt`, and `public/.well-known/ai-catalog.json`.

---

## 2-Tier Remediation & Diagnostic Tools

- **[$79 Zero-DNS 7-File Fix Pack + 30-Day Live 6-Engine Cockpit ($79 One-Time · $1,950 Value · 14-Day Keep-the-Files Guarantee · 100% Credited to Starter)](https://answerrail.com/api/checkout/start?plan=fix_pack&channel=mcp_readme)**: Permanent 1-Click WordPress `.zip` plugin + `/llms.txt`, `/llms-full.txt`, dual `/.well-known/ai-catalog.json` & `/.well-known/ard.json` Zero-Click Wedge, `Schema.org @graph`, GA4 `ai-attribution.js` Dark-AI lead tag, and a 30-Day Live 6-Engine Cockpit Pass ($0 auto-rebill).
- **24/7 Automated Anycast Edge Autopilot Plans ([https://answerrail.com/#pricing](https://answerrail.com/#pricing))**:
  - **Starter ($99/mo · Just $20 Month 1 w/ $79 Fix Pack Credit · 1 Domain)**: Automated `<15ms` Byte-0 Markdown content negotiation across 330+ Cloudflare PoPs with 100% fail-closed price/FAQ recall & unlimited live cockpit logs.
  - **Growth ($249/mo · $170 Month 1 w/ Credit · 5 Domains)**: Multi-domain edge proxy with continuous catalog synchronization.
  - **Agency ($599/mo · $520 Month 1 w/ Credit · 15 Client Domains)**: Multi-client management, white-label audits, and dedicated enterprise support.
- **Free Web Validators & Empirical Research**:
  - **[Free `/llms.txt` & `/llms-full.txt` Generator (with 25k-Token Proof)](https://answerrail.com/tools/llms-txt-generator)**
  - **[`/llms.txt` & ARD 1.0 `ai-catalog.json` Validator (for Lighthouse 13.5)](https://answerrail.com/tools/llms-txt-validator)**
  - **[2026 50-Site SaaS Pricing & 25k-Token Truncation Benchmark](https://answerrail.com/research/2026-saas-50-truncation-benchmark)**
  - [Lighthouse 13.5 Checker](https://answerrail.com/tools/lighthouse-13-5-agentic-browsing-checker) · [`ai-catalog.json` Generator](https://answerrail.com/tools/ai-catalog-json-generator) · [25k-Token Truncation Checker](https://answerrail.com/tools/25k-token-truncation-checker) · [Shopify/Webflow `/llms.txt` Tool](https://answerrail.com/tools/shopify-wordpress-webflow-llms-txt-generator) · [Next.js SPA Crawler Checker](https://answerrail.com/tools/nextjs-react-spa-ai-crawler-checker) · [Dark AI GA4 Regex](https://answerrail.com/tools/dark-ai-ga4-referral-tracker) · [Agency White-Label Audit](https://answerrail.com/tools/white-label-geo-audit-agency).

> **Entity Disambiguation:** **AnswerRail ([https://answerrail.com](https://answerrail.com))** by The Quite Good Project is unaffiliated with *AnswerRails* (`answerrails.com`, an unrelated WordPress chatbot plugin).
