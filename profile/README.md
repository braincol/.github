<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/braincol/.github/main/profile/braincol-banner-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/braincol/.github/main/profile/braincol-banner-light.svg">
    <img alt="Braincol" src="https://raw.githubusercontent.com/braincol/.github/main/profile/braincol-banner-dark.svg" width="600">
  </picture>
</p>

<h3 align="center">Enterprise-grade solutions for the AI agent era</h3>

<p align="center">
  We build security &amp; intelligence infrastructure that solves real problems<br/>
  in agentic technologies &mdash; multi-agent systems, secret governance, and anomaly detection.
</p>

---

### What we build

| Project | Description | Status |
|---------|-------------|--------|
| **Braincol Sentry** | Agentic, source-agnostic data intelligence platform. Four-plane architecture for financial monitoring & analysis with AI agent capabilities. | Active Development |
| **Braincol Vault** | Local-first secret manager for the AI agent era. Reference implementation of the Never Leak Protocol. Ensures secrets are used but never visible to AI agents. | v1.0 Released |
| **Never Leak Protocol** | The open standard for AI agent secret governance. Agents request actions, not secrets. 7 levels of defense. | v1.0 Specification |

---

### Braincol Sentry

An agentic data intelligence platform with a four-plane architecture:

```
Trust & Money Plane     ──  Auth, policy, billing, secrets, audit
Product / Control Plane ──  Connectors, resources, jobs, artifacts
Execution / Reasoning   ──  LLM workflows, MCP tools, anomaly detection
Presentation Plane      ──  Dashboards, real-time visualizations
```

Built with NestJS, FastAPI, Next.js, LangGraph, MongoDB, and Redis. Designed for enterprise-grade financial monitoring, anomaly analysis, and AI-driven investigation at the highest levels of intelligence and security.

### Braincol Vault

The first secret manager purpose-built for AI coding agents. Every AI agent (Claude Code, Cursor, Copilot, etc.) has a fundamental flaw: when given a secret, it enters the LLM context window. Braincol Vault prevents this entirely.

- **5-layer defense architecture** &mdash; From instructions to cryptography (X25519 + ChaCha20-Poly1305)
- **7 agent integrations** &mdash; Claude Code, Cursor, Copilot, Codex, Windsurf, Aider, and generic MCP
- **Multi-user RBAC** &mdash; Admin, Editor, Viewer roles with per-project scoping
- **2,128+ tests** &mdash; Comprehensive security, unit, integration, and E2E coverage

### Never Leak Protocol

An open standard (Apache 2.0) that defines how AI agents must interact with secrets without them ever entering the LLM context.

**7 Levels of Defense:**

| Level | Name | Purpose |
|-------|------|---------|
| L1 | Agent Identity | Cryptographic identity and trust levels |
| L2 | Action-Based Access | Agents request actions, not secrets |
| L3 | Execution Isolation | Subprocess execution, env scrubbing |
| L4 | Pre-Execution Defense | Command interception, injection detection |
| L5 | Audit & Integrity | SHA-256 hash-chained, tamper-evident records |
| L6 | Attack Detection | Behavioral anomaly detection, circuit breakers |
| L7 | Cross-Agent Trust | Delegation tokens, scope attenuation |

Aligned with OWASP Top 10 for LLMs, MCP, and Agentic Apps.

---

### Tech Stack

`TypeScript` `Python` `NestJS` `FastAPI` `Next.js` `React` `LangGraph` `MongoDB` `Redis` `Turborepo`

---

<p align="center">
  <sub>Braincol &mdash; Building the security & intelligence infrastructure for the agentic future.</sub>
</p>
