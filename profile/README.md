<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/braincol/.github/main/profile/braincol-banner-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/braincol/.github/main/profile/braincol-banner-light.svg">
    <img alt="Braincol" src="https://raw.githubusercontent.com/braincol/.github/main/profile/braincol-banner-dark.svg" width="600">
  </picture>
</p>

<p align="center">
  <strong>Building the infrastructure for AI-native enterprises.</strong>
</p>

<p align="center">
  Secure credential management, intelligent monitoring, and open security standards<br/>
  for the next generation of enterprise software.
</p>

<p align="center">
  <a href="https://braincol.com">Website</a> &middot;
  <a href="https://github.com/braincol/braincol-vault">Vault</a> &middot;
  <a href="https://github.com/braincol/braincol-sentry">Sentry</a> &middot;
  <a href="https://github.com/braincol/never-leak-protocol">NL Protocol</a>
</p>

---

### What we build

<table>
  <tr>
    <td width="33%" valign="top">
      <h4>🔐 <a href="https://github.com/braincol/braincol-vault">Braincol Vault</a></h4>
      The first secret manager purpose-built for AI coding agents. Secrets are used but never visible to the LLM. Reference implementation of the Never Leak Protocol.<br/><br/>
      <a href="https://github.com/braincol/braincol-vault"><img src="https://img.shields.io/badge/v1.0-Released-22C55E?style=flat-square" alt="Released"/></a>
    </td>
    <td width="33%" valign="top">
      <h4>📡 <a href="https://github.com/braincol/braincol-sentry">Braincol Sentry</a></h4>
      Source-agnostic agentic intelligence platform. Connects to any data source, detects anomalies with AI, and explains what happened and why.<br/><br/>
      <a href="https://github.com/braincol/braincol-sentry"><img src="https://img.shields.io/badge/status-Active_Development-3B82F6?style=flat-square" alt="Active Development"/></a>
    </td>
    <td width="33%" valign="top">
      <h4>🛡️ <a href="https://github.com/braincol/never-leak-protocol">Never Leak Protocol</a></h4>
      Open standard for AI agent secret governance. 7 levels of defense. Agents request actions, not secrets.<br/><br/>
      <a href="https://github.com/braincol/never-leak-protocol"><img src="https://img.shields.io/badge/spec-v1.0-8B5CF6?style=flat-square" alt="v1.0 Spec"/></a>
    </td>
  </tr>
</table>

---

### Braincol Sentry

Most monitoring tools are source-specific, reactive, rules-based, and bolt on multi-tenancy as an afterthought. Sentry is the opposite on every dimension.

**The problem:** Organizations have no unified way to understand, monitor, and investigate anomalies across their entire data landscape. You end up with Datadog for metrics, Splunk for logs, custom scripts for correlation, and manual alert tuning &mdash; 3+ vendors, zero cross-source intelligence.

**What Sentry does differently:**

- **Source-agnostic AI agent** &mdash; The agent understands *concepts* (aggregation, cardinality, drift, anomalies), not specific databases. Add a new data source by creating an MCP server; the agent uses it automatically without code changes. Same anomaly detection works across Elasticsearch, Postgres, S3, data warehouses, or any API.

- **LLM reasons, Python computes** &mdash; The LLM handles intent classification, hypothesis generation, and explanation. Heavy math (z-scores, MAD, STL decomposition, changepoints) runs in Python with Polars/SciPy. Result: intelligence at 10x lower token cost than alternatives.

- **Deny-by-default security** &mdash; Every operation goes through a Policy Decision Point (PDP) that returns not just allow/deny, but *obligations*: redact PII, limit to 100 rows, restrict tools, enforce budget. PDP unavailable? Deny everything. No policy exists? Deny. Fail-closed, always.

- **Immutable audit trail** &mdash; Append-only, hash-chained, monotonic sequences, WORM-anchored. Legal holds prevent purge. Every access, every policy decision, every agent action &mdash; cryptographically verifiable. Built for SOX, HIPAA, GDPR, and PCI-DSS auditors.

- **Multi-tenancy from day one** &mdash; Organization &rarr; Workspace isolation. `workspaceId` mandatory on every query. Secrets accessed via lease/redeem pattern (JWE encrypted, single-use tokens, 60s TTL). Cross-tenant access returns 404, not 403 &mdash; don't even reveal existence.

**Four-plane architecture:**

```
Trust & Money       ──  Auth, PDP, billing, encrypted secrets, immutable audit (NestJS)
Product / Control   ──  Connectors, resources, versioned artifacts, job orchestration (NestJS)
Execution / Reason  ──  LangGraph workflows, MCP tools, anomaly detection, Polars (Python)
Presentation        ──  Chat interface, streaming responses, real-time dashboards (Next.js)
```

Each plane is independently deployable, independently scalable, and architecturally isolated. The agent plane can crash without affecting auth. The security plane can't execute business logic. By design, not by discipline.

---

### Braincol Vault

Every AI coding agent (Claude Code, Cursor, Copilot, Codex) has a fundamental flaw: when you give it a secret, that secret enters the LLM context window. Braincol Vault prevents this entirely.

- **5-layer defense** &mdash; Instructions &rarr; Permissions &rarr; Interception &rarr; MCP opaque proxy &rarr; Cryptography (X25519 + ChaCha20-Poly1305)
- **7 agent integrations** &mdash; Claude Code, Cursor, Copilot, Codex, Windsurf, Aider, and generic MCP
- **`{{nl:namespace/SECRET}}` placeholders** &mdash; Agents request actions, never receive values
- **Multi-user RBAC** &mdash; Admin, Editor, Viewer with per-project, per-environment scoping
- **2,655 tests** &mdash; Security, unit, integration, and E2E coverage
- **Zero custom crypto** &mdash; Built on pyrage (age-encryption standard)

### Never Leak Protocol

The open standard (Apache 2.0) that defines how AI agents must interact with secrets. Braincol Vault is its first implementation.

| Level | Defense | What it does |
|-------|---------|-------------|
| L1 | Agent Identity | Cryptographic identity, trust tiers, JWT-based |
| L2 | Action-Based Access | Opaque handles &mdash; agents request actions, never see values |
| L3 | Execution Isolation | Subprocess sandboxing, environment scrubbing, memory wipe |
| L4 | Pre-Execution Defense | Command interception, prompt injection detection |
| L5 | Audit & Integrity | SHA-256 hash-chained, tamper-evident audit records |
| L6 | Attack Detection | Behavioral anomaly detection, automatic circuit breakers |
| L7 | Cross-Agent Trust | Delegation tokens with scope attenuation |

**Conformance tiers:** Basic (L1-L3) for startups, Standard (L1-L5) for SaaS teams, Advanced (L1-L7) for enterprise and regulated industries. Aligned with OWASP Top 10 for LLMs, MCP, and Agentic Apps.

---

### Tech Stack

`TypeScript` `Python` `NestJS` `FastAPI` `Next.js` `React 19` `LangGraph` `MongoDB` `Redis` `Turborepo` `Polars` `Zod` `Pydantic`

---

<p align="center">
  <a href="https://braincol.com">braincol.com</a>
  <br/><br/>
  <sub>Built in Colombia &mdash; Security &amp; intelligence infrastructure for the agentic future.</sub>
</p>
